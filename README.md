# Tombly

**Find the subscriptions you forgot, and bury the ones you don't need.**

Tombly is a web app that detects recurring charges from your bank or card statements, shows what you're really spending each month, and warns you before each renewal so you can cancel in time.

---

## The Problem

Most people pay for subscriptions they've forgotten about: a free trial that converted, an app they stopped using, a streaming service they only needed for one show. These charges are:

- **Invisible**: they're small and scattered across multiple cards and accounts.
- **Easy to forget**: nothing reminds you they exist until you scan a statement.
- **Costly over time**: a few forgotten $10 charges add up to hundreds per year.

## The Solution

Tombly finds recurring charges for you. Paste or upload statement lines, and the app detects repeating payments, groups them into subscriptions, and shows your total monthly and yearly burn. Before each renewal, it sends a heads-up so you can decide whether to keep or cancel.

## Key Features (MVP)

- **Statement import**: paste transaction text or upload a CSV from your bank or card.
- **Recurring charge detection**: identifies repeating payments by merchant, amount, and interval (weekly, monthly, yearly).
- **Subscription dashboard**: every detected subscription in one list with cost, frequency, and next expected charge.
- **Monthly and yearly burn**: total recurring spend at a glance, with a breakdown by category.
- **Renewal alerts**: email reminders (for example 7 days and 1 day) before each charge.
- **Keep / Cancel marking**: tag each subscription as "keep", "reviewing", or "buried" (cancelled), and track money saved.
- **Manual add and edit**: correct anything the detection got wrong or add subscriptions yourself.

## How It Works

1. **Import** your statement lines (paste or CSV upload).
2. **Review** the subscriptions Tombly detected and confirm or edit them.
3. **Get alerts** before each renewal.
4. **Bury** what you don't need and watch your monthly burn shrink.

## Target Users

- Anyone who suspects they're paying for things they don't use
- Budget-conscious individuals and households
- Freelancers tracking software and tool costs
- People who sign up for free trials and forget to cancel

## Privacy Approach

Financial data is sensitive, so the MVP avoids direct bank connections.

- No bank login or open-banking access in v1; the user supplies the data.
- Only transactions the user imports are stored.
- Option to delete all data at any time.
- Optional: process imports in the browser and store only the detected subscriptions, not raw statements.

## Planned Roadmap

**v1.0: MVP**
- Account signup and login
- Paste and CSV import
- Recurring charge detection
- Dashboard with monthly and yearly totals
- Email renewal alerts
- Keep / Cancel marking

**v1.1**
- Forward-an-email import (receipts and renewal notices)
- Free trial tracking with end-date alerts
- "How to cancel" links for popular services
- Shared household view

**v2.0**
- Optional bank connection through an open-banking provider
- Price-increase detection
- Duplicate and overlapping service warnings
- Monthly savings report

## Proposed Tech Stack

> Suggestions only; finalize before building.

| Layer | Option |
|---|---|
| Frontend | React / Next.js |
| Backend | Node.js (Next.js API routes) or similar |
| Database | PostgreSQL |
| Auth | Email + password, or a hosted auth provider |
| Parsing / detection | Rule-based matching on merchant, amount, and interval; optional merchant-name normalization list |
| Email delivery | Transactional email service (Resend, Postmark, or SendGrid) |
| Scheduling | Cron job or queue-based worker for renewal alerts |
| Hosting | Vercel / Render / Fly.io |
| Payments (billing) | Stripe |

## Pricing Idea (Draft)

| Plan | Price | Includes |
|---|---|---|
| Free | $0 | Up to 10 subscriptions, one import at a time, email alerts |
| Pro | ~$5/month | Unlimited subscriptions, email forwarding, trial tracking, savings reports |
| Household | ~$9/month | Shared view for multiple people |

## Success Metrics

- Average number of subscriptions detected per user
- Total monthly spend cancelled by users ("money saved")
- Import completion rate (how many users finish their first import)
- Alert open and click rates
- Free-to-paid conversion rate

## Open Questions

- How accurate can detection be with messy merchant names across different banks?
- Which CSV formats should be supported first?
- Is pasted text or CSV upload the easier first step for users?

## Project Status

**Planning stage.** No code has been written yet.

## Getting Started

_Setup instructions will be added once development begins._

## Contributing

_Contribution guidelines to be added._

## License

_MIT_
