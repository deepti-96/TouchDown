# Touchdown

Touchdown is a static relocation-tracking web app for people managing international moves. This build brings onboarding, move details, checklist progress, document handling, and profile management into one guided experience.

This repository contains the shipped frontend artifact rather than the original source codebase. It works best as a deployable UI snapshot for demos, reviews, stakeholder walkthroughs, and lightweight static hosting.

## Best For

This artifact repository is especially useful when you need to:

- preview the current Touchdown UI quickly
- share a static build with reviewers or non-technical stakeholders
- deploy a simple hosted demo without rebuilding from source

## At a Glance

Touchdown currently presents a relocation workflow centered around:

- account registration and sign-in
- destination, visa, arrival-date, and nationality setup
- dashboard task tracking, search, and urgent-item visibility
- document upload, organization, and prep-sheet downloads
- profile management with pre-filled form data
- data export, local sign-out controls, and dark mode support

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

## Main App Areas

| Area | What it covers |
| --- | --- |
| Authentication | Login and registration flows with Google and email-oriented account paths |
| Onboarding | Destination country, visa type, arrival date, and nationality capture |
| Dashboard | Checklist progress, filtering, search, and urgent-task visibility |
| Documents | Prep sheets, document uploads, category organization, and downloads |
| Profile | Personal details, move summary tools, and profile-backed form prefill |
| Privacy | Data export and local-device sign-out controls |

## Routes

The bundled app currently exposes the following client routes.

| Route | Area |
| --- | --- |
| `#/` | Landing page |
| `#/login` | Login |
| `#/register` | Registration |
| `#/onboarding` | Relocation setup |
| `#/dashboard` | Progress dashboard |
| `#/documents` | Forms and document vault |
| `#/profile` | Profile and privacy tools |

If no hash route is present, the app redirects to `#/`.

## Deployment Notes

Touchdown can be deployed to any static hosting provider, including Netlify, Vercel, GitHub Pages, Cloudflare Pages, or S3-backed static hosting.

Deployment checklist:

1. Upload the repository contents as-is.
2. Serve `index.html` as the entry point.
3. Preserve the `assets/` directory structure.
4. Keep `favicon.svg` at the repository root.

Because routing is hash-based, additional SPA rewrite rules are generally not required.

## Repository Scope

This is not the original development repository. It should be treated as a reviewable frontend artifact and deployable product snapshot.

What is not included here:

- source React components
- build configuration
- test suites
- environment files
- backend services
- deployment automation

## Current Limitations

A few boundaries are important to call out clearly when sharing this repo:

- server-side account deletion is not available in this shipped build
- repository-level edits happen against compiled assets rather than source components
- deeper architecture details are not recoverable from this artifact alone
- validation and behavior changes should be treated as bundle-level patches, not full source maintenance

## Current Build Highlights

This snapshot already includes a number of usability and cleanup improvements, including:

- corrected Touchdown-branded export filenames
- improved favicon handling for static hosting
- improved mobile viewport behavior
- persistent dark mode with public and in-app theme toggles
- clearer sign-out and privacy messaging
- more reliable object-URL download flows
- stricter document upload validation and error handling
- dashboard search, filter feedback, urgent-task visibility, and richer status cues
- document vault search with filtered-result feedback and summary badges
- move summary, destination copy/download actions, and profile readiness indicators
- removal of stray injected markup and unused font imports from the app shell

## Maintenance Notes

When updating this artifact repo, the safest workflow is:

1. Make narrowly scoped edits.
2. Re-verify the shipped bundle after each change.
3. Keep README statements tied to behavior visible in the current build.
4. Avoid describing missing source code, backend behavior, or unreleased features as present.

## Suggested Next Step

For long-term maintainability, pair this frontend build with the original source repository so future documentation can cover the real stack, setup flow, environment variables, and deployment pipeline.
