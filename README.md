# Touchdown 

Touchdown is a relocation companion for people moving across borders. It is designed to make international moves feel less chaotic by bringing onboarding, relocation details, document management, and account controls into one guided experience.

This folder contains the production build of the frontend application. It is ready to be previewed locally or deployed to a static hosting platform.

## Overview

The shipped application appears to support the core journey of an international mover:

- create an account or sign in
- complete a relocation onboarding flow
- track move-related information such as destination, visa type, arrival date, and nationality
- manage relocation documents from a dedicated documents area
- review and update profile information
- control privacy settings, export data, and delete the account when needed

The app uses a dashboard-style interface and hash-based client-side routing, which makes it suitable for static hosting without server-side route handling.

## What’s in this folder

This export includes only compiled frontend assets:

- `index.html` - application entry point
- `assets/index-CRLi9VJE.js` - bundled JavaScript application code
- `assets/index-CVMP6SqA.css` - compiled stylesheet bundle

This export does **not** include:

- source React components
- `package.json`
- build scripts
- test files
- environment configuration
- backend services

That means this directory should be treated as a deployment artifact, not the original development repository.

## Core App Areas

Based on the bundled application, the main user-facing sections are:

### Authentication

Users can sign in or register through dedicated auth screens. The build also references both Google sign-in and email-based account access.

### Onboarding

New users are guided through a relocation setup flow that appears to capture move-specific details such as destination country, visa type, arrival date, and nationality.

### Dashboard

The dashboard acts as the central workspace for a user’s relocation journey and likely surfaces status, next steps, or move progress in a single view.

### Documents

The documents section is intended for relocation paperwork and document-related workflows, making it easier to keep required files in one place.

### Profile and Privacy

The profile area includes editable personal details, a move summary, data export, and account deletion controls, with privacy messaging built into the interface.

## Available Routes

The app bundle includes the following client routes:

- `#/`
- `#/login`
- `#/register`
- `#/onboarding`
- `#/dashboard`
- `#/documents`
- `#/profile`

If the URL does not contain a hash, the app automatically redirects to `#/`.

## Running Locally

Since this is a static build, you only need a simple local web server.

### Option 1: Python

```bash
python3 -m http.server 8000
