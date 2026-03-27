# WeChat Publisher

**在 Obsidian 里写作，一键发布到微信公众号。**

WeChat Publisher 是一个 Obsidian 插件，让你在熟悉的写作环境里完成公众号排版，无需离开 Obsidian 就能发布。

**[⬇️ 下载最新版本](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher-latest.zip)**（v0.1.0，国内直连）　｜　[GitHub Releases](https://github.com/RanceLee233/wechat-publisher/releases)（历史版本）

---

## 效果预览

以下截图来自真实发布到微信的文章：

| 代码块语法高亮 | 数学公式渲染 |
|:-:|:-:|
| ![代码块](https://cf-img.discoverlabs.ac.cn/20260327c916de953070733331cab62712eec696.png) | ![数学公式](https://cf-img.discoverlabs.ac.cn/2026032704137d0f614862447b02215acd431f76.png) |

| Mermaid 图表 | Ruby 注音 |
|:-:|:-:|
| ![Mermaid](https://cf-img.discoverlabs.ac.cn/202603276eabb1622acc88e053be510f54377bc1.png) | ![Ruby注音](https://cf-img.discoverlabs.ac.cn/2026032794844a6524c92f22cf4ce34f8d1fccbe.png) |

---

## 功能

| 功能 | 免费版 | 付费版 |
|------|:------:|:------:|
| 格式预览（Markdown → 微信排版，所见即所发） | ✅ | ✅ |
| 复制 HTML（一键粘贴到公众号编辑器） | ✅ | ✅ |
| 跳转公众号平台 | ✅ | ✅ |
| 账号配置 · 直连公众号 API | ❌ | ✅ |
| 发布到草稿箱（无需打开浏览器） | ❌ | ✅ |
| 封面系统（自动设置封面，支持默认封面） | ❌ | ✅ |

**支持的 Markdown 格式**

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

---

## 价格

买断制，**¥28**，一次付费，终身使用（含后续更新）。

扫码加微信好友，备注「WeChat Publisher」，发送支付凭证即可获得激活码：

![微信二维码](https://cf-img.discoverlabs.ac.cn/2026032759a8f679ee666d68f7863edea53ce2e7.webp)

---

## 安装

### 方式一：BRAT（推荐，可自动更新）

1. 在 Obsidian 社区插件中安装并启用 **BRAT**
2. 打开「设置」→「BRAT」→ 点击 **Add Beta plugin**
3. 输入：`RanceLee233/wechat-publisher`，点击 **Add Plugin**

![BRAT 安装](https://cf-img.discoverlabs.ac.cn/202603272fe616a63272ecc499e14c731934ac9f.webp)

> 国内用户如无法访问 GitHub，请使用下方手动安装方式。

### 方式二：手动安装

1. 前往 [博客下载页](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher/) 下载最新版本 zip
2. 解压后将 `wechat-publisher` 文件夹放入：`.obsidian/plugins/wechat-publisher/`
3. 在「设置」→「第三方插件」中启用 **WeChat Publisher**

![手动安装](https://cf-img.discoverlabs.ac.cn/20260327e50f0cd87e0dff2b55587f5e26f287f4.webp)

---

## 使用

### 快速上手

打开任意 Markdown 文章 → 点击左侧边栏 **WeChat Publisher 图标**（或 `Cmd/Ctrl+P` 搜索）→ 预览实时渲染 → **复制 HTML** 或 **发布草稿**。

![插件界面](https://cf-img.discoverlabs.ac.cn/20260327265d84010f9ccf2a4d288d9ac8f2dccc.webp)

### 格式与主题

点击**格式**展开样式控制栏，切换内置主题或进入**样式配置**精细调节字号、行距、颜色等。建议首次使用调好参数后保存为「已存样式」，之后每篇文章一键套用。

![样式配置](https://cf-img.discoverlabs.ac.cn/20260327cc923f87a73d4ce0f348f02a55134e60.webp)

### 账号配置（付费）

点击**账号配置**，填写公众号 AppID 和 AppSecret。

![账号配置](https://cf-img.discoverlabs.ac.cn/2026032724e0825e42bccb6bc54e4d7a4ab2857b.webp)

| 字段 | 说明 |
|------|------|
| AppID | 微信开发者平台「基础信息」页获取 |
| AppSecret | 需在平台手动启用，只显示一次请立即保存 |
| IP 白名单辅助 | 插件自动检测公网 IP，复制后填入微信平台白名单 |
| 默认作者 / 默认封面 | 可选，发布时自动使用 |

**获取 AppID 和 AppSecret**：打开 `developers.weixin.qq.com` → 前往控制台 → 找到公众号 → 基础信息页。

![获取 AppID](https://cf-img.discoverlabs.ac.cn/20260327338a1f10db1b76c8dfb8661961a2b5ac.webp)

### 激活码绑定（付费）

在账号配置弹窗的「账号授权」区域填入激活码，确认 AppID 后点击**绑定当前公众号**。

![激活码绑定](https://cf-img.discoverlabs.ac.cn/20260327835f4c00ba78a5dfc50d3f1d048bef8d.webp)

> 1 个激活码绑定 1 个 AppID，不支持改绑。换电脑后点「刷新授权状态」即可恢复，无需重新输入。

### 发布草稿（付费）

点击**发布草稿**，插件自动上传图片、渲染公式/图表，推送到草稿箱。在公众号后台审阅后手动群发。

### 封面系统（付费）

![封面设置](https://cf-img.discoverlabs.ac.cn/20260327c9d6037db80885c6f2fe738fc425bb77.webp)

优先级：手动选择 > 账号默认封面 > 占位封面。建议尺寸：900×383 px，支持 JPG / PNG。

---

## 隐私

- 所有数据本地存储，不收集任何用户信息
- AppSecret 仅保存在本地，不上传至任何服务器
- 激活码绑定时仅传输：激活码 + AppID，AppSecret 始终不离开本地
- 图片直接上传至微信官方 CDN，不经过第三方服务器

---

## License

[MIT](LICENSE)
