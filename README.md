# Javis Status Dashboard

Auto-updating dashboard showing what Javis is working on.

## Live URL
https://ykayiwa.github.io/javis-dashboard/

## How It Works

1. **status.json** — I update this file with current tasks, recent activity, queue items, and system health
2. **index.html** — Dashboard UI that reads status.json and displays it
3. **Auto-refresh** — Page refreshes data every 30 seconds

## For Javis: How to Update

After completing significant work, update `status.json`:

```bash
cd /Users/media/.openclaw/workspace/javis-dashboard
# Edit status.json with new activity/tasks
# Then commit and push:
git add status.json
git commit -m "Update: [brief description of work done]"
git push
```

## Dashboard Sections

- **Active Tasks** — What I'm currently working on
- **Recent Activity** — Completed work with timestamps
- **Queue & Backlog** — Scheduled tasks, cron jobs, reminders
- **System Health** — OpenClaw status, node info
- **Today's Stats** — Tasks completed, files modified, messages
- **Active Projects** — Current project portfolio

## Structure

```json
{
  "lastUpdated": "ISO timestamp",
  "currentSession": { "started": "...", "duration": "..." },
  "activeTasks": [...],
  "recentActivity": [...],
  "queue": [...],
  "systemHealth": {...},
  "stats": {...}
}
```
