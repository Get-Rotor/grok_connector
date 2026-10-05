---
name: weekly-visits
description: Summarize this week's Rotor visits by day and crew, and flag unassigned or overbooked days.
---

# Summarize this week's visits

1. Call `get_current_context` to learn the company. Use the company's timezone for "this week" (Monday 00:00 to next Monday 00:00).
2. Call `list_visits` with ISO `start` and `end` for that range (a range can be at most 62 days). Page through all results.
3. Call `get_visit` only for visits that need more detail.
4. Report by day: time, customer, address, job, and crew. Flag visits with no crew and days that look overbooked.
5. End with totals: visits per day and per crew member.

Read only. Never call `update_visit` unless the user asks to reschedule; moving a job's first visit also moves the job's start date, and automations may notify the customer.
