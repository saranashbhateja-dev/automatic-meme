# Jee OS 2.4.0 — PCM Hourly Blocks

This is the core JEE planner build. Notes Studio is intentionally omitted. The project retains the supplied tracker, playlist links, test/revision system, local progress, optional Supabase sync, and Android build workflow.

## Curriculum
- Physics: 43 chapters / 481 listed lectures
- Chemistry: 49 chapters / 868 listed lectures
- Maths: 37 chapters / 1,376 listed lectures
- Total: 129 chapters / 2,725 listed lectures
- `tracker.json` is the active seed; `playlist-durations.json` supplies average durations where available.

## Daily planner
- Each Morning block is 3 hours: Physics 1 hour, Chemistry 1 hour, Maths 1 hour.
- Each Night block is 3 hours with the same PCM allocation.
- Each subject progresses through its own chapters in tracker order.
- Videos are estimated from playlist-average original durations divided by 1.5 for the playback speed. These are estimates, not exact per-video durations.
- Videos are never split. If the next whole video does not fit the remaining subject-hour, it carries into the next slot for that subject; unused time remains available for revision/practice. A video estimated longer than a full subject-hour would be placed in a dedicated whole-video overrun slot.
- Special kickoff dates: 10 Oct 2026 has the Night block only; 11 Oct 2026 has both blocks and no planned tests. Other Sundays remain protected test/rest days.

## Run on Windows
1. Install Node.js 22 or newer.
2. Extract the ZIP into a writable folder.
3. Double-click `start.bat`.
4. Jee OS opens in your default browser at `http://127.0.0.1:3000`.
Do not open `index.html` directly.

## Playlist duration refresh (optional)
The included backend script can refresh playlist duration averages using the YouTube Data API v3. It requires your own API key in the terminal environment; no API key is bundled. In PowerShell, from the project folder:

```powershell
$env:YOUTUBE_API_KEY="YOUR_YOUTUBE_DATA_API_V3_KEY"
npm run refresh:durations
```

Restrict the key to YouTube Data API v3 and do not paste or commit the key. Public playlist videos are supported, while private, deleted, restricted or unavailable videos may not return data. The app also works with the included duration data without refreshing it.

## Android
Capacitor configuration and the GitHub Actions APK workflow are included. The APK itself is not prebuilt in this ZIP. Push the project to GitHub and run the workflow to produce a debug APK. The workflow keeps the Watch buttons while removing chapter-link editing controls from the APK.

## Notes
- Notes Studio and all transcript/notes upload UI are omitted from this version by design.
- Local progress stays in this browser's storage. Supabase cloud sync remains optional.
- See `PATCH-NOTES-2.4.0.txt` and `FINAL-AUDIT.md` for the version summary and checks performed.
