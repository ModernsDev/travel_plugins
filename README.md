# 行间 Travel

在 ChatGPT 中查看家庭旅行和已登记的预订，维护每日安排，保存想去的地方。

## 导入工作区

管理员在 ChatGPT 管理控制台打开 **Plugins → Add → Import marketplace**。

- Source：`https://github.com/ModernsDev/travel_plugins`
- Path：留空
- Branch, tag, or commit：留空以跟踪 `main`

导入后查看平台标记和安装权限。此包直接声明远程 MCP，可能被标为 Desktop only。每位使用者用自己的行间 Travel 账号完成 OAuth 授权。

也可以在支持自定义 MCP 的 ChatGPT 网页端添加 `https://travel.moderns.dev/ai/mcp/`，选择 OAuth。

[OpenAI GitHub 导入说明](https://help.openai.com/articles/20001504)
