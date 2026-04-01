# SKYWARN Operators Console

A Windows desktop application for aggregating, logging, and managing National Weather Service (NWS) weather alerts and spotter reports for emergency management and coordination.

## Overview

SKYWARN Operators Console is a an application designed for weather observers, emergency managers, and incident coordinators. It provides real-time NWS alert monitoring, incident logging, spotter report tracking, multi-format data export, and report generation — all in a single desktop tool.

## Features

- **Real-Time Alert Monitoring** — On-demand polling of the NWS API (no API key required) with state, office, or zone filtering; county-based coverage filtering with color-coded severity; alert acknowledgment and archive
- **Incident Management** — Create and manage incident logs with auto-sequenced incident numbers (`YYYY-###`), rich narrative editor, operator assignments, and timestamped notes
- **Spotter Reports** — Log detailed spotter reports (location, type, magnitude, damage, reporter callsign); format and copy reports as Slack or Skype messages
- **Audio Alerts** — Text-to-speech announcements for high-priority alerts (tornado, severe thunderstorm, flood) using Windows built-in speech synthesis
- **Data Export & Reporting** — CSV, plain text, and ICS-214 operational log exports; spotter report summary, incident report summary, and end-of-action report dialogs with print preview
- **Settings Editor** — Built-in graphical settings editor; no manual file editing required

## Requirements

- Windows 10 or later
- ~50 MB disk space
- No .NET runtime installation required (releases are self-contained)

## Download

Pre-built releases are published on the [**Releases**](https://github.com/wilmingtonohioskywarn/skywarn-operators-console/releases) page of this repository.

1. Go to [Releases](https://github.com/wilmingtonohioskywarn/skywarn-operators-console/releases) and download the latest `SkywarnIlnLogger-vX.X.X-win-x64.zip`.
2. Extract the zip to a folder of your choice.
3. Run `SkywarnIlnLogger.exe` — no additional installation required.

## Configuration

All settings are managed through the built-in **Settings** dialog (accessible from the menu bar). On first launch, `settings.json` is created in the application directory.

Key settings to configure before use:

| Setting            | Description                                                   |
| ------------------ | ------------------------------------------------------------- |
| Alert Scope        | Filter alerts by US State, NWS Office (e.g., `ILN`), or Zone  |
| Coverage Counties  | Comma-separated list of counties for your coverage area       |
| NWS Calling Entity | Your group name — included in the NWS API `User-Agent` header |
| Contact Email      | Contact email — required by NWS API usage guidelines          |
| Operators          | List of operator names and callsigns for dropdowns            |

## Troubleshooting

**Alerts not loading** — Verify network connectivity and confirm that NWS Calling Entity and Contact Email are set in Settings.

**Application won't start** — Verify you are on Windows 10 or later. If using a self-contained release, no .NET install is needed.

**Audio alerts not working** — Ensure system audio is functional and Windows Speech platform voices are installed.

**Export or print is blank** — Confirm there are records for the selected date range and that the Export Folder in Settings is writable.

## License

Copyright © 2024–2026 Dave Gordley (K8DEG). All rights reserved.

This software is proprietary freeware provided free of charge for personal, non-commercial, and amateur radio/emergency management use. Redistribution, modification, or commercial use is not permitted without written permission from the copyright holder.

## Support

For issues or questions, please [open an issue](https://github.com/wilmingtonohioskywarn/skywarn-operators-console/issues) on this repository.
