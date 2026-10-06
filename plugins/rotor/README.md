# Rotor for Cursor

[Rotor](https://www.getrotor.com) is the operating system for field service businesses: window cleaning, exterior cleaning, and property services. This plugin connects Cursor to Rotor's MCP server so you can ask about your work and move it forward from chat.

The plugin is free. It needs a Rotor account; Rotor itself is a paid product.

## Install

In Cursor, run `/add-plugin rotor`, or open the Marketplace, find **Rotor**, and select **Install**.

## Sign in

The first time Cursor calls a Rotor tool, it opens Rotor in your browser. Sign in, choose the company to connect if you belong to more than one, review the access, and select **Allow**. Cursor stores the connection; you stay connected until you revoke access.

Rotor answers only from the company you chose, and only what your Rotor role can already see. Payroll is limited to owners and admins.

## What you can ask

- What visits are scheduled for this week?
- Which invoices are past due, and by how much?
- Show me the leads that came in this month and where they are in the pipeline.
- Create a lead for Dana Whitfield at 214 Oak Street, phone 555-0142.
- What did the crew log on yesterday's jobs?

The server exposes 47 tools: 37 read and 10 write. Write tools create and update leads, customers and tasks, reschedule visits, and create campaigns, campaign audiences and message templates. No tool moves money: payments, invoices, quotes and payroll are read-only. Creating or updating leads, customers and visits can trigger your company's automations, which may send email or SMS.

## Skills

| Skill | What it does |
| --- | --- |
| `triage-leads` | Leads that need action today, by stage, with a next step |
| `weekly-visits` | This week's visits by day and crew, with gaps flagged |

## Server

| | |
| --- | --- |
| URL | `https://mcp.getrotor.com/mcp` |
| Transport | Streamable HTTP |
| Auth | OAuth 2.1, dynamic client registration, PKCE |

## Support

- Help center: https://helpcenter.getrotor.com
- Email: support@getrotor.com
- Privacy: https://www.getrotor.com/privacy
- Terms: https://www.getrotor.com/terms
