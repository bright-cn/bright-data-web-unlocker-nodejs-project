# Bright Data Web Unlocker Node.js 项目
[![Bright Data 推广](https://github.com/bright-cn/LinkedIn-Scraper/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://www.bright.cn/)

[在 StackBlitz 编辑器中编辑 ⚡️](https://stackblitz.com/~/github.com/bright-cn/bright-data-web-unlocker-nodejs-project?file=index.js)

## Bright Data Web Unlocker API 示例

本项目演示如何使用 Bright Data 的 [Unlocker API](https://www.bright.cn/products/web-unlocker) 通过 Bright Data 的 [Unlocker API](https://www.bright.cn/products/web-unlocker) 访问网站。

## 概览

该脚本通过使用 Bright Data 的 Web Unlocker，帮助你在访问具备反爬虫保护或包含验证码的站点时自动绕过这些障碍。

### 在 StackBlitz 中使用环境变量

1. 选择 `.env` 文件
2. 添加以下变量：
   - `BRIGHT_DATA_API_TOKEN`：你的 Bright Data [API Token](https://docs.brightdata.com/general/account/api-token)
   - `BRIGHT_DATA_ZONE`：你的 Bright Data [Zone](https://www.bright.cn/cp/zones) 名称（例如 `web_unlocker1`）

### 直接配置

或者，直接在脚本中编辑 CONFIG 对象：

```javascript
const CONFIG = {
  apiToken: process.env.BRIGHT_DATA_API_TOKEN || 'YOUR_API_TOKEN', // 替换为你的实际 Token
  zone: process.env.BRIGHT_DATA_ZONE || 'web_unlocker1',           // 替换为你的 Zone
  targetUrl: 'https://geo.brdtest.com/welcome.txt'                 // 替换为你的目标 URL
};
```

## 运行示例

1. 确认已配置好 `API token` 和 `zone`
2. 在终端运行 `node index.js`
3. 在控制台查看输出结果

## 工作原理

1. 脚本向 Bright Data 的 Unlocker API 端点发送一个 POST 请求
2. 请求中包含你的认证 Token 与目标 URL
3. Bright Data 的 Web Unlocker 访问目标 URL
4. 响应返回到你的脚本，并在控制台展示

## 故障排除

如果遇到错误：

- 确认你的 API Token 正确无误
- 检查 Zone 名称是否有效
- 确保目标 URL 格式正确

## 修改示例

若要请求不同的 URL：
1. 更新 CONFIG 对象中的 `targetUrl`
2. 重新运行脚本

## 更多资源

- [Bright Data Web Unlocker API](https://docs.brightdata.com/scraping-automation/web-unlocker/introduction)
- [获取 API Token](https://docs.brightdata.com/general/account/api-token)
- [管理 Zones](https://www.bright.cn/cp/zones)

注意：这是一个用于学习的示例实现。在生产环境中，请考虑增加更完善的错误处理、日志记录与安全措施。
