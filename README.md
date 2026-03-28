# WeChat Publisher

**在 Obsidian 里写作，一键发布到微信公众号。**

WeChat Publisher 是一个 Obsidian 插件，让你在熟悉的写作环境里完成公众号排版，无需离开 Obsidian 就能发布。

**[⬇️ 下载最新版本](https://blog.discoverlabs.ac.cn/downloads/wechat-publisher-latest.zip)**（v0.1.6，国内直连）　｜　[GitHub Releases](https://github.com/RanceLee233/wechat-publisher/releases)（历史版本）

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

顶部操作栏从左到右：**格式** · **账号名称** · **账号配置** · **购买激活** · **用户指南** · **刷新渲染** · **复制HTML（免费）** · **去公众号粘贴（免费）** · **发布草稿（收费）**

### 格式与主题

点击**格式**展开样式控制栏，切换内置主题或进入**样式配置**精细调节字号、行距、颜色等。建议首次使用调好参数后保存为「已存样式」，之后每篇文章一键套用。

![样式配置](https://cf-img.discoverlabs.ac.cn/20260327cc923f87a73d4ce0f348f02a55134e60.webp)

### 账号配置（付费）

点击**账号配置**，弹窗顶部以标签页（Tab）形式列出所有已添加的账号，点击切换；右侧标有"已激活"/"未激活"状态。

| 字段 | 说明 |
|------|------|
| 账号名称 | 自定义名称，方便区分多个公众号 |
| AppID | 微信公众平台「基础信息」页获取 |
| AppSecret | 需在平台手动启用，只显示一次请立即保存 |
| 账号授权 | 显示激活状态（✅ 已绑定 / 未绑定），点击「刷新授权状态」重新验证 |
| IP 白名单辅助 | 插件自动检测公网 IP，复制后填入微信平台白名单 |
| 默认作者 / 默认封面 | 可选，发布时自动使用 |
| 设为默认账号 | 开启后，打开插件时自动选中该账号 |

**快速粘贴新建账号**：点击「快速粘贴新建账号」，将微信公众平台「基础信息」页全选复制的内容粘贴进来，插件自动识别账号名、AppID 和 AppSecret，一键完成添加。

![快速粘贴新建账号](https://cf-img.discoverlabs.ac.cn/202603281f45c5665594bf984cf5dccce8e9755e.webp)

**获取 AppID 和 AppSecret**：打开 `developers.weixin.qq.com` → 前往控制台 → 找到公众号 → 基础信息页。

**配置 IP 白名单**：点击「检测本机 IP」获取公网 IP，复制后填入微信公众平台「API IP 白名单」。

### 购买与激活（付费）

点击工具栏**购买激活**按钮，打开购买与激活弹窗。弹窗上半部分为购买二维码，下半部分为激活表单。

![购买激活弹窗](https://cf-img.discoverlabs.ac.cn/202603283639f1f52e9420c37e75f636b50efda5.webp)

1. 在账号列表中选择要绑定的公众号账号
2. 填入激活码（格式：`WCPR-XXXX-XXXX-XXXX-XXXX-XXXX-XXXX`）
3. 点击**绑定激活**，确认 AppID 无误后点确定
4. 绑定成功后，回到「账号配置」点击**刷新授权状态**，即可看到「✅ 已绑定」

> 1 个激活码绑定 1 个 AppID，不支持改绑。换电脑后点「刷新授权状态」即可恢复，无需重新输入。

### 发布草稿（付费）

完成账号配置和激活码绑定后，点击**发布草稿**。插件自动：
1. 将本地图片上传到微信 CDN
2. 处理 Mermaid 图表、数学公式等为图片
3. 将渲染后的 HTML 连同标题、作者、封面提交到草稿箱

> 草稿不会直接群发，需在公众号后台手动操作群发。
>
> **重复发布会自动更新，不会产生重复文章**：如果这篇笔记之前已经发布过草稿，修改后再次点「发布草稿」，插件会自动找到公众号平台上已有的那篇草稿并更新它，不会新建多余的重复文章。

### 封面系统（付费）

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
- **激活码验证**：激活时传输内容仅为激活码 + AppID，AppSecret 始终不离开本地
- **图片上传**：图片直接上传至微信官方 CDN，不经过第三方服务器
- **开源审计**：插件代码开源，可自行审计

---

## License

[MIT](LICENSE)
