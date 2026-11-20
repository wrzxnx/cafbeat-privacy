# 图格 / Slidecut 法律页面

正式版本：隐私政策与使用条款，支持简体中文、英文、繁体中文、日文、韩文、泰文、土耳其文、越南文。

开发者：wangrui。联系邮箱：wrzxnx@gmail.com。

## 已确认的应用行为

- 所有照片与生成图片完全在设备本地处理，绝不上传至开发者或第三方服务器，也不进入 Firebase、友盟或 AdMob 报告。
- Firebase、友盟用于设备标识统计和崩溃诊断。诊断上下文可能包含设备型号、系统及应用版本、时间和调用堆栈；联网也可能形成技术连接日志。
- 广告使用 Google AdMob；按 SDK 设置、权限和同意状态，可能处理广告相关标识符、网络、展示互动与诊断信息。
- Premium 条款按一次性买断编写，保留有效历史购买权益。
- 数据保存按必要目的、服务商设置和公开政策描述，未虚构固定期限或未经确认的处理国家。

## 线上目录

代码托管在 `wrzxnx/cafbeat-privacy` 仓库，图格静态页面位于 `slidecut/`，源码位于 `slidecut-source/`。使用现有从 main 分支发布的 GitHub Pages，新增文件即可触发发布。

公共入口：`slidecut/privacy.html`、`slidecut/terms.html`。可使用 `?lang=zh-Hans` 指定语言。无参数时按浏览器语言选择，未匹配时使用英文。

| 语言 | 隐私政策 | 使用条款 |
| --- | --- | --- |
| 简体中文 | zh-Hans/privacy.html | zh-Hans/terms.html |
| English | en/privacy.html | en/terms.html |
| 繁體中文 | zh-Hant/privacy.html | zh-Hant/terms.html |
| 日本語 | ja/privacy.html | ja/terms.html |
| 한국어 | ko/privacy.html | ko/terms.html |
| ไทย | th/privacy.html | th/terms.html |
| Türkçe | tr/privacy.html | tr/terms.html |
| Tiếng Việt | vi/privacy.html | vi/terms.html |

表内路径均相对于 `slidecut/`。每种语言都提供完整静态 HTML，语言菜单无须 JavaScript。仅通用入口使用脚本识别语言，禁用脚本时仍可阅读英文正文。

## 后续维护

1. 修改 `content/*.json` 对应语言的正文，并在 `config.json` 中更新日期与实际 SDK 情况。
2. 执行 `python3 build.py --release` 和 `python3 check.py`。
3. 将生成的 `docs/` 内容同步到仓库的 `slidecut/`，源码同步到 `slidecut-source/`，提交 main。
4. 确认 Pages 构建与线上页面成功。

本项目不依赖第三方 Python 包。网页不加载统计、广告脚本或外部字体。请让 App Store Connect 隐私标签、SDK 实际设置和 App 内授权流程始终与政策保持一致。提供网页不会自动改变 App 的数据处理行为。

如以后迁移到独立仓库，可采用源码附带的 `.github/workflows/pages.yml`，并在新仓库 Pages 设置中选择 GitHub Actions。不要把嵌套的该文件移动到现有仓库的顶层，以免改变现有发布方式。
