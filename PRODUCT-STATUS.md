# Elisio 365 — development status

This is the initial web application, not a finished app-store release.

## Implemented

- Responsive Uzbek interface with a black background and white text, country flags and profile customization.
- Server-stored profiles with unique usernames, first and last names, nicknames, bios and country choices.
- 120 portfolio variants: 10 layout families and 12 accent palettes. These are combinations, not 120 independently art-directed designs.
- Diary, projects, certificates, ideas and reading entries; editing and deletion.
- Server-enforced private, public, friends and family audiences. Groups are owner-managed access lists, not mutual friendship requests.
- R2 uploads linked to entries. Access to each file is checked against the entry's current audience. Supported formats: JPEG, PNG, WebP, GIF, MP4, WebM and PDF. Initial per-file limit 32 MB, six files per entry, 500 MB per user.
- Username search, profile links, likes and comments, comment deletion by its author or entry owner.
- Installation manifest and service worker for compatible Android/Windows browsers. Offline mode does not expose or cache private content; an internet connection is needed.
- JSON export of text/metadata; binary media is not included in that export.

## Required before a public release

- Direct Google and phone/SMS authentication: not connected. The current Sites platform uses ChatGPT authentication. Do not show SMS success, accept an unverified phone number as identity, or treat a client-supplied user ID as authentication.
- Appropriate public access configuration and a verified identity-provider integration before inviting users.
- Store packages, signing, store developer accounts, and Play/Microsoft review. No APK, AAB or MSIX has been generated or submitted.
- Account deletion, abuse reporting/blocking, moderation operations, retention policy, upload scanning, stronger rate limits and concurrency-safe storage quotas.
- Video transcoding, resumable large uploads, notifications and additional languages.
- Device and accessibility testing, load tests, backups and recovery tests. No guarantee of an error-free system is made.

The source of truth for user records is D1 and for media is R2. Browser storage is not used to persist user records. A private deployment's platform access rules still apply even to an entry marked public.

## Personal universe dashboard update — 2026-10-03

- Cosmic generated backdrop, dimensional monogram, subtle time-lapse and particles, responsive interactive section platforms; reduced-motion preference supported.
- Owner can reposition platforms using pointer drag or arrow keys, save to D1, cancel or restore defaults. Migration 0001 adds world_layout without replacing existing profiles.
- Real 14-day activity constellation derived from stored entries; no invented progress statistics.
- Header username search and portfolio navigation with shareable ?u=username URL.
- Journal modal has achievements, learned information and optional notes; composition preserves the existing entry storage and audience controls.
- Updated supplied 365 flag icon used in the sidebar, favicon and installation icons.
- Verified TypeScript, production build, journal roundtrip, and isolated integration checks including layout validation and owner isolation. Browser verified modal, search, portfolio URL and keyboard movement.
- This update is available in local preview. No successful online deployment is claimed.
