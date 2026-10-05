---
name: triage-leads
description: Triage the Rotor leads that need action today, grouped by pipeline stage, with a suggested next step for each.
---

# Triage today's leads

Use the Rotor MCP tools to show which leads need attention today.

1. Call `get_current_context` to learn the company and the user's role.
2. Call `list_pipelines` and `list_pipeline_stages` to learn the stage order.
3. Call `list_leads` (page through results, 100 per page at most). Filter by `stage` when the user names one.
4. For leads that look stalled or new, call `get_lead` for detail.
5. Report leads grouped by stage, oldest first. For each: name, stage, last activity, assignee, and one suggested next step (call, text, quote, or close out).
6. End with counts per stage.

Read only. Never call `create_lead`, `update_lead`, or any other write tool unless the user asks for that change in this conversation; Rotor automations may send email or SMS when a lead changes.
