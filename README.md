# Touchdown 

Touchdown is a relocation platform designed to simplify international moves. It brings onboarding, relocation planning, document organization, and account management into one experience so users can navigate a complex cross-border move with more clarity and less friction.

This repository currently contains the production-ready frontend build of the application. It can be previewed locally or deployed directly to any static hosting provider.

## Overview

International relocation usually involves scattered documents, deadlines, forms, and personal details spread across multiple tools. Touchdown is built to centralize that journey in one place.

From the shipped application, the product appears to support:

- user registration and sign-in
- relocation onboarding
- tracking move details such as destination, visa type, nationality, and arrival date
- document-related workflows
- profile and privacy management
- data export and account deletion

The app is structured as a client-side single-page application with hash-based routing, which makes it easy to host as a static site.

## Repository Contents

This project includes compiled frontend assets:

- `index.html` — application entry point
- `assets/index-CRLi9VJE.js` — bundled JavaScript application code
- `assets/index-CVMP6SqA.css` — compiled stylesheet bundle

## What Is Not Included

This is not the full source repository. It does not currently include:

- source React components
- build tooling
- test files
- environment configuration
- backend services
- deployment pipelines from the original app

Because of that, this repository should be treated primarily as a deployable frontend artifact rather than a full development workspace.

## Product Areas

### Authentication

The app includes dedicated login and registration flows, with references to both Google sign-in and email-based authentication.

### Onboarding

New users are guided through a relocation setup flow that appears to collect essential move context such as destination country, visa type, arrival date, and nationality.

### Dashboard

The dashboard acts as the central workspace for the relocation journey and likely helps users review progress, navigate the app, and keep track of what comes next.

### Documents

A dedicated documents area suggests support for organizing relocation paperwork and managing file-related tasks in one place.

### Profile and Privacy

The profile section includes editable personal details, move summaries, privacy messaging, data export, and account deletion controls.

## Routes

The bundle includes the following client-side routes:

- `#/`
- `#/login`
- `#/register`
- `#/onboarding`
- `#/dashboard`
- `#/documents`
- `#/profile`

If the app loads without a hash route, it redirects to `#/`.

## Running Locally

Since this is a static build, it can be previewed with any simple local server.

### Python

```bash
python3 -m http.server 8000
