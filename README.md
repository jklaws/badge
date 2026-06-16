# badge

This repo backs my **GitHub Universe badge**. Each capability the badge supports
lives in its own folder, so everything the badge knows is tracked here.

> **Note: this agenda is public.** The repo is public so the badge can read it
> with no login. Anyone who knows my GitHub username can see it too, so it only
> holds things I'm fine sharing.

| Folder | Used by | What it is |
|--------|---------|------------|
| `agenda/` | Agenda app | `agenda.json` — my live schedule (the badge syncs it over Wi-Fi) |

## agenda/agenda.json format

```json
{
  "event": "My Universe '26",
  "year": 2026,
  "days": [
    { "title": "OCT 28 - DAY 1", "date": "2026-10-28", "sessions": [
      { "start": "09:00", "end": null,    "title": "Keynote",  "subtitle": "Main Stage" },
      { "start": "10:30", "end": "12:00", "title": "Workshop", "subtitle": "Hall A" }
    ]}
  ]
}
```

- `start` / `end` are `"HH:MM"` (24h). `end` may be `null` for an open-ended item.
- `date` is `"YYYY-MM-DD"`; the badge highlights the session happening **now**.

Edit this file and the badge picks it up on the next sync (hold **A+C**, or press **B**, in the Agenda app).
