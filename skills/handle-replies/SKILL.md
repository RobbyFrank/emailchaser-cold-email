---
name: handle-replies
description: Triage replies to cold email campaigns in Emailchaser, edit and send AI reply drafts with the user's approval, and record booked meetings.
---

# Handle replies

Use this skill when the user asks who replied, wants to answer prospects, or wants to log meetings.

## Which tool to call

| Task | Tool |
|---|---|
| See new replies, filtered by category or campaign | `list_replies` |
| Read the whole thread with one prospect | `get_lead_conversation` |
| See the AI reply drafts waiting | `list_reply_drafts` |
| Edit a draft | `update_reply_draft` |
| Send a draft, or a reply you wrote | `send_reply_draft`, `send_reply` (cannot be recalled) |
| Change a reply's category | `update_lead_category` |
| Record or undo a booked meeting | `mark_lead_meeting`, `unmark_lead_meeting` |
| See replies, positive replies and meetings against spend | `get_outcomes_report` |

## How to answer

1. Group new replies by category (interested, meeting request, not now, unsubscribe) and lead with the interested ones.
2. For each reply the user wants to answer, show the draft in full, apply their edits with `update_reply_draft`, and send only after they say so.
3. When a prospect books a call, record it with `mark_lead_meeting` so the outcomes report counts it.
