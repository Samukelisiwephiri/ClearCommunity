# ClearCommunity — Water Quality & Civic Response Prototype

ClearCommunity is a single-page prototype for presenting community water-safety information and municipal response workflows. It demonstrates separate community and municipal views for a Pretoria-focused water-monitoring concept.

> **Prototype notice:** This repository currently contains a front-end demo, not a production water-monitoring or emergency-alert service. Readings, alerts, node health, forecasts, valve actions, tickets, login flows, USSD interactions, and report data are simulated in the browser. Do not use this application to make real water-safety decisions. Follow current instructions from the City of Tshwane and relevant health authorities.

## Features

### Community portal

- Suburb status cards and high-level turbidity indicators using illustrative data.
- Incident reporting form and a local demo feed; submissions are not sent to municipal services.
- USSD menu simulation for `*120*2782#`; it is not connected to a mobile carrier.
- Boiling-time calculator and countdown, plus general safe-storage and infant-formula guidance.
- ClearScore neighborhood participation demo.
- Language selector for English, Afrikaans, isiZulu, and Sesotho.

Translations are manually authored in the prototype and have not been certified or reviewed by fluent public-health translators. Health guidance and translations require review by qualified local authorities before public use.

### Municipal console

- Demo badge-number format check; this is not identity verification or access control.
- Simulated telemetry stream and system-health indicators.
- Illustrative downstream flow/prediction display.
- Demo valve-isolation controls; these do not control physical equipment.
- Maintenance-ticket assignment workflow using in-page sample data.
- Printable sample report with a SHA-256 digest; it is not a verified SANS 241 compliance report.

## Technology

- HTML5 with inline CSS and JavaScript
- Tailwind CSS, Chart.js, Font Awesome, and Google Fonts loaded from CDNs

There is no gateway server, database, real sensor integration, authentication service, or hardware firmware in this repository.

## Run locally

1. Open `clearcommunity_platform.html` in a modern browser.
2. Allow network access if you want the externally hosted CSS, charting, icon, and font assets to load.
3. Select a portal. Use the community sign-in form or enter a municipal badge number matching the displayed format to explore the respective demo view.

The prototype does not verify or store community credentials. Municipal badge format validation is also only a client-side demonstration.

## Repository contents

```text
.
├── clearcommunity_platform.html   # Single-page application and demo logic
├── clearcommunity-logo.png        # Portal logo
└── README.md
```

## Safety and production considerations

- Dashboard readings and status labels are simulated and are not laboratory results or official safety certifications.
- Boiling guidance is general demo content; local public-health instructions take precedence. Boiling does not remove chemical contaminants.
- Do not connect demo controls to valves or other operational equipment without a properly engineered, secured, and independently validated control system.
- Before production deployment, implement server-side authentication and authorization, trusted telemetry ingestion, audited operator actions, data protection, accessibility and localization review, and validation by water-quality and public-health specialists.
