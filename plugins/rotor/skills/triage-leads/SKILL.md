---
name: triage-leads
description: Triage the Rotor leads that need action today, grouped by pipeline stage, with a suggested next step for each.
---

# Triage today's leads

Use the Rotor MCP tools to show which leads need attention today.

1. Call `get_current_context` to learn the company and the user's role. Use today's date from the conversation; ask the user if it is unclear.
2. Call `list_pipelines` and `list_pipeline_stages` to learn the stage order.
3. Call `list_company_members` to turn each lead's `assigned_to` user ID into a name.
4. Call `list_leads` and page through all results (100 per page at most). Filter by `stage` when the user names one.
5. A lead needs action today when its `follow_up_date` is today or earlier, or it was created in the last 2 days and has no `follow_up_date`. Call `get_lead` only when you need its notes.
6. Report those leads grouped by stage in pipeline order, most overdue first. For each: name, stage, priority, follow-up date, assignee, projected value, and one suggested next step (call, text, quote, or close out).
7. End with counts per stage and the number of unassigned leads.

Read only. Never call `create_lead`, `update_lead`, or any other write tool unless the user asks for that change in this conversation; Rotor automations may send email or SMS when a lead changes.
