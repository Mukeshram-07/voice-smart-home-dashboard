# Voice Smart Home Dashboard

> A real-time, voice-controlled smart home interface with 3D room visualization, built with React, Three.js, and Firebase.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-voice--smart--home--muk.web.app-blue?style=flat-square)](https://voice-smart-home-muk.web.app)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react)](https://react.dev)
[![Firebase](https://img.shields.io/badge/Firebase-Firestore-FFCA28?style=flat-square&logo=firebase)](https://firebase.google.com)

---

## Overview

Voice Smart Home Dashboard lets you control home devices through natural language voice commands. Device states sync in real time via Firebase Firestore and are reflected immediately in an interactive 3D room built with React Three Fiber. A navigable character avatar, manual toggle controls, and a full command history round out the experience.

---

## Features

- **Voice Control** — Issue natural-language commands to toggle lights, fans, doors, and TV via the Web Speech API
- **3D Room Visualization** — Real-time interactive room rendered with Three.js and React Three Fiber
- **Real-Time Sync** — Device state persisted and broadcast via Firebase Firestore
- **Interactive Avatar** — Navigate the room with WASD / Arrow keys; sit on the sofa with Space or E
- **Manual Controls** — Side-panel toggles as a fallback for every device
- **Command History** — Timestamped log of all voice commands with status indicators
- **Responsive UI** — Glassmorphic design built with Tailwind CSS and animated with Framer Motion

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 19, TypeScript, Vite |
| 3D Graphics | Three.js, React Three Fiber, React Three Drei |
| Styling | Tailwind CSS, Framer Motion |
| Backend | Firebase — Firestore, Hosting |
| Voice | Web Speech API |

---

## Getting Started

### Prerequisites

- Node.js ≥ 18
- A Firebase project with Firestore enabled

### Installation

```bash
# Clone the repository
git clone https://github.com/Mukeshram-07/voice-smart-home-dashboard.git
cd voice-smart-home-dashboard

# Install dependencies
npm install

# Start the development server
npm run dev
```

---

## Firebase Configuration

1. Create a project at [console.firebase.google.com](https://console.firebase.google.com) and enable Firestore Database.
2. Copy your project credentials into `src/firebase.ts`:

```ts
// src/firebase.ts
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  // ...
};
```

3. Build and deploy:

```bash
npm run build
npx firebase-tools@latest deploy --only hosting
```

---

## Usage

### Voice Commands

| Device | Commands |
|---|---|
| Light | `turn on light` / `turn off light` |
| Fan | `fan on` / `fan off` |
| Door | `open door` / `close door` |
| TV | `turn on tv` / `turn off tv` |

### Keyboard & Mouse Controls

| Input | Action |
|---|---|
| Mouse drag | Orbit camera |
| Mouse scroll | Zoom |
| WASD / Arrow keys | Move avatar |
| Space / E (near sofa) | Sit / stand |

---

## Project Structure

```
src/
├── components/
│   ├── room/               # Three.js room and device components
│   ├── landing/            # Landing page components
│   ├── VoiceController.tsx # Web Speech API integration
│   └── CommandHistory.tsx  # Command log panel
├── hooks/                  # Custom React hooks
├── utils/                  # State reducers and command parsers
├── pages/                  # Top-level page components
├── firebase.ts             # Firebase initialisation and config
├── types.ts                # Shared TypeScript types
└── App.tsx                 # Root component
```

---

## Testing

```bash
# Run the test suite
npm test

# Run with coverage report
npm run test:coverage
```

---

## Contributing

Contributions are welcome. Please open an issue to discuss your proposed change before submitting a pull request.

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push and open a pull request

---

## License

Released under the [MIT License](LICENSE).

---

## Author

**Mukeshram** — [@Mukeshram-07](https://github.com/Mukeshram-07)
