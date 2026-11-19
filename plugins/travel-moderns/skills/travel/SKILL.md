---
name: travel
description: 查询或维护用户家庭在行间 Travel 已登记的旅行、预订、每日安排、偏好、权益和旅行想法。用于用户自己的旅行资料。
---

使用 Travel MCP。需要连接时，请用户在客户端通过 OAuth 登录自己的 Travel 账号并授权。

先查 Travel 已登记事实，再回答或规划。调用 travel_query 后用 travel_get_task 查询终态，核对业务回执、unresolved、pending_confirmations 和 continuation。相关追问复用 session_id。同一请求重试沿用 request_id。

按用户要求维护记录时，先查当前记录、版本及 API 契约。优先使用对应的专用工具，否则用 travel_propose_change 和 travel_execute_change 提交并执行固定提案，无需重复征求业务批准。核对写后回读。若结果未知，先查询状态，避免重复写入。登记或修改已确认预订后，检查受影响日期并处理计划冲突。汇报实际变更、连带调整和未解决事项。缺少实质影响结果的信息时再询问用户。供应商交易须有已接入的能力与相应授权。

用户明确表达的旅行愿望或粗略构想，先用 travel_list_ideas 查重，再用 travel_save_idea 保存或补充并保留来源。范围限于当前可访问聊天中用户表达的意图。
