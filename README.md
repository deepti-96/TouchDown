# Touchdown

Touchdown is a relocation platform for people managing international moves. It brings onboarding, move details, document handling, and profile management into one guided experience so users can stay organized through a complex cross-border process.

This repository currently contains the production frontend build of the app rather than the original source codebase.

## What Touchdown Does

From the shipped app bundle, Touchdown appears to support:

- account registration and sign-in
- relocation onboarding
- destination, visa, arrival-date, and nationality tracking
- document upload and download workflows
- profile management with form pre-fill data
- data export
- privacy and sign-out controls

The app uses hash-based client-side routing, so it can be hosted as a static single-page application.

## What’s In This Repository

The project currently includes compiled frontend assets:

- `index.html` — application entry point
- `assets/index-CRLi9VJE.js` — bundled JavaScript application code
- `assets/index-CVMP6SqA.css` — compiled stylesheet bundle
- `favicon.svg` — checked-in favicon asset

## What’s Missing

This is not the original development repository. It does not currently include:

- source React components
- build configuration
- test suites
- environment files
- backend services
- deployment automation

Because of that, this repo should be treated primarily as a deployable frontend artifact and reviewable product snapshot.

## Main App Areas

### Authentication

Touchdown includes dedicated login and registration flows, with support references for both Google and email-based accounts.

### Onboarding

Users are guided through a relocation setup flow that captures key move context such as destination country, visa type, arrival date, and nationality.

### Dashboard

The dashboard acts as the central navigation and status area for the relocation journey.

### Documents

The documents area provides:

- fillable preparation guides
- uploaded document management
- category-based document organization
- file download and deletion actions

### Profile and Privacy

The profile area includes editable personal information, move summaries, and privacy tools such as data export and sign-out.

## Important Product Note

This shipped build does **not** currently support server-side account deletion.

The privacy flow in this repo supports:

- exporting user data as JSON
- signing out on the current device

It should not be described as permanently deleting server-side records unless the underlying backend is updated to support that behavior.

## Routes

The bundled app includes these client routes:

- `#/`
- `#/login`
- `#/register`
- `#/onboarding`
- `#/dashboard`
- `#/documents`
- `#/profile`

If no hash route is present, the app redirects to `#/`.

## Running Locally

Because this is a static build, you can preview it with a simple local server.

### Python

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

## Deployment

Touchdown can be deployed to any static hosting provider, including:

- Netlify
- Vercel
- GitHub Pages
- Cloudflare Pages
- Amazon S3 + CloudFront

Deployment notes:

1. Upload the repository contents as-is.
2. Serve `index.html` as the entry point.
3. Preserve the `assets/` directory structure.
4. Keep external font access available if you want the shipped typography to render correctly.

Because routing is hash-based, additional SPA rewrite rules are generally not required.

## Current Build Notes

Recent fixes in this repository include:

- corrected Touchdown-branded export filenames
- improved favicon handling for static hosting
- improved mobile viewport behavior
- clearer sign-out and privacy messaging
- more reliable object-URL download flows
- stricter document upload validation and better document error handling

## Best Use For This Repo

This repository is well suited for:

- product review
- stakeholder demos
- static deployment
- UI inspection

It is less suited for:

- feature development from source
- dependency management
- running meaningful automated tests
- rebuilding the application from source

## Suggested Next Step

For long-term maintainability, pair this frontend build with the original source repository so this README can document the real stack, setup process, environment variables, build workflow, and backend dependencies.
