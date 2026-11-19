---
name: travel-itinerary
description: Plan, create, or update a formal family trip in Xingjian Travel. Use for daily itinerary planning, moving activities, changing time windows, or resolving schedule conflicts.
---

Read the affected trip, days, confirmed bookings, and current versions through Travel MCP. Keep tentative plans in chat until the user asks to save them. For explicit creation of a formal trip, use `travel_create_trip`.

For a local itinerary edit, use a versioned `PATCH /trips/{id}/itinerary` with only the affected dates or time windows. Keep existing bookings and unspecified itinerary content intact. Prepare the fixed change with `travel_propose_change` and execute it with `travel_execute_change` without a separate approval step.

Poll `travel_get_task` until terminal. Check read-back evidence and report every actual change and unresolved item. Handle `pending_confirmations` and `continuation` in the same session, using the original task tool for follow-ups. If a write outcome is unknown, check actual state before retrying with the same request ID.
