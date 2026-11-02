---
name: launch-a-cold-email-campaign
description: Take a cold email campaign from a company website to a launched Emailchaser campaign: ideal customer profile, sequence, leads, sender mailboxes and schedule.
---

# Launch a cold email campaign

Use this skill when the user wants to start outreach to a new audience, or turn a draft into a live campaign.

## Steps

| Step | Tool | Notes |
|---|---|---|
| 1. Draft the audience and the emails | `copilot_plan` | Give it the user's company website. Read-only. |
| 2. Size the audience | `get_audience_size`, `search_lead_finder` | Both free. Lead Finder results are masked until revealed. |
| 3. Save the audience | `create_icp`, `set_primary_icp` | |
| 4. Create the draft campaign | `copilot_launch` or `create_campaign` | Both create a draft that sends nothing. |
| 5. Write or edit the sequence | `replace_campaign_sequence` | Replaces the whole sequence, so send every step each time. |
| 6. Add leads | `add_leads` (the user's own list) or `source_prospects` (spends credits) | |
| 7. Attach sender mailboxes | `list_sender_emails`, `attach_campaign_sender_emails` | |
| 8. Set the sending window | `update_campaign_schedule` | |
| 9. Launch | `launch_campaign` | Only after the user approves the summary below. |

## How to answer

1. Before step 9, show one summary: audience size, number of leads, each email in the sequence, the sender mailboxes and the schedule.
2. After launch, give the campaign name and id, and check `get_campaign_stats` the next time the user asks.
