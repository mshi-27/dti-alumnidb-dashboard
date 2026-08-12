# AlumniDB Dashboard

A full-stack alumni management dashboard built for Cornell Digital Tech & Innovation. It replaces a manual CSV-and-bulk-upload workflow with a self-service interface for creating, editing, and maintaining alumni records.

> **Demo note:** The recorded demo uses fictional data. Production source code, configuration, and data are private because this is an internal Cornell tool.

## Demo

<!-- Add a 20–45 second GIF or video link here. -->
<img width="1110" height="720" alt="Screen Recording 2026-08-11 at 10 10 27 PM" src="https://github.com/user-attachments/assets/86bab267-f81e-47f8-90ce-f5ae1d7384bb" />





## What it does

- Lets 20+ team administrators create and update records for 100+ alumni without engineering support
- Provides typeahead location search across 40+ known locations
- Ranks location suggestions by prior usage and geocodes new natural-language locations with Nominatim
- Supports image upload with instant local previews
- Avoids abandoned storage writes and removes replaced images after a successful save

## Tech stack

- **Frontend:** React, TypeScript, Semantic UI
- **Backend/data:** Node.js, Firebase, Firestore
- **Integrations:** Nominatim geocoding API

## Engineering highlights

### Replacing a manual operational workflow

Previously, even a one-record change required editing a CSV file and rerunning a bulk-upload script. The dashboard makes those updates directly accessible to authorized administrators.

### Consistent location data

The location workflow surfaces existing locations before querying Nominatim for unfamiliar entries. This helps standardize records and reduce duplicate variants such as “NYC” and “New York City.”

### Safer image storage

Images are previewed locally before upload. Storage writes occur only after confirmation, and the prior image is removed only after its replacement has saved successfully.

## My contribution

I built the alumni-management dashboard, location-assignment workflow, and image-upload flow as a Software Engineer at Cornell Digital Tech & Innovation.

## Availability

This repository is a portfolio case study. The production application and source code are private because they contain internal workflows and data.
