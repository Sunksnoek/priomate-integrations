---
name: priomate
description: Use when the user asks about their tasks, to-dos, deadlines, notes, drafts, inbox, time tracking or team projects in Priomate - to look things up, create or update tasks, mark them done, track time or post in a project chat.
---

# Priomate

Use the Priomate tools for anything about the user's own Priomate workspace: tasks, checklist items, color tags, notes, drafts, inbox, time entries, and team projects with their tasks and chat.

## Reading

- For "what is on my plate" questions start with `tasks_overview`; for a specific task use `tasks_search`, `tasks_list` or `tasks_get`.
- Team projects: `projects_list`, then `project_get` and `project_messages`.
- Time: `time_totals`, `time_entries`, `time_running`.
- Help questions about how Priomate works: `docs_search`, then `docs_get`.

## Changing things

- Before creating, changing, completing, or posting anything, tell the user what you are about to do and wait for a clear yes. Batch several changes into one confirmation.
- After a change, report what was changed.
- Only touch data the user asked about. Never guess an id: look the item up first.

## Limits

- Priomate tools cannot delete anything. If asked to delete tasks, notes, projects, or time entries, say that deleting is not possible through this connection and that the user has to do it in the Priomate app.
- Only the signed-in user's own workspace and the team projects they belong to are accessible. Do not try to look up other people's accounts.
