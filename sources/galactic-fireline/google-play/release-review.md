# Google Play 隐私政策发布核对

状态：本地审核稿；尚未推送或上线。编写日期：2026-10-28。

## 编写依据

- 公司名称、地址取自 `sources/poker-swap-puzzle/google-play/privacy.md`；联系邮箱使用用户本次生成稿中的 `contact@panchenglabs.com`，替换早期草稿的 Gmail。
- 用户已手动操作生成器并提供本游戏生成稿，逐字保存在 `privacy.generator.md`（仅内部参考，不放入 docs 发布）。正式稿结合该生成稿、已核对的游戏功能和 SDK 披露修订。
- 游戏名同时使用 Galactic Fireline / 银河火线，包名来自当前 Android 导出配置。
- 检查当前游戏脚本：本地进度、局内存档及设置；AdMob 激励广告；未发现业务层 Firebase、注册登录、自建游戏后端或内购接入。
- Android 广告配置中 AdMob 启用，AdColony、Meta、Vungle mediation 关闭。发布前仍需检查最终 AAB 的实际依赖。
- 没有照搬旧模板中的注册、营销邮件、仅匿名共享、12/24 个月保留期限、应用内隐私开关等未经确认的描述。

## 发布前待确认

1. **目标年龄未定。** 用户明确回复尚未决定。政策未擅自写成 13+、16+ 或 18+，也未承诺游戏面向儿童。确定 Play Console 目标受众后，复核儿童段落及 AdMob 的年龄、内容与广告配置；包含儿童时需要另行评估 Families 要求。
2. **广告隐私同意流程。** 当前 `ad_manager.gd` 在 Android 启动时调用 `MobileAds.initialize()`；业务脚本中未找到 UMP consent 更新、广告请求许可检查或隐私选项入口。插件自带 UMP API 不代表业务已接好。确认计划发行地区后，在需要的地区接好同意和撤回/隐私选项流程并真机验证，再发布；政策文本不能代替实际功能。
3. **应用内政策入口。** 本次业务脚本搜索未发现隐私政策网址或打开入口。正式版需提供可访问的政策链接。文稿未声称已有设置开关。
4. **广告状态。** 当前 `SHOW_AD_BUTTONS` 为 false，但 `_ready()` 仍初始化 AdMob。不能仅凭隐藏广告按钮认定无 SDK 数据处理。政策按用户确认的 AdMob 发行方案披露，最终以实际发布包为准。
5. **数据安全表。** 按最终 SDK 版本、manifest、依赖、AdMob 后台设置和运行行为填写，尤其注意广告标识符、IP 推算的大致位置、互动和诊断数据；不要把“无自建后端”填成“不收集数据”。Google 当前披露页针对其最新版本，不是本项目打包依赖的版本证明。
6. 确认公司在 Play Console 的登记名称/政策中的名称对应、地址和邮箱有效，确认英文游戏名。2026-10-28 是本次稿件日期；如果之后才发布，应在 MD 和 HTML 中同步更新生效日期。
7. 如需针对特定地区补充法定告知或广告退出机制，应先实现对应流程，再同步政策。不要仅添加无法兑现的法律承诺。

## 文件与发布

- 编辑稿：`sources/galactic-fireline/google-play/privacy.md`
- 发布页：`docs/galactic-fireline/google-play/privacy/index.html`
- 首页：`docs/index.html` 增加对应入口。
- 预计 URL：`https://panjung99.github.io/game-legal-pages/galactic-fireline/google-play/privacy/`
- GitHub Pages 使用 main 分支的 docs 目录；本次不自动提交或推送。发布前完成以上确认，并同时更新 MD 与 HTML。

## 参考资料

- https://developers.google.com/admob/android/privacy/play-data-disclosure
- https://developers.google.com/admob/android/privacy
- https://support.google.com/googleplay/android-developer/answer/10144311
- https://policies.google.com/privacy
- https://policies.google.com/technologies/partner-sites
- https://app-privacy-policy-generator.nisrulz.com/

## 本次生成稿修订说明

- 使用 `contact@panchenglabs.com` 作为正式稿所有联系和删除请求邮箱。
- 保留 Google Play services 和 AdMob 的隐私政策链接；这不意味着本游戏接入了 Google 登录或 Play Games。
- 移除无对应功能依据的页面访问统计、营销邮件和要求玩家提供个人信息的笼统表述。
- 将“仅传输汇总匿名数据”更正为广告 SDK 的具体数据披露。
- 删除未经运营确认的 12/24 个月保留承诺，分别说明本地存档、支持邮件和 Google 数据处理。
- 没有账号系统，不承诺账号删除功能；区分本地清除、公司控制的信息与 Google 控制的数据。
- 生成器将数字同意年龄 16 写成游戏不面向 16 岁以下，此处未照搬。13+ 是此前讨论的建议，用户尚未明确确认；目标受众和发行范围仍待最终确定。正式稿暂用不虚构固定年龄门槛的儿童隐私段落。
