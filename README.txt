Jee OS 2.4.0 — PCM Hourly Blocks

START ON WINDOWS
1. Install Node.js 22 or newer if it is not already installed.
2. Extract this ZIP into a normal writable folder.
3. Double-click start.bat.
4. The app opens at http://127.0.0.1:3000.

DAILY VIDEO PLAN
- Each available Morning block is 3 hours: Physics 1h, Chemistry 1h, Maths 1h.
- Each available Night block is also 3 hours: Physics 1h, Chemistry 1h, Maths 1h.
- Each subject proceeds through its chapters in its own syllabus order.
- Estimated watch time uses playlist-average original durations divided by 1.5× playback speed. Estimates are not exact per-video duration records.
- Whole videos only. If the next estimated whole video does not fit the remaining subject-hour, it carries to the next slot for that subject; unused minutes stay free for revision/practice. A video estimated longer than one hour would receive a dedicated whole-video slot.

SPECIAL DATES
- 10 October 2026: Night block only.
- 11 October 2026: both blocks are used for lectures, and no tests are scheduled on that date.
- Other Sundays remain protected rest/test days.

PRESERVED FEATURES
Dashboard, Planner, Calendar (today and future only), Syllabus, Revision, Tests, Settings, Watch links, playlist duration merge, local progress, backup import/export, optional Supabase cloud sync, Windows launcher, and the Android build workflow.

INTENTIONALLY OMITTED
Notes Studio and transcript upload/source-pack features. This version does not ask for notes or transcript files.

OTHER NOTES
- Existing local progress is kept under the app's existing browser storage key. The scheduler cache is rebuilt on launch for the PCM hourly layout.
- Supabase cloud sync is optional; the app works locally without signing in.
- The APK is not prebuilt in this ZIP; use the included GitHub Actions workflow to build it.
