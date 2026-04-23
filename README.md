# TouchDown 
# Touchdown

Touchdown is a static frontend build for an international relocation tracker. The app guides users through onboarding, helps them manage relocation documents and tasks, and provides profile and privacy controls in a dashboard-style interface.

## What is included

This folder contains a production-ready frontend build:

- `index.html` bootstraps the app
- `assets/index-CRLi9VJE.js` contains the bundled JavaScript
- `assets/index-CVMP6SqA.css` contains the compiled styles

No source files, package manifest, or build configuration are included in this export, so this repository should be treated as a deployable static site rather than a development workspace.

## Inferred product features

Based on the shipped bundle, the app includes:

- authentication flows for login and registration
- an onboarding flow for relocation setup
- a dashboard for tracking relocation progress
- a documents area for managing relocation paperwork
- a profile area for personal information and move details
- privacy controls including data export and account deletion
- support for Google sign-in and email-based accounts

## Routes

The app uses hash-based routing. Main routes present in the bundle:

- `#/`
- `#/login`
- `#/register`
- `#/onboarding`
- `#/dashboard`
- `#/documents`
- `#/profile`

If no hash is present, the app defaults to `#/`.

## Local preview

Because this is a static build, you can preview it with any simple HTTP server.

### Python

```bash
python3 -m http.server 8000
