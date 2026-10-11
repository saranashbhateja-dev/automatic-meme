# Jee OS 2.4.0 — Build Audit

## Source data
- `tracker.json` retained unchanged from the prior core planner build.
- Chapters: 129
- Listed lectures: 2,725
- Physics: 43 chapters / 481 lectures
- Chemistry: 49 chapters / 868 lectures
- Maths: 37 chapters / 1,376 lectures
- `playlist-durations.json` retained unchanged.

## Scheduling behavior
- Morning and Night are each 3-hour blocks.
- Every block independently reserves one hour each for Physics, Chemistry and Maths.
- Each subject follows its own chapter order from the included tracker.
- Whole-video scheduling estimates original playlist-average duration divided by the saved 1.5× playback speed. Individual video estimates are approximate.
- A video that does not fit within the remaining hour is carried to the next slot for the same subject; no video is split.
- 10 Oct 2026: Night only. 11 Oct 2026: both blocks and no planned tests. Other Sundays remain protected.

## Preserved features
- Dashboard, Planner, Calendar (past calendar cells hidden), Syllabus, Revision, Tests and Settings.
- Local-first progress and backup import/export.
- Optional Supabase cloud sync.
- Playlist Watch buttons and Android build workflow.
- Notes Studio intentionally absent.

## Checks completed
- `node --check app.js`: passed.
- `node --check server.js`: passed.
- JSON parse checks for `tracker.json`, `playlist-durations.json` and `package.json`: passed.
- Schedule harness: checked Oct 10 Night-only, Oct 11 two-block exception, regular Sunday rest behavior, and one-hour PCM caps.
- Full schedule simulation: all 2,725 lecture entries assigned exactly once, no duplicates; 202 future lecture days from the supplied start configuration.
- Local server smoke test: `/health`, `/`, `/app.js` and `/tracker.json` returned HTTP 200.
- ZIP integrity check is run after packaging.
- Android APK compilation is not claimed; only the source workflow is included.
