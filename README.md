# chatgpt_commercial
**本项目是基于我的开源版本 https://github.com/dirk1983/chatgpt 开发的商业版，和开源项目相比有以下几项差异：**

| 差异 | 开源版 | 商业版 |
| --- | --- | --- |
| 是否开源 | 完全开源 | 部分开源，部分代码需要绑定域名运行 |
| 项目定位 | 个人自用或小范围分享，对服务器资源要求低 | 商业化运营，支持用户付费使用，对服务器资源要求高一些 |
| 问答速度 | stream流模式，session传递问题和上下文，无需数据库，但多人同时使用时可能会卡顿 | stream流模式极速版，更多异常和超时处理机制，数据库传递问题和上下文，多人使用不卡顿 |
| 支持会员 | 不支持 | 支持会员和提供付费业务 |
| API_KEY数量 | 只能配置一个 | 可以配置无数个，自动轮询，自动剔除无效API_KEY |
| 前端界面 | 默认深色背景风格 | 默认浅色背景风格，未来将支持多种风格随意替换 |
| 使用模式 | 只能免费分享给朋友使用，或要求使用者自备API_KEY | 用户可以通过在线支付购买查询次数，或通过淘宝或发卡站购买储值卡使用 |
| 角色和问答 | 支持预设问题，不支持定义角色 | 未来支持定义角色和针对各业务的预设问题 |
| 功能扩展 | 免费使用，用户根据自己需要改进代码，开源版未来没有架构层面修改的计划 | 一次购买永久免费升级，用户可以提需求，商业版会不断改进并持续更新 |

**本项目目前已实现的功能如下：**

1. 无需注册会员，微信扫码登录。由于注册微信有门槛，因此方便用户登录的同时，还可以防止用户批量注册账号白嫖体验次数。还可以给公众号引流。
2. 每个微信用户可以设置成免费体验若干条数。
3. 后台可以设置API_KEY列表，全局+出错时自动轮询，保证用户每次查询都能返回结果。
4. 支持批量生成充值卡，可设置查询次数和有效期。次数和有效期用完之前续费，累加次数并延长有效期。
5. 暂时不支持微信支付或支付宝付费接口，可以生成充值卡后挂到发卡站、淘宝店、微店、扫站长微信二维码转账。
6. 进一步优化接口响应速度，实现秒级回复，并支持查询和继续历史对话。

**未来功能规划：**
1. 支持批量查看每个API_KEY的余额等信息，支持二次验证被标记为失效的KEY
2. 如果系统的回答速度超过n秒则本次问答免费
3. 支持多个前端UI风格自由切换
4. 对于已开通企业微信支付或支付宝支付的站长，支持用户自行扫码购买查询次数，不用再通过充值卡充值。
5. 支持自定义ChatGPT的system_role，对具体使用场景进行效果优化，比如写代码、写文章、翻译等
6. 支持用户分享奖励，即通过用户分享链接每注册一个账户则奖励用户一定查询次数，每付费一个用户则奖励一定比例的查询次数
7. 其他功能大家可以提需求，我认为合理的会考虑增加

该商业版软件我打算利用空闲时间兼职开发，近期发布的版本中包含已规划好的6点功能，未来功能规划后续逐步实现。

初步计划定价299元，限量200人，未来随着功能不断完善可能会提升价格，但只要一次购买终身免费升级。

商业版不完全开源，需要绑定域名，对于大家普遍的需求我会尽快完善免费更新，对于个性化定制需求可以单独付费开发。

测试网址和购买方式请进群获取，每个用户免费提问10次，欢迎测试并提出宝贵意见。

**前台界面截图如下：**

PC端：

![1](https://user-images.githubusercontent.com/5563148/232328735-412a2910-354d-4c05-99af-d6b9650a94c2.png)
![2](https://user-images.githubusercontent.com/5563148/232328747-ba4d9e6a-c003-4eee-840c-fdc2219a9b9e.png)
![3](https://user-images.githubusercontent.com/5563148/232328749-34cb8beb-74d0-47ca-a5e4-297d584e9c20.png)
![4](https://user-images.githubusercontent.com/5563148/232328753-a43a353c-a7e0-4991-be4f-5e52639853c5.png)

手机端：

![m1](https://user-images.githubusercontent.com/5563148/232328803-2cc476ad-4ae4-480d-ae54-8c706ba19a17.jpg)
![m2](https://user-images.githubusercontent.com/5563148/232328806-e9b6d916-b921-465f-a427-87bcdf49bbc3.jpg)
![m3](https://user-images.githubusercontent.com/5563148/232328808-92102760-ab3b-40f7-b397-fe9a61eda36e.jpg)
![m4](https://user-images.githubusercontent.com/5563148/232328810-b3684b0b-1687-4f5d-9347-406a38a02689.jpg)
![m5](https://user-images.githubusercontent.com/5563148/232328801-ff8e6cae-3120-4286-9f10-a0bf9739a525.jpg)

后台：

![b1](https://user-images.githubusercontent.com/5563148/232328835-cac61a1d-146a-4194-840f-066a599e9a83.png)
![b2](https://user-images.githubusercontent.com/5563148/232328836-ef739254-7f2a-4dab-a3fc-5e5698484418.png)
![b3](https://user-images.githubusercontent.com/5563148/232328837-c7e86353-e04d-41da-a9d3-17bae3cff137.png)
![b4](https://user-images.githubusercontent.com/5563148/232328838-3150e2e2-7b88-4099-97e8-4b3e15e39db0.png)
![b5](https://user-images.githubusercontent.com/5563148/232328840-2bfa1978-e22a-4492-bf77-38c1b0655820.png)
![b6](https://user-images.githubusercontent.com/5563148/232328842-002d26bb-165c-49db-9a4e-517462298abc.png)
![b7](https://user-images.githubusercontent.com/5563148/232328844-928be3c4-ce89-470a-91c3-6c084cdde849.png)
![b8](https://user-images.githubusercontent.com/5563148/232328846-bdd1f14f-ca21-41f4-8a17-eee7b7735593.png)
![b9](https://user-images.githubusercontent.com/5563148/232328847-786ea909-96e5-4b30-80d3-e586766b90f5.png)
![b10](https://user-images.githubusercontent.com/5563148/232328849-49fe83d5-e3b8-423f-b1b2-d36153344d7b.png)
![b11](https://user-images.githubusercontent.com/5563148/232328851-70c2dfe1-5ed4-496c-a44e-f4e0c5b3cd28.png)
![b12](https://user-images.githubusercontent.com/5563148/232328853-a6884ce6-e0dc-4094-8a28-97f24df6727d.png)
