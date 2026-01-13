# Slackbrix

Slackbrix is a modular, enterprise-ready Slack app framework designed for **multi-organization distribution**, **Slack Enterprise Grid**, and **OAuth-based installs**. It provides a reusable foundation for building Slack apps that securely manage per-installation tokens and avoid hard-coded environment credentials.

This repository is intended as a **starter + reference implementation** for Slack apps that must scale across many Slack organizations.

---

## Key Features

- OAuth v2 installation flow using Slack Bolt + ExpressReceiver  
- Enterprise Grid–ready (supports org-wide installs)  
- Per-installation token storage (no global bot tokens)  
- Prisma-backed persistence for install metadata and tokens  
- Modular “install kit” designed for reuse across apps  
- One-click install entry point (within Slack’s admin constraints)

---

## Architecture Overview

Slackbrix is intentionally split into two concerns:

### Installation & Auth (`install-kit/`)
Responsible for:
- OAuth install and callback handling
- Installation persistence
- Token resolution per request
- Enterprise vs workspace install resolution

### App Logic (`index.js`)
Responsible for:
- Slack events, messages, and commands
- Using the Slack client injected by Bolt
- Automatically operating with the correct token per install

