# 🆘 ReliefLink – Disaster Coordination Hub

A web platform where **citizens, volunteers and authorities** coordinate during a disaster: requests, resource offers and official updates in one place.

**Live demo:** https://warm-smakager-34ec55.netlify.app

## Problem

Disaster response is often slowed by poor coordination between citizens reporting needs, volunteers offering help and authorities managing resources. ReliefLink brings all three groups into one shared view.

## Features

**Three roles (switch at the top of the page)**

| Role | What they can do |
|---|---|
| Citizen | Post help requests (type, urgency, location pinned on the map), report missing people, check shelters and alerts |
| Volunteer | Take open requests ("I can help"), publish resource offers, update shelter supplies |
| Authority | Broadcast Emergency/Warning/Info alerts, resolve or remove requests, register shelters, manage records |

**Platform**

- **Dashboard** with live counts, urgent needs, recent activity and a one-tap situation report to copy into WhatsApp, SMS or email
- **Help requests** with urgency sorting, search and filters, and a status flow: Open → Assigned → Resolved
- **Volunteer offers** (food, transport, medical aid and more) with contact numbers
- **Live map** with pins for requests (coloured by urgency), volunteer offers and relief camps, a flood zone, nearest camp and volunteer with distance, plus approximate GPS coordinates
- **City picker, GPS button and world map** with a demo incident feed
- **Shelters** with capacity bars, check-in/check-out and food, water and medical supply status
- **Missing persons registry** with search and a "Mark found" action
- **Official updates** broadcast by authorities
- **Emergency contacts, safety tips and an interactive go-bag checklist**
- **SOS button** that jumps to a critical-priority request form
- **Edit** any request, offer or alert after posting
- **Relo, a 3D guide robot** with context-aware tips, a guided tour and optional voice
- Animated disaster-themed hero and a natural night-landscape background

## Tech stack

- Single-file app: HTML, CSS and vanilla JavaScript (no build step)
- [three.js](https://threejs.org/) (r128, loaded from cdnjs) for the 3D guide
- Hand-drawn SVG city and world maps
- Browser `localStorage` for data

## Run locally

Open `index.html` in any modern browser. An internet connection is needed only for the 3D guide; without it the guide falls back to an emoji.

## Deploy

Drag the folder onto [Netlify Drop](https://app.netlify.com/drop), or enable **GitHub Pages** (Settings → Pages → Deploy from branch → `main` / root).

## Limitations

- Data is saved in each visitor's own browser, so users do not see each other's entries. A real deployment would need a shared backend and database.
- The city map is a schematic demo city. Coordinates are approximate and anchored to the selected city.
- Incident and shelter data are demo data. SMS and email alerts are not included.

## Roadmap

- Shared backend (real-time sync between citizens, volunteers and authorities)
- Real map tiles (OpenStreetMap) and live GPS pins
- SMS/email alerts and multi-language support
- Volunteer skills registration and hospital resource sharing
- Role-based login for authorities

## License

MIT, see [LICENSE](LICENSE).
