# WeChat Publisher

> 在 Obsidian 里写作，一键发布到微信公众号。

WeChat Publisher 是一个 Obsidian 插件，让你无需离开 Obsidian 就能完成公众号排版和发布。

## 功能

**免费功能**
- 🎨 格式预览：Markdown 实时渲染为微信样式，所见即所发
- 📋 复制 HTML：一键复制渲染结果，粘贴到公众号编辑器
- 🔗 跳转公众号平台：快速打开微信公众号后台

**付费功能**
- 🚀 发布到草稿箱：直接推送到公众号，无需打开浏览器
- ⚙️ 账号配置：直连公众号 API，支持多账号管理
- 🖼 封面系统：自动设置封面，支持默认封面

**支持的格式**

| 格式 | 说明 |
|------|------|
| 代码块 | 语法高亮，保留缩进与空格 |
| 数学公式 | `$...$` 行内 / `$$...$$` 块级，渲染为图片 |
| Mermaid 图表 | 流程图、时序图等，渲染为图片 |
| 表格 | 完整样式还原 |
| 图片 | 本地 + 远程图片，自动上传微信 CDN |
| Ruby 注音 | `{文字\|注音}` 语法 |
| 警示块 | `> [!NOTE]` / `[!WARNING]` 等 |
| 横向滑图 | 多图并排轮播 |

## 安装

### 方式一：BRAT（推荐）

1. 在 Obsidian 社区插件中安装 [BRAT](https://github.com/TfTHacker/obsidian42-brat)
2. 打开「设置」→「BRAT」→ **Add Beta plugin**
3. 输入：`RanceLee233/wechat-publisher`，点击 **Add Plugin**

> 国内用户如无法访问 GitHub，请使用下方手动安装方式。

### 方式二：手动安装

1. 前往 [博客下载页](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher/) 下载最新版本（国内直连）
   或在 [GitHub Releases](https://github.com/RanceLee233/wechat-publisher/releases) 下载历史版本
2. 解压后将文件夹放入：`.obsidian/plugins/wechat-publisher/`
3. 在「设置」→「第三方插件」中启用 **WeChat Publisher**

## 使用文档

→ [完整用户指南](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher/)

## 价格

插件采用买断制，免费版可使用格式预览和复制 HTML，付费版解锁发布、账号配置和封面系统。

详情见 [产品页](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher/#价格)。

## 隐私

- 所有数据本地存储，不收集任何用户信息
- 微信 AppID / AppSecret 仅保存在本地 Obsidian 配置中
- 激活码验证仅传输激活码本身，不含个人信息
- 图片直接上传至微信官方 CDN，不经过第三方服务器

## License

[MIT](LICENSE)
