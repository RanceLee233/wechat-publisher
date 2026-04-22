# WeChat Publisher

> **Write in Obsidian, publish to WeChat Official Account (微信公众号).**
>
> WeChat Publisher renders your Markdown notes into WeChat-compatible HTML with proper formatting — code highlighting, math formulas, Mermaid diagrams, local image upload, and one-click draft push to your Official Account. **Free for personal use**, please don't use it for commercial purposes.
>
> 👇 中文文档见下方

---

**在 Obsidian 里写作，一键发布到微信公众号。**

WeChat Publisher 是一个 Obsidian 插件，让你在熟悉的写作环境里完成公众号排版，无需离开 Obsidian 就能发布。

**个人使用完全免费**，全部能力直接解锁，无需激活码。

**[⬇️ 下载最新版本](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher-latest.zip)**（v0.1.14，国内直连）　｜　[GitHub Releases](https://github.com/RanceLee233/wechat-publisher/releases)（历史版本）

---

## 简介

很多人用 Obsidian 写公众号文章，但发布时总绕不开一个麻烦：Markdown 渲染后的样式在微信编辑器里根本不对，代码块、标题、图片全乱，还要手动重排。

WeChat Publisher 解决的就是这个问题。它在 Obsidian 侧边栏直接预览微信排版效果，支持：

- **格式预览 + 复制 HTML**：一键跳转公众号后台粘贴，全程不需要填写任何账号信息
- **直连公众号 API**：配置 AppID/AppSecret 后，直接从 Obsidian 推送到草稿箱，无需打开浏览器

**支持的 Markdown 格式：**

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

全部能力对个人用户免费开放：

| 功能 | 说明 |
|------|------|
| 格式预览 | Markdown → 微信排版，所见即所发 |
| 复制 HTML | 一键粘贴到公众号编辑器 |
| 跳转公众号平台 | 一键打开 mp.weixin.qq.com |
| 账号配置 · 直连公众号 API | 填入 AppID/AppSecret 后直连 |
| 发布到草稿箱 | 无需打开浏览器，一键推送 |
| 封面系统 | 自动设置封面，支持账号默认封面 |
| 多账号切换 | 同时管理多个公众号 |

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

## 使用条款

**v0.1.13 起，WeChat Publisher 对个人用户完全免费，无需激活码。** 全部能力（格式预览、复制 HTML、发布草稿、多账号、封面系统等）直接解锁。

- 本插件对个人用户完全免费
- 请勿用于商业用途（包括转售、商用培训、二次分发收费等）
- 如在公司/商业团队使用，请先通过公众号「HelloRanceLee」联系作者获取授权

如果插件对你有帮助，欢迎关注公众号 **HelloRanceLee**，同步更新 Obsidian 教程、写作技巧与这个插件的最新动态。

---

## 安装

### 方式一：BRAT（推荐，可自动更新）

BRAT 是 Obsidian 官方市场中的一个插件管理工具，可以直接从 GitHub 安装未上架的插件，并自动管理更新。

**第一步：安装 BRAT**

在 Obsidian「设置」→「第三方插件」→「浏览」中搜索 **BRAT**，安装并启用。

![BRAT 安装](https://cf-img.discoverlabs.ac.cn/202603272fe616a63272ecc499e14c731934ac9f.webp)

**第二步：添加 WeChat Publisher**

打开「设置」→「BRAT」→ 点击 **Add Beta plugin**，输入：

```
RanceLee233/wechat-publisher
```

点击 **Add Plugin**，选择 Latest version，BRAT 会自动下载安装最新版本。

![BRAT 添加插件](https://cf-img.discoverlabs.ac.cn/2026032713d6d729fcf1e57760c4cbf371763d3c.webp)

![BRAT 选择版本](https://cf-img.discoverlabs.ac.cn/20260327470a731d145a98e625b8ed39b6ecb971.webp)

**第三步：启用插件**

回到「设置」→「第三方插件」，找到 **WeChat Publisher**，开启开关启用。

> 国内用户如无法访问 GitHub，请使用下方手动安装方式。

### 方式二：手动安装

**第一步：下载插件**

前往 [博客下载页](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher/) 下载最新版本 zip。

**第二步：解压到插件目录**

将 zip 解压后，把文件夹复制到 Obsidian 插件目录：

```
你的仓库路径/.obsidian/plugins/wechat-publisher/
```

完成后目录结构应为：

```
.obsidian/
  plugins/
    wechat-publisher/
      main.js
      manifest.json
      styles.css
```

![手动安装目录结构](https://cf-img.discoverlabs.ac.cn/20260327e50f0cd87e0dff2b55587f5e26f287f4.webp)

**第三步：启用插件**

在「设置」→「第三方插件」中找到 **WeChat Publisher**，点击右侧开关启用。

![启用插件](https://cf-img.discoverlabs.ac.cn/20260327e97ca2137887b2088bd22fd595206657.webp)

---

## 使用

### 打开插件

启用后，点击 Obsidian 左侧边栏的 **WeChat Publisher 图标**，或按 `Cmd/Ctrl+P` 搜索 `WeChat Publisher` 打开预览面板。

![插件界面](https://cf-img.discoverlabs.ac.cn/20260327265d84010f9ccf2a4d288d9ac8f2dccc.webp)

v0.1.11 起，界面改为**单行工具栏 + 可展开抽屉**的设计，和 Obsidian 原生风格一致。工具栏从左到右依次为：

| 区域 | 说明 |
|------|------|
| **元信息卡** | 封面缩略 + 标题 + 「作者 · 封面状态 · 点击编辑 →」，点击展开抽屉编辑本次发布的标题/作者/封面 |
| **账号胶囊** | 当前账号名 + 状态圆点（绿=已就绪 / 橙=未填写 AppID/AppSecret / 灰=未配置）；点击切换账号 |
| **主题/排版胶囊** | 显示当前主题（如「湖水青」），点击弹出主题/排版速切面板 |
| **🔄 刷新渲染** · **📋 复制 HTML** | 工具图标，悬停显示完整名称 |
| **发布草稿** | 主按钮，一键发布到公众号草稿箱 |
| **⋯ 更多** | 去公众号粘贴、滚动同步、隐藏工具栏、账号配置、用户指南、关于 / 联系作者 |

**隐藏工具栏** → 顶部出现「⌄ 显示工具栏」吊签，预览区扩展到全屏。

### 格式与主题

点击工具栏的**主题/排版胶囊**，弹出速切面板：

- **上半：主题风格** —— 13 个内置主题（经典蓝、石墨灰、枫糖棕、薄荷绿、朝阳橙、湖水青、报刊风、森林绿，v0.1.11 新增：极简白 / 编辑部 / 墨卡 / 暖栗色 / 技术流），附简短描述，点击即切换
- **下半：排版模板** —— 均衡版 / 紧凑版 / 舒展版 / 专栏版，控制字号、行距和留白节奏
- **底部：高级微调 / 我的方案…** —— 打开弹窗做细粒度调整（h1~h4 样式、callout、代码块主题等）或套用保存过的方案

**一键切换**即刻刷新预览，不会遮挡文章内容。

### 刷新渲染

插件会在你切换笔记时自动重新渲染预览。如果感觉预览没有及时更新，可点击**刷新渲染**按钮手动触发。

### 双向滚动同步

打开工具栏的 **⋯ 菜单**，点击「滚动同步」进入同步模式（菜单项右侧显示当前状态：已关闭 / 请先滚动编辑器校准 / 已开启）。

**使用步骤：**

1. 点击「滚动同步」开启，状态变为"请先滚动编辑器校准"
2. 在左侧**编辑器中滚动一次**，状态变为"已开启"表示校准完成
3. 之后滚动任意一侧，另一侧自动跟随

同步优先按**标题段落对齐**，没有标题时按全文比例降级。再次点击「滚动同步」即可关闭。

### 复制 HTML

点击顶部的**复制 HTML** 按钮，插件会将当前预览区的渲染结果复制为微信兼容的 HTML。

复制完成后，打开微信公众号后台编辑器，在正文区域直接粘贴即可。适合不需要直连 API、手动上传文章的场景。

### 去公众号粘贴

点击**去公众号粘贴**，浏览器会自动打开微信公众号后台 `mp.weixin.qq.com`，方便你在复制 HTML 后切换到后台粘贴。

### 账号配置

若要一键把文章推送到公众号草稿箱，需要先完成**账号配置**（填写公众号的 AppID / AppSecret）。

点击顶部操作栏中的**账号配置**按钮，打开配置弹窗。弹窗顶部以标签页（Tab）形式列出所有已添加的账号，点击标签可切换。

弹窗中各字段说明如下：

| 字段 | 说明 |
|------|------|
| **账号名称** | 自定义名称，方便区分多个公众号，例如：主号 / 备用号 |
| **AppID** | 微信公众号的 AppID，在微信公众平台「基础信息」页获取 |
| **AppSecret** | 微信公众号的开发密钥，需在微信公众平台手动启用 |
| **IP 白名单辅助** | 插件自动检测你当前的公网 IP，点击「复制」后去微信平台填入白名单 |
| **默认作者** | 可选。发布资料区没有填写作者时，自动使用此处的名字 |
| **默认封面** | 可选。为该账号设置一张固定封面，每次发文章时自动使用 |
| **设为默认账号** | 开启后，打开插件时自动选中该账号 |

底部有两个按钮：**手动新增账号**（填表手动添加）和**快速粘贴新建账号**（一键从微信公众平台复制内容自动识别）。填写完成后点**保存**。

> 账号信息仅保存在本地 Obsidian 配置文件中，不会上传到任何服务器。

#### 快速粘贴新建账号

嫌填表麻烦？有更快的方式：打开微信公众平台「基础信息」页，全选页面内容复制，然后在 WeChat Publisher 账号配置弹窗里点「快速粘贴新建账号」，把内容粘贴进去，插件自动识别账号名、AppID 和 AppSecret，一键完成添加。

![快速粘贴新建账号](https://cf-img.discoverlabs.ac.cn/202603281f45c5665594bf984cf5dccce8e9755e.webp)

复制后的内容格式大致如下：

```
公众号
你的公众号名称
AppID
wx_your_appid_here
AppSecret
your_appsecret_here
```

#### 如何获取 AppID 和 AppSecret

**第一步：** 打开微信开发者平台 `developers.weixin.qq.com`，点击**前往控制台**。

![前往控制台](https://cf-img.discoverlabs.ac.cn/20260327338a1f10db1b76c8dfb8661961a2b5ac.webp)

**第二步：** 在「我的业务」页面找到你的**公众号**并点击进入。

![找到公众号](https://cf-img.discoverlabs.ac.cn/202603279344ceddd894874ea59b66cf38eca2d4.webp)

**第三步：** 进入公众号管理后台，在**基础信息**页面找到 **AppID**（直接复制）以及**开发密钥**区域。点击 AppSecret 旁的**启用**，扫码授权后即可获取 AppSecret。

![基础信息页](https://cf-img.discoverlabs.ac.cn/20260327b8996df79a73ea68add38c2e8b883605.webp)

![获取 AppSecret](https://cf-img.discoverlabs.ac.cn/2026032735d0fa9e2d6b2daf2e3af6b1de8d16f3.webp)

> AppSecret 只会在启用时完整显示一次，请立即复制保存。

#### 如何配置 IP 白名单

微信公众号 API 要求调用接口的服务器 IP 在白名单内。由于 WeChat Publisher 从你的电脑直接调用 API，需要将你的电脑公网 IP 加入白名单。

**操作步骤：**

1. 在插件的账号配置弹窗中，点击**检测本机 IP**，插件自动获取你的当前公网 IP
2. 点击**复制**，复制该 IP 地址
3. 前往微信公众平台「基础信息」页，点击「API IP 白名单」旁的**设置名单**
4. 将复制的 IP 粘贴进去，多个 IP 用回车隔开，点击**确定**

> 如果你在家和公司都会用，两个网络的公网 IP 不同，都要加进去。

### 发布草稿

完成账号配置后，点击**发布草稿**。插件自动：
1. 将本地图片上传到微信 CDN
2. 处理 Mermaid 图表、数学公式等为图片
3. 将渲染后的 HTML 连同标题、作者、封面提交到草稿箱

> 草稿不会直接群发，需在公众号后台手动操作群发。
>
> **重复发布会自动更新，不会产生重复文章**：如果这篇笔记之前已经发布过草稿，修改后再次点「发布草稿」，插件会自动找到公众号平台上已有的那篇草稿并更新它，不会新建多余的重复文章。

### 封面系统

![封面设置](https://cf-img.discoverlabs.ac.cn/20260327c9d6037db80885c6f2fe738fc425bb77.webp)

| 按钮 | 说明 |
|------|------|
| 从电脑选择封面 | 从本地选一张图片作为本次文章的封面 |
| 清空封面 | 发布时使用占位空白封面 |
| 默认封面 | 使用账号配置中设定的默认封面 |

**封面优先级**：手动选择 > 账号默认封面 > 占位封面。建议尺寸：900×383 px，支持 JPG / PNG。

---

## 隐私

- **不收集任何用户数据**：插件完全本地运行，无后台服务器
- **API 凭证本地存储**：AppSecret 仅存储在本地，不上传至任何服务器
- **图片上传**：图片直接上传至微信官方 CDN，不经过第三方服务器
- **开源审计**：插件代码开源，可自行审计

---

## License

[MIT](LICENSE)
