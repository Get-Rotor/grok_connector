---
name: weekly-visits
description: Summarize this week's Rotor visits by day and crew, and flag unassigned or overbooked days.
---

# Summarize this week's visits

1. Call `get_current_context` to learn the company. "This week" is Monday 00:00 to the next Monday 00:00 in the user's timezone; ask the user if the timezone is unclear.
2. Call `list_visits` with ISO `start` and `end` for that range (a range can be at most 62 days). Page through all results.
3. Call `list_company_members` to turn each visit's `job.assigned_to` user IDs into names.
4. Call `get_visit` only for visits that need more detail.
5. Report by day: time, customer, address, job number, and assigned team members. Flag visits with nobody assigned and days that look overbooked.
6. End with totals: visits per day and per team member.

Read only. Never call `update_visit` unless the user asks to reschedule; moving a job's first visit also moves the job's start date, and automations may notify the customer.
