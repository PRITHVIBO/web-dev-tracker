# StackForge — Web Development Tracker

A no-build, single-page web app for tracking web projects across different technology stacks.

## Run locally

1. Download or clone this folder.
2. Open `index.html` in a modern browser.
3. Your progress is saved in that browser's local storage.
4. To use the live GitHub finder, keep an internet connection available. The core tracker and saved progress still work offline.

No package installation, server, API key, or build step is required for the core tracker.

## Features

- 411 starter entries: 250 practice briefs and 161 real repository references with GitHub links and project/live-site links.
- **Live GitHub project finder:** choose any of the 25 stack presets (including MERN, MEAN, MEVN, PERN, LAMP, Laravel, Django, Flask, FastAPI, Spring Boot, ASP.NET Core, Rails, Next.js, SvelteKit, WordPress, Astro, AWS Serverless, Go + React, NestJS, Firebase, GraphQL, and Vue + Supabase) and search up to **250 public repositories per search**.
- Stack-aware repository queries, optional search keywords, result filtering, star/fork counts, last-push dates, direct source repository links, and maintainer-provided homepage/demo links when available.
- Add discovered repositories to your tracker with one click, then record your own GitHub repository and live deployment URL separately.
- Create, edit, delete, filter, search, and sort projects.
- Track difficulty, status, priority, progress, target date, and notes.
- Export the filtered catalog to CSV and back up/restore all project data as JSON.
- Responsive layout for desktop, tablet, and mobile.

## Important notes about live project discovery

The GitHub finder queries GitHub's public Search API at run time; it does **not** bundle 6,250 static links in the download. Up to 250 real public repositories are fetched for the selected stack when you search, which keeps the starter download small and lets the repository list reflect current public GitHub data. Results are keyword/README-based matches, not a guarantee that every repository uses every technology in the selected stack. Review the README, dependencies, license, last activity, security posture, deployment steps, and project suitability before cloning or adapting a repository.

A **Live demo** link is shown only when the repository maintainer has listed a homepage. Some projects do not publish a public demo, may require accounts or local setup, or may have a homepage that is no longer active. No demo URL is invented when one is missing.

The finder uses anonymous public API requests. GitHub may temporarily rate-limit repeated searches; when that happens, wait a while or use the **Open query on GitHub** link. Results are cached in the current page session for 15 minutes to reduce repeated requests.

## Persistence and backup

The app stores projects only in browser local storage on the device where you open it. The data is not automatically synced between browsers or devices. Use **Backup** to download a JSON backup and **Import** to restore it in another browser.

## Hosting on GitHub Pages

1. Create a GitHub repository.
2. Upload `index.html` and `README.md` to its root. Include `real-project-references.json` if you want to keep the standalone reference dataset alongside the app.
3. Open **Settings → Pages**.
4. Under build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. Open the published Pages URL. The live GitHub finder requires a browser with internet access.

## Project discovery sources

- [GitHub repository search](https://github.com/search?type=repositories)
- [roadmap.sh project ideas](https://roadmap.sh/projects)
- [roadmap.sh frontend projects](https://roadmap.sh/frontend/projects)
- [Florin Pop's App Ideas](https://github.com/florinpop17/app-ideas)
- [Project Based Learning](https://github.com/practical-tutorials/project-based-learning)
- [RealWorld cross-stack example app](https://github.com/gothinkster/realworld)
- [MERN Project Ideas](https://github.com/king04aman/MERN-Project-Ideas)
- [Developer Roadmaps](https://roadmap.sh/roadmaps/)

In the tracker, the **Existing repo + live link** filter shows saved real repositories. Use the GitHub finder to discover more and add the ones you want to recreate. For a selected repository, open its README and setup instructions first, then build your own version in a separate repository and attach your own repo/demo URLs in the tracker.
