# Hospital Dashboard

## Overview

A responsive clinical-operations dashboard for census, bed utilization, emergency wait time, live patient acuity, unit capacity, and outpatient schedules.

## Features

Asynchronous snapshot loading, operational metrics, filterable patient board, acuity badges, capacity visualization, appointment statuses, responsive clinical navigation, loading placeholders, and accessible controls.

## Technology Stack

React 19, TypeScript 7, Vite 8, Lucide icons, Testing Library, Vitest 5, Nginx, and Docker.

## Requirements / Installation

Install Node.js 24+ and npm 11+, then run `npm install`.

## Environment Variables

Set the public `VITE_API_BASE_URL` from `.env.example`; never expose clinical secrets or privileged tokens through Vite variables.

## Database Setup

The runnable demonstration uses a mock service at `src/services/clinicalApi.ts` and has no local database.

## Running the Application

Run `npm run dev`; run `npm run build` for a production bundle.

## Running Tests

Run `npm run check`. Tests cover snapshot loading, clinical-unit filtering, and schedule presentation.

## Default Development Accounts

The UI uses the fictional development persona Dr. Jordan Lee. Authentication is delegated to a real clinical backend.

## API Endpoints

A production integration should expose authorized, minimum-necessary census, patient-board, capacity, and schedule resources beneath `VITE_API_BASE_URL`.

## Folder Structure

`components` contains patient/schedule views, `services` is the mock API boundary, `types` defines safe view models, and `tests` contains interaction tests.

## Security Notes

All displayed records are fictional and React escapes content. The browser must never be the authorization boundary: a HIPAA/GDPR-aware backend must enforce identity, role and care-team access, minimum-necessary fields, audit access, encryption, short sessions, and safe caching. Avoid embedding protected health information in URLs, logs, or analytics.

## Known Limitations

This is not a medical device. It omits orders, medication administration, live EHR integration, alerts escalation, clinical decision support, and real patient data.

## License

MIT
