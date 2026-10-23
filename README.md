# utools-plugins

[farfarfun-utools](https://github.com/farfarfun-utools) 组织下所有 uTools 插件的统一索引。
列出每个插件解决什么问题、在 uTools 里怎么唤起、数据存在哪里，帮你在动手装之前先挑对插件，
再跳转到对应仓库看详细说明。

插件的实现和维护仍在各自的源仓库里，本仓库**不复制代码、不做构建**，只维护索引表与共同约定，
避免每次新增 / 调整插件时要在多处仓库间手工同步文档。

## 索引表

| 插件 | 解决什么问题 | uTools 里怎么唤起 | 数据在哪 |
| --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/funchat-64.png" alt="" width="40"> [utools-funchat](https://github.com/farfarfun-utools/utools-funchat) | 和多个不同人设的 AI 角色聊天，角色可从内置市场挑，话题可回溯、可一键导出 | 主输入框关键字进入插件界面 | 本机 `dbStorage`；对话直接发往你自己配置的大模型服务商 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/fundoc-64.png" alt="" width="40"> [utools-fundoc](https://github.com/farfarfun-utools/utools-fundoc) | 本地管理 Markdown 文档，支持 LaTeX 公式、多级目录与跨设备同步 | 主输入框关键字进入插件界面，可搜索或导入文档 | 本机 `dbStorage`；可选跨设备同步 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/funlink-64.png" alt="" width="40"> [utools-funlink](https://github.com/farfarfun-utools/utools-funlink) | 把零散书签整理成网址导航：二级分类、拖拽排序、收集箱、废纸篓（可恢复） | 主输入框搜索网址后回车直接打开，支持指定浏览器 | 本机 `dbStorage`，不上传 |
| <img src="https://raw.githubusercontent.com/farfarfun/.github/master/brand/png/mark/funotp-64.png" alt="" width="40"> [utools-funotp](https://github.com/farfarfun-utools/utools-funotp) | 替代手机上的验证器 App：本地离线生成 TOTP / HOTP 动态码，兼容 Google Authenticator | 主输入框搜账号名回车即复制验证码，常用账号可注册独立关键字 | 本机 `dbStorage`；可选 WebDav 备份（需手动配置） |
| <img src="https://raw.githubusercontent.com/farfarfun-utools/utools-funcalendar/master/utools/logo.png" alt="" width="40"> [utools-funcalendar](https://github.com/farfarfun-utools/utools-funcalendar) | **时光常伴**：离线查看阳历、农历、节气与每日宜忌，按嫁娶、搬家、开市等事项查询吉日 | 输入 `时光常伴` / `日历` / `农历` / `黄历`；输入 `吉日` / `择吉` 进入筛选；插件内主输入框输入日期跳转 | 历法与宜忌数据随插件打包；仅在本机 `localStorage` 保存主题偏好，不联网 |

## 怎么挑

- 想**少开一个窗口聊 AI** → `utools-funchat`
- 想在 uTools 中管理 Markdown 文档 → `utools-fundoc`
- 常用网址 / 文档入口**记不住又懒得翻书签** → `utools-funlink`
- **手机验证器拿来拿去太麻烦**，想在电脑上复制验证码 → `utools-funotp`
- 想**同时看阳历、农历、节气，按事情查吉日** → `utools-funcalendar`（时光常伴；黄历仅作民俗参考）

五个插件互不依赖，可以只装其中任意一个。

## 共同约定

- **本地优先**：按需使用本地存储或 uTools 的 `dbStorage`，不需要注册账号、不需要自建服务端。时光常伴完全离线；其他插件的模型请求、同步和备份方式见各自 README。
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

Node.js 版本以各仓库 `package.json#engines` 为准（时光常伴要求 ≥ 22.22.2），
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
