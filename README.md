# Shvasa Solo: AI self-workout app prototype

Clickable prototype of a self-workout AI app within Shvasa. It is a single HTML file (`index.html`) that shows the app inside a phone shell, with a side panel for controls, a flow map and design notes.

> **Status:** prototype for product review. Nothing here is production code or live data. "Shvasa Solo" is the working name in the file and is not confirmed. Values shown as `[in brackets]` in the prototype are placeholders that have not been confirmed.

## Open the prototype

- **Live (GitHub Pages):** https://pink-mind-space.github.io/AI-Self-workout-app/
- **Locally:** download `index.html` and open it in a browser. No build step or server is needed.

The file is about 2.8 MB because the workout videos are embedded in it, so it can load slowly on a mobile connection.

## What the prototype covers

The phone shell holds the app screens. The side panel has three tabs:

| Tab | What it does |
|---|---|
| **Controls** | Switch entry point (new user, invited user, existing live member), guest first or returning visit, Free or Full access tier, live-classes access, checkout region, platform and payment result, wearable day since sync and device signals, voice sound and speed, and simulate events (friend finishes a session, skip to next pose, finish session, phone call, screen lock) |
| **Flow map** | Jump straight to any screen or state, grouped into flows A to G (below) |
| **Notes** | Design decisions, placeholders and open questions for the screen currently shown |

### Flows in the flow map

- **A. First contact to first workout:** splash, welcome (first-time and returning guest), goal, time, welcome workout, first-workout badge and next step, invite landing, browse mode
- **B. Signup and weekly plan:** sign up, days a week, limitations, pod selection, connecting a device, permissions, stats before an account, plan build, weekly plan (Today)
- **C. Free habit loop:** Today, free session with call-outs, session complete, recap card, post-workout feedback, break check, Explain & Ask, wearable states (not synced, calibrating, week on week, partial and full data, basic report, EDA device picker, conflict resolution), benchmark and retest, challenges
- **D. Locked surface to paid plan:** the upgrade prompts (U1 to U9), checkout, checkout while not signed in, payment failed, invite friends instead
- **E. Post-upgrade tour:** payment confirmed and coach marks
- **F. Switching between apps:** the buy-access prompt and the live app
- **G. Engagement (full access):** friends on Today, practising now, small wins after a session, badges, community feed, posts and comments, reactions, threads, group conversation, leaderboard, friends and quest partner, share with a deep link, shared-workout landing, home-screen widget

### Workout structure in the prototype

- Durations: 5, 10, 15 and 20 minutes.
- A 5-minute block is 5 poses of 1 minute each. A 1-minute **Break** sits between blocks (a placeholder video is used for the break).
- The break asks whether the workout is too hard, just right or too easy, and later blocks adapt to the answer.
- Player states covered: exit with save and resume, partial credit, phone call, screen lock, headphone change and video failure.
- The **welcome workout** is a one-time, full-experience session that sits outside the free and paid caps. It uses the AI-generated placeholder videos.

### Pods (workout styles) in the prototype

Flexibility, Strength, Calm & Meditation, Dance Fitness, Vinyasa, Hatha and Restorative. The library has six pre-designed workouts (5, 10, 15 and 20 minutes). There are no custom workouts and no mini-courses in this version.

### Wearables

Connecting a device goes through a single permissions page. After sync there is a 3-day calibration period, then week-on-week comparison. The full report is free to day 14 and then reverts to a basic report on the free tier.

## Not built in this prototype

- Streak protection (on hold).
- Hindi (removed for now).
- Custom workouts and pre-recorded mini-courses (removed).
- Real video generation, payments, notifications, calendar writes and wearable syncing. These are simulated screens only.

## Related document

The product requirements are in the separate **Shvasa AI Rebuild PRD** (PDF). It is not stored in this repo. At the time of writing its welcome-workout section is out of date compared with this prototype, and the prototype takes precedence.

## Updating

Edit `index.html` in place and push to `main`. GitHub Pages serves the root of `main`, so the live link updates after the next build.
