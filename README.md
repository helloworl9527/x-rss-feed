# X RSS Feed

使用 GitHub Actions 每天定时启动三次 RSSHub，抓取 X 账号 `weixin_wechat`、`openai`、`github`、`claudeai`、`elonmusk` 和 `bbchinesd`，然后把静态 RSS 发布到 GitHub Pages。

订阅地址：

```text
https://mystool.me/x-rss-feed/feeds/weixin_wechat.xml
https://mystool.me/x-rss-feed/feeds/openai.xml
https://mystool.me/x-rss-feed/feeds/github.xml
https://mystool.me/x-rss-feed/feeds/claudeai.xml
https://mystool.me/x-rss-feed/feeds/elonmusk.xml
https://mystool.me/x-rss-feed/feeds/bbchinesd.xml
```

## 维护

- 抓取时间：北京时间每天 07:00、11:00、20:00。GitHub 定时任务可能延迟。
- 手动更新：打开仓库的 **Actions → Update X RSS feed → Run workflow**。
- X 登录失效时，更新仓库 Secret `TWITTER_AUTH_TOKEN`。
- RSSHub 或 X 接口临时故障时，工作流会失败，但上一次成功发布的 RSS 仍然保留。

Token 仅保存在 GitHub Actions Secret 中，不在仓库文件里。
