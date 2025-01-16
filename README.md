# 红杏加速器
### 一次性套餐+自动化签到=机场永久使用
1. 复制workers.js中的代码到cloudflareWorkers中
2. 完整脚本的详细使用方式
 - 以下是你的 Cloudflare Worker 脚本的使用方式以及配置说明。这个脚本的目的是每天通过定时任务自动执行签到操作，并通过 Telegram 发送签到结果。所有的敏感信息（如 Telegram Bot Token 和签到账号的邮箱和密码）都通过环境变量进行配置。
3. 环境变量设置
  - 脚本通过环境变量获取配置参数，确保敏感信息不会直接硬编码在代码中。你需要在 Cloudflare Workers 的配置中设置以下环境变量：

  - `TG_BOT_TOKEN`：你的 `Telegram Bot Token`。
  - `TG_CHAT_ID`：你要发送消息的 Telegram 群或个人的 Chat ID。
  - `HX_EMAIL`：用于登录红杏加速器的邮箱。
  - `HX_PSD`：用于登录红杏加速器的密码。

4. 定时任务配置
  - `10 16 * * *` 每天凌晨00:10分签到
