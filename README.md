# X RSS Feed

使用 GitHub Actions 每天定时启动三次 RSSHub，抓取 X 账号 `weixin_wechat`、`openai`、`github`、`claudeai`、`elonmusk`、`thsottiaux`、`antigravity`、`anthropicai`、`googlegemma`、`z_lib_official`、`notionhq`、`google`、`naval`、`ssamat` 和 BBC 中文（`bbcchinese`），然后把静态 RSS 发布到 GitHub Pages。

订阅地址：

```text
https://mystool.me/x-rss-feed/feeds/weixin_wechat.xml
https://mystool.me/x-rss-feed/feeds/openai.xml
https://mystool.me/x-rss-feed/feeds/github.xml
https://mystool.me/x-rss-feed/feeds/claudeai.xml
https://mystool.me/x-rss-feed/feeds/elonmusk.xml
https://mystool.me/x-rss-feed/feeds/thsottiaux.xml
https://mystool.me/x-rss-feed/feeds/antigravity.xml
https://mystool.me/x-rss-feed/feeds/anthropicai.xml
https://mystool.me/x-rss-feed/feeds/googlegemma.xml
https://mystool.me/x-rss-feed/feeds/z_lib_official.xml
https://mystool.me/x-rss-feed/feeds/notionhq.xml
https://mystool.me/x-rss-feed/feeds/google.xml
https://mystool.me/x-rss-feed/feeds/naval.xml
https://mystool.me/x-rss-feed/feeds/ssamat.xml
https://mystool.me/x-rss-feed/feeds/bbchinesd.xml
```

## 维护

- 抓取时间：北京时间每天 07:00、11:00、20:00。GitHub 定时任务可能延迟。
- 手动更新：打开仓库的 **Actions → Update X RSS feed → Run workflow**。
- X 登录失效时，更新仓库 Secret `TWITTER_AUTH_TOKEN`。
- 单个账号抓取失败时会跳过该账号，并在上一份 feed 还在时保留它；其他账号继续更新。只有 RSSHub 起不来，或一份可用 feed 都没有时，工作流才会失败，已发布的页面保持不动。

Token 仅保存在 GitHub Actions Secret 中，不在仓库文件里。
