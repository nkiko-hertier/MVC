# 🧠 SYNAPSE — Test Version 1 (MVP)

> Goal: Build a lightweight, mock-data-driven version of SYNAPSE to test core features like relationship tracking, map visualization, and real-time feed analysis — without any backend.




---

🚀 MVP Overview

This version is designed to be simple, local-only, and focused on visual + interactive components.

We’re building:

✅ Clickable Graph View

✅ Map Tracking of fake GPS locations

✅ A Live Social Feed with risky word detection

✅ Basic Role-Based Access Control


All data is mocked and stored locally. No API or database required.


---

📦 Tech Stack

Feature	Tech Used

UI	React.js + Tailwind CSS
Relationship Graph	Cytoscape.js
Map Visualization	Leaflet.js
Live Feed + State	React Context or Zustand
Alerts	react-toastify


Install with:

npm install react react-dom cytoscape leaflet tailwindcss react-toastify


---

🗺️ Features Breakdown

1. 🔹 Landing Page

Simple navbar

Description of features

Buttons to navigate to:

Graph View

Map View

Social Feed View




---

2. 🧩 Clickable Relationship Graph

Tech: Cytoscape.js + React

Visualize 6–8 fake people/devices

Clicking a node highlights direct connections

Tooltips show:

Shared IP/device

Communication frequency



Goal: Visualize a basic web of connections.


---

3. 📍 Map View (Simulated GPS Tracking)

Tech: Leaflet.js + React

Show a city map

Simulate 2–3 phones moving across the map

Zones:

🟢 Green = Safe

🔴 Red = Alert zone



Goal: Simulate how location tracking looks visually.


---

4. 📢 Live Social Feed (Mocked)

Tech: React + Zustand or Context API

Scrolling fake messages

Flag “risky” keywords (e.g., bomb, riot, attack)

Display toast alert when a risky word is detected


Goal: Mimic real-time alerts from social posts.


---

5. 👥 Role-Based Access

Dropdown to select:

Analyst

Supervisor


Example effect:

Analyst: Hide “Export Data” button

Supervisor: Full access



Goal: Simulate role-based access control (RBAC).


---

🧪 Mock Data

graphData.json
```json
{
  "nodes": [
    { "data": { "id": "A", "label": "Alice" } },
    { "data": { "id": "B", "label": "Bob" } }
  ],
  "edges": [
    { "data": { "source": "A", "target": "B", "label": "Shared IP" } }
  ]
}

```
---

fakePosts.js
```js
export const fakePosts = [
  { id: 1, user: "user123", content: "We are planning a peaceful protest." },
  { id: 2, user: "anon567", content: "Let's bomb the system!" }, // <-- flagged
  { id: 3, user: "observer", content: "Interesting times ahead." }
];

```
---

🗂️ Project File Structure
```bash
synapse-mvp/
├── public/
│   └── index.html
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── GraphView.jsx
│   │   ├── MapView.jsx
│   │   ├── SocialFeed.jsx
│   │   └── RoleSelector.jsx
│   ├── data/
│   │   ├── fakePosts.js
│   │   └── graphData.json
│   ├── App.jsx
│   ├── main.jsx
│   └── styles.css
├── tailwind.config.js
├── package.json
└── README.md

```
---

📌 Tips for Development

Use Tailwind for styling fast components.

Cytoscape layouts can be tweaked with presets like cose, circle, or grid.

Simulate map movement using setInterval + marker updates.

Use react-toastify to show real-time alerts in the social feed.



---
