---
name: wechat-draft
description: 将现成 Markdown 用主题和排版模板转换为微信公众号草稿。适用于排版预览、发送或更新微信草稿；不负责写作、群发或第三方图床。
---

# 微信草稿助手

使用随包脚本 `scripts/wechat-draft.cjs`，需要 Node.js 22 或更新版本；没有 npm 安装步骤。所有路径相对本 Skill 所在目录解析，不能假定 Agent 的当前目录就是这里。

## 首次配置区（安装后由用户修改）

- 私有配置文件路径：`待用户指定`
- 默认主题：`classic`
- 默认排版模板：`balanced`
- 默认文章目录：`待用户指定`

首次运行时请用户按自己的环境修改上面这一区域。可以在用户授权后代为填写路径和排版偏好，**不能把 AppSecret 写进 SKILL.md**。将 `config.example.json` 复制到用户选择的、仓库外的私有目录，由用户填写自己的 AppID、AppSecret、作者和封面路径。Unix 上将配置文件权限设为 600。不得读取作者或其他插件的凭证，不打印配置文件、token 或完整请求 URL。

只需要微信公众号开发凭证；此工具不调用大模型 API，不需要另外购买模型接口。公众号需具备草稿接口权限，并将运行电脑的出口 IP 加入微信白名单。

安装时把整个 `wechat-draft` 文件夹放入 Agent 的 skills 目录。Codex 默认使用 `~/.codex/skills/`；其他 Agent（如 Kimi Code）应先检查其本机配置或官方安装说明，使用该 Agent 实际支持的 skills 目录，不要改动无关配置。

## 工作流程

1. 确定用户指定的 Markdown 文件、标题、主题与排版模板，不默认读取当前笔记或整个知识库。
2. 使用 `node scripts/wechat-draft.cjs themes` 列出可用主题与模板。
3. 离线预览：`node scripts/wechat-draft.cjs preview --input /文章绝对路径.md --output /新的预览路径.html --theme classic --template balanced`。输出文件已存在时会拒绝覆盖。向用户展示排版与将使用的标题、作者、封面。
4. 仅预览请求到此结束。用户明确要求发送草稿时执行：`node scripts/wechat-draft.cjs send --input /文章绝对路径.md --config /私有配置路径.json --title "文章标题" --theme classic --template balanced`。已有明确发送授权不重复确认；仅请求排版或预览不等于发送授权。
5. 保存命令返回的 `mediaId` 到用户允许的本地任务记录。再次更新时传 `--media-id`；脚本先校验草稿存在，失效会停止，不自动新建。更新多篇图文中的第一篇前需确认该目标就是用户希望修改的文章。
6. 提交超时或网络错误时停止，提示用户到微信草稿箱核对，不能盲目重试创建。成功只表示已送入草稿箱，最终发布由用户在微信后台操作。

## 图片与格式边界

支持共享内核的 17 个主题、排版模板、标准 Markdown、表格、代码高亮与引用。独立版本不具备 Obsidian 的公式/Mermaid 栅格化或 Wiki 图片解析能力；遇到这些格式先转换为标准图片，不把源码直接发送。

无需第三方图床。正文支持文章目录下的 PNG/JPEG 本地图片，脚本直接上传微信正文图片接口，重复图片只上传一次但逐一替换。每张图片不超过 2 MB；其他格式先由用户选择的本地工具转换。外链先让用户保存为本地文件，不能自动抓取不可信网址。已有 `https://mmbiz.qpic.cn/` 图片可直接保留。

封面在私有配置指定 `coverPath`（相对配置文件目录或绝对路径），或使用同一公众号的永久素材 `thumbMediaId`。指定 coverPath 时每次会上传封面；经常使用同一封面时填写已有 thumbMediaId 来避免重复上传。Skill 不维护作者的账号、缓存或封面。

官方接口参考：[新增草稿](https://developers.weixin.qq.com/doc/offiaccount/Draft_Box/Add_draft.html)。不得调用群发或正式发布接口。
