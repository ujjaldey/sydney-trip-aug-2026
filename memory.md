# Memory

## Purpose
This file stores a persistent record of our conversations, decisions, preferences, and context so I can refer back to it whenever required.

---

## Session Log

### Session 1 — 2026-08-07
- User asked me to create this `memory.md` file.
- This file will be used to capture all future conversations and context for reference.

---

## About the User

- **Name:** Ujjal
- **Travels with:** Wife (both are photographers).

---

## Travel Preferences

- Both are photographers — trips should be photography-oriented to capture good photos.
- Enjoy walking in nature trails and light hiking.
- Prefer to avoid overly touristy places.
- Like trips that are simple, quiet, and close to nature.

---

## Travel Plans

### Sydney Trip — August/September 2026
- Ujjal is planning trips in and around Sydney.
- **Dates:** 28 August 2026 to 6 August 2026 *(note: end date appears to be a typo — likely 6 September 2026; needs clarification)*

---

### Trip 1 — Blue Mountains (First Weekend)
- **When:** First weekend of the trip (likely Sat 29 – Sun 30 Aug 2026).
- **Starting point:** Strathfield (user said "Stratfield", likely Strathfield, Sydney).
- **Transport:** Driving from Strathfield to Blue Mountains.
- **Day 1 (morning):** Depart Strathfield in the morning, drive to Blue Mountains.
- **Accommodation:** Rent a BnB or a decent hotel, staying overnight.
- **Day 2:** Roam around in the morning, then drive back to Strathfield by afternoon or evening.

---

## Working Files

- **`Blue Mountain Trip.md`** — the FINAL planner document for the Blue Mountains trip. Created 2026-08-07. Contains: blog research (Gary P Hayes, Walk My World, NSW NPWS, My Katoomba, + more), a 2-day itinerary (Sat 29 / Sun 30 Aug), accommodation shortlist, photo-spot table, logistics, packing list, and to-do checklist. User wants this as the final planning doc — keep it updated.
- **`memory.md`** — this file; captures conversation history and context.

---

## Session 2 — 2026-08-07 (Blue Mountains research)
- User asked me to search the internet for blogs by like-minded travellers (photographers/nature lovers, last couple of years) about the Blue Mountains, and document everything in a single markdown file `Blue Mountain Trip.md` to use as the final trip planner.
- Researched and documented: Gary P Hayes (landscape photographer local), Walk My World (hiking couple), NSW National Parks blog, My Katoomba (local hosts), plus Logds.com, Australia for Beginners, Girt By Sea Photography, Momentslog, Australian Photography, George Wheelhouse, Jay Evans.
- Key planning inputs captured: trip is winter (late Aug) — cold (~0–3°C mornings), strong waterfalls, dramatic skies; best sunrise = Govetts Leap/Narrow Neck; best sunset = Lincoln's Rock; recommended quiet walks = Valley of the Waters, Grand Canyon Loop, Minnehaha Falls, Fairy Bower, Rocket Point.
- Open item still pending: confirm trip end date (28 Aug → 6 **Aug** is a typo — likely 6 Sep).

---

## Google Docs Integration (in progress)
- **Goal:** Replace/augment markdown output with direct updates to Google Docs. User wants the Blue Mountains planner maintained as a Google Doc.
- **Decisions made (2026-08-07):**
  - Auth method: **OAuth desktop app** (docs owned by user's own account, appear in their Drive).
  - Config scope: **Global config** (`~/.config/opencode/opencode.json`).
  - MCP server: **`@a-bonus/google-docs-mcp`** (npx, tools: docs_create, docs_read, docs_append_text, docs_replace_text, etc.; token stored at `~/.config/google-docs-mcp/token.json`).
- **User still needs to do (Google Cloud Console):** create project, enable Google Docs API + Drive API, configure OAuth consent screen, create OAuth Client ID (Desktop app), and share the Client ID + Client Secret (or the downloaded JSON).
- **My next steps (after user confirms):**
  1. Add `mcp.google-docs` block to `~/.config/opencode/opencode.json` (keep existing Ollama provider).
  2. Run `GOOGLE_CLIENT_ID=... GOOGLE_CLIENT_SECRET=... npx -y @a-bonus/google-docs-mcp auth` (opens browser for one-time approval).
  3. Restart opencode; recreate `Blue Mountain Trip` content as a Google Doc and keep updating it there.
- Keep `memory.md` as the canonical conversation log; `Blue Mountain Trip.md` may become a local mirror.

### OUTCOME — 2026-08-07 (Google Docs setup ABANDONED)
- User got stuck on the Google Cloud OAuth consent screen (new "Google Auth Platform" UI — test users live under `https://console.developers.google.com/auth/audience`, publishing status must be "Testing"). Could not get it working.
- **Decision:** User chose to continue with the LOCAL MARKDOWN FILE approach. Google Docs integration is dropped for now.
- Cleanup done: removed the `google-docs` MCP block from `~/.config/opencode/opencode.json` (config restored to original). Credentials file `~/.config/opencode/google-oauth.json` still exists on disk — user may delete it if not needed.
- **Blue Mountain Trip.md remains the FINAL planner** and will be maintained as markdown going forward.

### Planner content preferences (2026-08-07)
- User asked to REMOVE from `Blue Mountain Trip.md`: **Packing List, Notes & To-Do, and Driving / Logistics** sections (and their TOC entries). The planner should focus on: blog research, itinerary, accommodation, and photo spots/nature walks.
- Do not re-add those sections unless the user asks.

### Accommodation recommendations (2026-08-07)
- User asked for BnB or decent hotel with **private room + private bathroom**. Updated `Blue Mountain Trip.md` → Accommodation section with detailed options (source: Walk My World first-hand guide updated Apr 2026; My Katoomba cottages).
- **BnBs/cottages:** Rosebud Cottage (Katoomba, 2br/private bath, quiet, ~5 min walk to town), Leura Hideaway (Airbnb, private apt for 2, hot tub), Whispering Pines (Wentworth Falls), Foys Folly (Megalong Valley, remote/rural).
- **Hotels (en-suite):** Lilianfels (Katoomba, luxury), Parklands (Blackheath, quiet luxury), Hydro Majestic (Medlow Bath), Fairmont (Leura), Kyah (Blackheath boutique), Metropole (Katoomba budget), Blackheath Motor Inn (budget), Katoomba YHA (budget private en-suite).
- Note flagged: The Carrington (Katoomba) cheaper wing has a separate private bathroom, not attached — book ensuite if staying there.
