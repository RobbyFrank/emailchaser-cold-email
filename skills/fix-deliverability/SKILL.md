---
name: fix-deliverability
description: Find out why cold emails land in spam or get few replies, and fix it with Emailchaser's mailbox health, warmup, DNS and inbox placement tools.
---

# Fix deliverability

Use this skill when open or reply rates drop, emails land in spam, or the user is about to add new sender mailboxes.

## Which tool to call

| Question | Tool |
|---|---|
| What is wrong right now, worst first? | `get_deliverability_insights` |
| Are SPF, DKIM and DMARC set up on this mailbox's domain? | `get_sender_email_dns` |
| Is warmup running, and how far along is it? | `get_sender_email_warmup`, `update_sender_email_warmup` |
| How is each mailbox's reputation? | `get_sender_reputation` |
| Where do test emails land (inbox, spam, missing)? | `list_inbox_placement_runs`, `get_inbox_placement_run`, `get_inbox_placement_stats_by_date` |
| Which mailboxes are sending, and how much? | `list_sender_emails`, `update_sender_email` |

## How to answer

1. Start with `get_deliverability_insights` and lead with its top issue and the action that fixes it.
2. For DNS problems, show the exact record to add or change at the user's domain host.
3. For a mailbox with poor placement, suggest lowering its daily limit or pausing it in campaigns while warmup continues, and say how to confirm the fix with the next placement run.
