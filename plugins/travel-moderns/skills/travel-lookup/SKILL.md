---
name: travel-lookup
description: Look up saved family trips, daily schedules, existing reservations, traveler preferences, past trips, or card benefits in Xingjian Travel. Use for questions about recorded travel facts.
---

Use the Travel MCP connection and `travel_query` to retrieve recorded facts. Use `travel-ideas` for saved travel wishes and `travel-credits` for supplier-issued travel credit. Skip Travel for general travel knowledge or public price searches.

Poll `travel_get_task` to a terminal state. Check the business receipt, `unresolved`, `pending_confirmations`, and `continuation`. Continue related questions in the same `session_id` and reuse `request_id` when retrying the same turn.
