# utools-plugins

[farfarfun-utools](https://github.com/farfarfun-utools) 组织下所有 uTools 插件的统一索引。
列出每个插件解决什么问题、在 uTools 里怎么唤起、数据存在哪里，帮你在动手装之前先挑对插件，
再跳转到对应仓库看详细说明。

插件的实现和维护仍在各自的源仓库里，本仓库**不复制代码、不做构建**，只维护索引表与共同约定，
避免每次新增 / 调整插件时要在多处仓库间手工同步文档。

## 索引表

| 插件 | 解决什么问题 | uTools 里怎么唤起 | 数据在哪 |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funchat-64.png" alt="" width="40"> [utools-funchat](https://github.com/farfarfun-utools/utools-funchat) | **[言来语往](https://farfarfun.github.io/packages/utools-funchat/)**：和多个不同人设的 AI 角色聊天、生成图片；角色可从内置市场挑，话题可回溯、可一键导出 | 输入 `言来语往` / `AI` / `funchat` / `Funchat` / `聊天助手`，或选中文字使用「问 AI 好友」 | uTools 数据库，可选同步；请求直接发往所选 AI 服务商 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/fundoc-64.png" alt="" width="40"> [utools-fundoc](https://github.com/farfarfun-utools/utools-fundoc) | **[落笔成章](https://farfarfun.github.io/packages/utools-fundoc/)**：本地管理 Markdown 文档，支持 LaTeX 公式、多级目录与跨设备同步 | 输入 `落笔成章` / `FunDoc` / `文档` / `笔记`，可搜索或导入文档 | 正文和附件存放在 uTools 文档数据库，开启同步后可跨设备访问 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funlink-64.png" alt="" width="40"> [utools-funlink](https://github.com/farfarfun-utools/utools-funlink) | **[一链即达](https://farfarfun.github.io/packages/utools-funlink/)**：把零散书签整理成网址导航：二级分类、拖拽排序、收集箱、废纸篓（可恢复） | 输入 `一链即达` 打开；主输入框搜索网址后回车直接打开，支持指定浏览器 | uTools 数据库，可随账号同步；支持手动 WebDAV 备份 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funotp-64.png" alt="" width="40"> [utools-funotp](https://github.com/farfarfun-utools/utools-funotp) | **[密钥随行](https://farfarfun.github.io/packages/utools-funotp/)**：替代手机上的验证器 App：本地离线生成 TOTP / HOTP 动态码，兼容 Google Authenticator | 输入 `密钥随行` 打开；主输入框搜账号名回车即复制验证码，常用账号可注册独立关键字 | 明文密钥保存在 uTools 数据库，开启同步后可随账号同步；支持手动 WebDAV 明文备份 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funcalendar-64.png" alt="" width="40"> [utools-funcalendar](https://github.com/farfarfun-utools/utools-funcalendar) | **[时光常伴](https://farfarfun.github.io/packages/utools-funcalendar/)**：离线查看阳历、农历、节气与每日宜忌，按嫁娶、搬家、开市等事项查询吉日 | 输入 `时光常伴` / `FunCalendar` / `日历` / `黄历`；输入 `吉日` 进入筛选；插件内主输入框输入日期跳转 | 历法与宜忌数据随插件打包；仅在本机 `localStorage` 保存主题偏好，不联网 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funqr-64.png" alt="" width="40"> [utools-funqr](https://github.com/farfarfun-utools/utools-funqr) | **[码上生花](https://farfarfun.github.io/packages/utools-funqr/)**：文本与二维码互转，自定义配色、渐变、码点和中心 Logo，导出 PNG / SVG | 输入 `码上生花` / `FunQR` / `二维码`；输入 `扫码` 识别图片；选中文字使用「生成二维码」 | 完全离线，图片和内容仅在当前会话处理；仅保存主题偏好 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funcalc-64.png" alt="" width="40"> [utools-funcalc](https://github.com/farfarfun-utools/utools-funcalc) | **[算有所得](https://farfarfun.github.io/packages/utools-funcalc/)**：支持变量、矩阵和 LaTeX 排版的计算笔记本，历史可搜索、复制与复用 | 主输入框输入数字算式直接查看并复制结果；输入 `算有所得` / `FunCalc` / `计算笔记` / `历史计算器` / `矩阵计算` 打开；也可选中文字后计算 | 本机 IndexedDB；历史和变量一起持久化，重复结果合并，不联网 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funvideo-64.png" alt="" width="40"> [utools-funvideo](https://github.com/farfarfun-utools/utools-funvideo) | **[视频工坊](https://farfarfun.github.io/packages/utools-funvideo/)**：批量压缩、裁剪、转换、抽帧及处理音频，可将多个时间点的画面拼成一张 JPG | 输入 `视频工坊` / `FunVideo` / `批量视频`；也可选中视频文件后进入 | 视频仅在本机处理，不保存历史；处理结果保存到独立批次目录 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/b0915330bb901208953c4027a545c16c9654f4a9/brand/png/mark/funimage-64.png" alt="" width="40"> [utools-funimage](https://github.com/farfarfun-utools/utools-funimage) | **[图片工坊](https://farfarfun.github.io/packages/utools-funimage/)**：批量压缩、编辑、加水印，可调整队列顺序后拼图或合并为 PDF、GIF | 输入 `图片工坊` / `FunImage` / `图片压缩`；也可选中图片文件后进入 | 图片仅在本机处理，不保存历史；结果另存新文件 |
| <img src="https://raw.githubusercontent.com/farfarfun/farfarfun-web/34c5b1a3e2d830db964be200701c6494addbdd91/brand/png/mark/funjson-64.png" alt="" width="40"> [utools-funjson](https://github.com/farfarfun-utools/utools-funjson) | **[JSON工坊](https://farfarfun.github.io/packages/utools-funjson/)**：离线 JSON 五视图工作台，支持编辑/树形/多级递归嵌套表格/栏列/语义差异对比、JSONPath 查询、智能修复、9 语言类型生成与键名转换 | 输入 `JSON工坊` / `FunJSON` / `json` / `JSON格式化` / `JSONPath`；支持正则识别 JSON、打开 JSON 文件或选中文本解析 | 完全离线，多标签页、历史快照与偏好保存在本机（仅在手动触发外部 AI 修复时请求所选服务商） |
| <img src="https://raw.githubusercontent.com/farfarfun/farfarfun-web/34c5b1a3e2d830db964be200701c6494addbdd91/brand/png/mark/fundata-64.png" alt="" width="40"> [utools-fundata](https://github.com/farfarfun-utools/utools-fundata) | **[数形万变](https://farfarfun.github.io/packages/utools-fundata/)**：离线 10 合 1 开发者数据工具箱，支持 10 格式万能互转、编解码与多时区时间戳、JWT 解析/验签/签发、Protobuf 重编号、SQL 美化、哈希/HMAC & UUID、正则实验室、Cron 推算、色值/进制/字节换算与文本批处理对比 | 输入 `数形万变` / `FunData` / `数据转换` / `yaml` / `jwt` / `sql` / `cron` / `regex` / `hash` / `uuid`（按工具拆分为多组入口）；也支持打开数据文件或选中文本自动路由 | 完全离线，所有运算、签名、哈希与解析均在本机完成；仅在本机保存主题/语言偏好 |

各插件还提供按职责划分的 AI 工具，例如计算、日历查询、二维码识别、文档搜索与新建，以及书签管理。工具列表与可返回的数据见各插件 README；第三方 Agent 需由用户开启 uTools MCP 服务。

## 怎么挑

- 想**少开一个窗口聊 AI** → `utools-funchat`（言来语往）
- 想在 uTools 中管理 Markdown 文档 → `utools-fundoc`（落笔成章）
- 常用网址 / 文档入口**记不住又懒得翻书签** → `utools-funlink`（一链即达）
- **手机验证器拿来拿去太麻烦**，想在电脑上复制验证码 → `utools-funotp`（密钥随行）
- 想**同时看阳历、农历、节气，按事情查吉日** → `utools-funcalendar`（时光常伴；黄历仅作民俗参考）
- 想**把文字变成好看的二维码，或识别图片里的二维码** → `utools-funqr`（码上生花）
- 想**保留计算过程，复用变量并计算矩阵** → `utools-funcalc`（算有所得）
- 想批量加工本地视频 → `utools-funvideo`（视频工坊）
- 想批量编辑、预览或拼接图片 → `utools-funimage`（图片工坊）
- 想**深度查看、编辑、嵌套表格浏览、JSONPath 查询、语义对比 JSON，或生成多语言类型** → `utools-funjson`（JSON工坊）
- 想**做多格式互转（YAML/TOML/XML/CSV）、编解码与时间戳、JWT 验签签发、Protobuf/SQL 美化、哈希/UUID、正则测试、Cron 推算或色值/进制/文本批处理** → `utools-fundata`（数形万变）

这些插件互不依赖，可以只装其中任意一个。

## 共同约定

- **本地优先**：按需使用本地存储或 uTools 的 `dbStorage`，不需要注册账号、不需要自建服务端。时光常伴与码上生花完全离线；其他插件的模型请求、同步和备份方式见各自 README。
- **主搜索框集成**：核心操作都能在 uTools 主输入框里完成，不必先进插件界面再找功能。
- **实现方式**：各插件使用 Vite 构建前端，按功能选用 Vue 3/TypeScript 或原生 JavaScript；插件运行目录统一是 `utools/`。
- **构建与验证**：仓库根目录的 `sh build.sh` 是统一入口，产物写入 `utools/dist/`；CI 与 Release 都调用它。

## 安装（通用步骤）

从各插件的 GitHub Release 下载 `.upxs` 导入 uTools；开发版先运行 `sh build.sh`，再按对应仓库的 README 在开发者工具中载入 `utools/plugin.json`。各插件的配置项、快捷键和备份方式也见各自 README。

## 新增 / 调整插件时

在源仓库完成插件的新增、删除或职责调整后，回到这里同步更新上面索引表的一行，
并同步 [`.github/profile/README.md`](https://github.com/farfarfun-utools/.github/blob/master/profile/README.md)
的「插件总览」表，保持这两处是插件一览的唯一入口。

---

## 关于 farfarfun-utools

[farfarfun](https://github.com/farfarfun) 的 uTools 插件产品线：本地优先、集成 uTools 主搜索框。

- 🏠 组织主页：<https://github.com/farfarfun-utools>
- 📧 联系：farfarfun@qq.com

本项目基于 [MIT](LICENSE) 协议开源。
