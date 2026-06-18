# Demo Video Script

A scene-by-scene script for the submission demo video (with voiceover). **SHOW** =
on-screen action, **SAY** = voiceover. Target length ~5 minutes; a tighter ~3-minute
cut is at the bottom.

## Pre-recording checklist

- Run `npm run seed` so missions are freshly **in-progress** (drones visibly flying).
- Open the **deployed Vercel link** in a clean/incognito window (not localhost).
- Have one mission **mid-flight** on the monitor before starting.
- Close other tabs; browser zoom 100%; mute notifications.
- Optional: keep DevTools device-mode ready for the mobile segment.

---

## Full cut (~5 min)

### Scene 1 — Intro & framing (0:00–0:30)

**SHOW:** Overview page (`/`), global ops map with drones moving.

**SAY:** "Hi, I'm Vaibhav. This is my Drone Survey Management System for the FlytBase
challenge — a platform for large organizations to plan, monitor, and report autonomous
drone surveys across multiple global sites. Data capture and video are out of scope, so
I focused on the operational backbone: mission management, real-time monitoring, fleet
coordination, and reporting. It's built with Next.js, TypeScript, and Supabase, and it's
deployed live on Vercel."

### Scene 2 — The core design idea (0:30–1:00)

**SHOW:** Stay on the ops map; point at two moving drones at different sites.

**SAY:** "Since real drones are out of scope, telemetry is simulated — but the key design
decision is that it's deterministic. A mission's live position, progress, and battery are
a pure function of its start time and flight path stored in the database. That means
there's no central simulation loop — it runs perfectly on serverless, every viewer
computes the exact same state, and it scales to any number of concurrent missions. Here
you can see multiple drones flying across different sites at once, each tracked
independently."

### Scene 3 — Mission Planning (1:00–2:15)

**SHOW:** Mission Planner → New mission. Name it. Pick a site. Use the search bar to jump
to a location. Click to draw a polygon. Drag a vertex.

**SAY:** "Let's plan a mission. I'll name it, pick a site — and I can search any location
on Earth to plan anywhere. I draw the survey area by clicking vertices directly on the
map, and I can drag any point to reshape it."

**SHOW:** Toggle patterns Crosshatch → Perimeter → Parallel, watching the path redraw.
Adjust altitude and overlap sliders; watch waypoints/coverage/duration update live.

**SAY:** "Now the survey pattern. These aren't just labels — each is a real
path-generation algorithm. Crosshatch is a double perpendicular sweep for maximum detail;
perimeter traces the boundary; parallel is a single sweep. Line spacing is computed from
the sensor's footprint, altitude, and overlap percentage — so as I raise altitude or
overlap, the path regenerates and you can see coverage, distance, and estimated duration
update in real time."

**SHOW:** Switch to No-fly zone mode, draw a zone over the path → launch-blocking warning
appears. Move it off → warning clears. Save the mission.

**SAY:** "For safety, I added geofencing. If I draw a no-fly zone that the flight path
crosses, the system detects the intersection and blocks launch until the route is clear.
There's also an endurance check that warns if a mission exceeds the assigned drone's
battery range. Then I save the mission."

### Scene 4 — Real-time Monitoring (2:15–3:20)

**SHOW:** Live Monitor. Animated drone gliding along the path; telemetry panel.

**SAY:** "Once launched, the mission appears on the live monitor. The drone animates
smoothly along its flight path, and the telemetry panel shows progress percentage,
estimated time remaining, live battery drain, heading, and distance covered — all
recomputed every second."

**SHOW:** Pause → progress freezes. Resume → continues. Abort → confirmation → confirm.

**SAY:** "I have full mission control. Pause freezes the simulation clock exactly — watch
the progress hold. Resume picks up precisely where it left off, with no lost progress.
And abort safely stops the mission and releases the drone back to the fleet, behind a
confirmation step. All of these are real database state changes — and because of Supabase
Realtime, if a second operator had this open, they'd see every change instantly."

_(Optional: open the same mission in a second window and pause in one to show live sync.)_

### Scene 5 — Fleet Dashboard (3:20–3:55)

**SHOW:** Fleet page. Point at an in-mission drone with live draining battery; show
statuses and vitals.

**SAY:** "The fleet dashboard gives an organization-wide view of every drone across all
sites — real-time status like available, in-mission, or charging, plus battery, cruise
speed, endurance, and lifetime flight stats. For drones currently flying, the battery
here is live — it matches the draining value on the monitor, not a static number."

### Scene 6 — Reporting & Analytics (3:55–4:25)

**SHOW:** Reports page. KPI cards, missions-by-site bar chart, status pie, completed
survey table.

**SAY:** "Finally, the reporting portal. At the top, org-wide stats — total surveys,
distance flown, area surveyed, total flight time. Below that, missions broken down by
site and by status, and a per-flight report table with duration, distance, and coverage
for every completed survey. Completed missions are reconciled automatically — even with
no one watching — so these numbers are always accurate."

### Scene 7 — Engineering & AI (4:25–5:00)

**SHOW:** Resize window / DevTools device mode to show the mobile drawer + stacked layout;
optionally flash the tests folder, CI, or AI_USAGE.md.

**SAY:** "A few things under the hood: the app is fully responsive — here's the mobile
layout with a slide-in nav. The domain logic — pattern generation, simulation, analytics
— is covered by a unit-test suite running in GitHub Actions CI. And I built this
end-to-end with Claude Code, using it to commit to the deterministic-simulation
architecture up front and to keep tight build-and-verify loops — there's an AI_USAGE doc
detailing exactly how. Thanks for watching."

---

## Tight cut (~3 min)

For a shorter video, keep Scenes 1, 3, and 4 in full and compress the rest:

1. **Intro (0:00–0:25):** Scene 1 voiceover, trimmed to the first three sentences, over
   the ops map. Add one line: "telemetry is deterministically simulated, so it scales to
   many concurrent missions on serverless."
2. **Planning (0:25–1:30):** Scene 3 — draw area, switch crosshatch/perimeter, adjust one
   slider, draw a no-fly zone to trigger the block, save.
3. **Monitoring (1:30–2:25):** Scene 4 — animated drone + telemetry, then pause / resume /
   abort.
4. **Fleet + Reports (2:25–2:50):** One sentence each while showing the page — live fleet
   battery, then the reports KPIs and charts.
5. **Close (2:50–3:00):** "Built with Next.js, Supabase, and Claude Code, fully tested and
   deployed on Vercel. Thanks for watching."

## Delivery tips

- Talk to the design decisions, not just the clicks — the deterministic simulation,
  geofencing, and auto-reconciliation are the differentiators.
- ~150 words/minute is a comfortable pace; keep energy up.
- Record one take per scene; clarity beats polish.
