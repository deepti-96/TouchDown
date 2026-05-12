# Touchdown

Touchdown is a static relocation-tracking web app for people managing international moves. This build brings onboarding, move details, checklist progress, document handling, and profile management into one guided experience.

This repository contains the shipped frontend artifact rather than the original source codebase. It works best as a deployable UI snapshot for demos, reviews, and lightweight static hosting.

## At a Glance

Touchdown currently presents a relocation workflow centered around:

- account registration and sign-in
- destination, visa, arrival-date, and nationality setup
- dashboard task tracking and search
- document upload, organization, and prep-sheet downloads
- profile management with pre-filled form data
- data export and local sign-out controls

The app uses hash-based client-side routing, so it can be hosted as a static single-page application without extra rewrite complexity.

## Product Flow

1. Create an account or sign in.
2. Complete onboarding with move details.
3. Review dashboard progress and urgent tasks.
4. Prepare forms and manage uploaded files.
5. Maintain personal data from the profile area.

## Quick Preview

Because this repository is already a compiled static build, you can preview it locally with a simple file server.

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000/](http://localhost:8000/).

## Repository Contents

The repository intentionally stays small and tracks just the shipped app shell plus minimal repo metadata.

| Path | Purpose |
| --- | --- |
| `index.html` | Static application entry point |
| `assets/index-CRLi9VJE.js` | Bundled JavaScript application code |
| `assets/index-CVMP6SqA.css` | Compiled stylesheet bundle |
| `favicon.svg` | Checked-in favicon asset |
| `.gitignore` | Local-environment cleanup rules |

## Repository Scope

This is not the original development repository. It should be treated as a reviewable frontend artifact and deployable product snapshot.

What is not included here:

- source React components
- build configuration
- test suites
- environment files
- backend services
- deployment automation
