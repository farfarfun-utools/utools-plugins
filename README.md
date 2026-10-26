# utools-plugins

[farfarfun-utools](https://github.com/farfarfun-utools) 组织下所有 uTools 插件的统一索引。
列出每个插件解决什么问题、在 uTools 里怎么唤起、数据存在哪里，帮你在动手装之前先挑对插件，
再跳转到对应仓库看详细说明。

插件的实现和维护仍在各自的源仓库里，本仓库**不复制代码、不做构建**，只维护索引表与共同约定，
避免每次新增 / 调整插件时要在多处仓库间手工同步文档。

## 索引表

| 插件 | 解决什么问题 | uTools 里怎么唤起 | 数据在哪 |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/funchat-64.png" alt="" width="40"> [utools-funchat](https://github.com/farfarfun-utools/utools-funchat) | **[言来语往](https://farfarfun.github.io/packages/utools-funchat/)**：和多个不同人设的 AI 角色聊天，角色可从内置市场挑，话题可回溯、可一键导出 | 输入 `言来语往` / `AI` / `funchat` / `Funchat` / `聊天助手`，或选中文字使用「问 AI 好友」 | 本机 `dbStorage`；对话直接发往你自己配置的大模型服务商 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/fundoc-64.png" alt="" width="40"> [utools-fundoc](https://github.com/farfarfun-utools/utools-fundoc) | **[落笔成章](https://farfarfun.github.io/packages/utools-fundoc/)**：本地管理 Markdown 文档，支持 LaTeX 公式、多级目录与跨设备同步 | 输入 `落笔成章` / `FunDoc` / `文档` / `笔记`，可搜索或导入文档 | 本机 `dbStorage`；可选跨设备同步 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/funlink-64.png" alt="" width="40"> [utools-funlink](https://github.com/farfarfun-utools/utools-funlink) | **[一链即达](https://farfarfun.github.io/packages/utools-funlink/)**：把零散书签整理成网址导航：二级分类、拖拽排序、收集箱、废纸篓（可恢复） | 输入 `一链即达` 打开；主输入框搜索网址后回车直接打开，支持指定浏览器 | 本机 `dbStorage`，不上传 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/funotp-64.png" alt="" width="40"> [utools-funotp](https://github.com/farfarfun-utools/utools-funotp) | **[密钥随行](https://farfarfun.github.io/packages/utools-funotp/)**：替代手机上的验证器 App：本地离线生成 TOTP / HOTP 动态码，兼容 Google Authenticator | 输入 `密钥随行` 打开；主输入框搜账号名回车即复制验证码，常用账号可注册独立关键字 | 本机 `dbStorage`；可选 WebDav 备份（需手动配置） |
| <img src="https://raw.githubusercontent.com/farfarfun-utools/utools-funcalendar/master/utools/logo.png" alt="" width="40"> [utools-funcalendar](https://github.com/farfarfun-utools/utools-funcalendar) | **[时光常伴](https://farfarfun.github.io/packages/utools-funcalendar/)**：离线查看阳历、农历、节气与每日宜忌，按嫁娶、搬家、开市等事项查询吉日 | 输入 `时光常伴` / `FunCalendar` / `日历` / `黄历`；输入 `吉日` 进入筛选；插件内主输入框输入日期跳转 | 历法与宜忌数据随插件打包；仅在本机 `localStorage` 保存主题偏好，不联网 |
| <img src="https://raw.githubusercontent.com/farfarfun-utools/utools-funqr/master/utools/logo.png" alt="" width="40"> [utools-funqr](https://github.com/farfarfun-utools/utools-funqr) | **[码上生花](https://farfarfun.github.io/packages/utools-funqr/)**：文本与二维码互转，自定义配色、渐变、码点和中心 Logo，导出 PNG / SVG | 输入 `码上生花` / `FunQR` / `二维码`；输入 `扫码` 识别图片；选中文字使用「生成二维码」 | 完全离线，图片和内容仅在当前会话处理；仅保存主题偏好 |
| <img src="https://raw.githubusercontent.com/farfarfun-utools/utools-funcalc/master/utools/logo.png" alt="" width="40"> [utools-funcalc](https://github.com/farfarfun-utools/utools-funcalc) | **FunCalc**：支持变量、矩阵和 LaTeX 排版的计算笔记本，历史可搜索、复制与复用 | 输入 `FunCalc` / `计算笔记` / `历史计算器` / `矩阵计算`；选中文字后选择计算表达式 | 本机 IndexedDB；历史和变量一起持久化，不联网、不自动清理 |

## 怎么挑

- 想**少开一个窗口聊 AI** → `utools-funchat`（言来语往）
- 想在 uTools 中管理 Markdown 文档 → `utools-fundoc`（落笔成章）
- 常用网址 / 文档入口**记不住又懒得翻书签** → `utools-funlink`（一链即达）
- **手机验证器拿来拿去太麻烦**，想在电脑上复制验证码 → `utools-funotp`（密钥随行）
- 想**同时看阳历、农历、节气，按事情查吉日** → `utools-funcalendar`（时光常伴；黄历仅作民俗参考）
- 想**把文字变成好看的二维码，或识别图片里的二维码** → `utools-funqr`（码上生花）
- 想**保留计算过程，复用变量并计算矩阵** → `utools-funcalc`（FunCalc）

这些插件互不依赖，可以只装其中任意一个。

## 共同约定

- **本地优先**：按需使用本地存储或 uTools 的 `dbStorage`，不需要注册账号、不需要自建服务端。时光常伴与码上生花完全离线；其他插件的模型请求、同步和备份方式见各自 README。
- **主搜索框集成**：核心操作都能在 uTools 主输入框里完成，不必先进插件界面再找功能。
- **统一技术栈**：Vue 3 + Composition API + Vite，插件根目录统一是 `utools/`（`plugin.json`、图标、构建产物，按需包含 `preload.js`）。
- **统一构建入口**：每个仓库都有 `sh build.sh`，执行各插件的测试、类型检查和构建校验，任一步失败即中止。

## 安装（通用步骤）

```bash
git clone https://github.com/farfarfun-utools/<plugin>.git
cd <plugin>
pnpm install
sh build.sh
```

然后在 uTools 里打开「插件应用市场 → 开发者工具 → 新建项目」，载入 `utools/plugin.json`。

Node.js 版本以各仓库 `package.json#engines` 为准（时光常伴、码上生花要求 ≥ 22.22.2），
pnpm 版本跟着 `package.json#packageManager` 走。各插件的配置项、快捷键和备份方式见自己仓库的 README。

## 新增 / 调整插件时

在源仓库完成插件的新增、删除或职责调整后，回到这里同步更新上面索引表的一行，
并同步 [`.github/profile/README.md`](https://github.com/farfarfun-utools/.github/blob/master/profile/README.md)
的「插件总览」表，保持这两处是插件一览的唯一入口。

---

## 关于 farfarfun-utools

[farfarfun](https://github.com/farfarfun) 的 uTools 插件产品线：本地优先、集成 uTools
主搜索框、统一 Vue 3 + Vite 技术栈。

- 🏠 组织主页：<https://github.com/farfarfun-utools>
- 📧 联系：farfarfun@qq.com

本项目基于 [MIT](LICENSE) 协议开源。
