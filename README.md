# TN BusConnect

[![License: MIT](https://img.shields.io/badge/License-MIT-0D6B4E.svg)](./LICENSE)
[![Live Demo](https://img.shields.io/badge/Live-Netlify-00C7B7.svg)](https://tn-bus-connect.netlify.app)

An open-source, daylight-readable civic-tech web app unifying **Tamil Nadu's 8 state transport corporations** (MTC, SETC, and 6 TNSTC divisions) into one commuter-first interface.

- **Live App:** https://tn-bus-connect.netlify.app
- **Repository:** https://github.com/maniraja5599/tn-bus-connect

## Key Features
- **District → From → To → Reverse (`⇅`):** Pick any district (Namakkal, Salem, Trichy, Chennai, Madurai, Coimbatore, Tirunelveli, Vellore) and search both within-district town buses and inter-district express/SETC routes with instant return direction (`⇅`).
- **Vetri Payanam (`₹0`) Filter:** 1-tap filter to spot eligible ordinary town buses.
- **QR-Ready Stand Departure Boards:** Deep-link directly to stand boards (e.g. `#stand=namakkal`).
- **Open Community Data (`data/districts.json`):** Clean JSON dataset separated from UI so anyone can add routes or districts via Pull Request.

## Project Structure
```text
├── index.html                  # Light-first mobile PWA UI
├── data/
│   └── districts.json          # All district stops, 70+ routes & stand boards
├── netlify.toml                # Netlify static publish config
├── CONTRIBUTING.md             # How to add bus timings or districts
├── LICENSE                     # MIT License
└── .github/ISSUE_TEMPLATE/     # Non-coder bus timing submission forms
```

## Contributing
Want to add your town's bus timings or fix a via-stop?
- **No coding needed:** Open an Issue using the **[Add or Fix Bus Timing](../../issues/new?template=add-bus-timing.yml)** template.
- **Developers:** Edit `data/districts.json` and open a Pull Request. See [CONTRIBUTING.md](./CONTRIBUTING.md) for the exact JSON schema.

Initiated by **Mani Raja** ([@manirajannm](https://x.com/manirajannm)).
