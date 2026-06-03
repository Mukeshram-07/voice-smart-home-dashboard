# 🏠 Voice Smart Home Dashboard

A voice-controlled smart home dashboard built with React, TypeScript, Three.js, and Firebase. Control your home devices using natural voice commands and see them react in a beautiful 3D room visualization.

## ✨ Features

- 🎤 **Voice Control** — Control lights, fans, doors, and TV using natural voice commands
- 🎨 **3D Room Visualization** — Interactive 3D room built with Three.js/React Three Fiber
- 🔥 **Firebase Integration** — Real-time device state sync with Firestore
- 🚶 **Interactive Person Avatar** — Move around the room with WASD/Arrow keys, sit on the sofa
- 📊 **Command History** — Track all voice commands with status indicators
- 🌐 **Responsive UI** — Modern, glassmorphic design with Tailwind CSS

## 🚀 Live Demo

**Live App:** https://voice-smart-home-muk.web.app

## 🛠️ Tech Stack

- **Frontend:** React 19, TypeScript, Vite
- **3D Graphics:** Three.js, React Three Fiber, React Three Drei
- **Styling:** Tailwind CSS
- **Animation:** Framer Motion
- **Backend:** Firebase (Firestore, Hosting)
- **Voice Recognition:** Web Speech API

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/Mukeshram-07/voice-smart-home-dashboard.git
cd voice-smart-home-dashboard

# Install dependencies
npm install

# Run development server
npm run dev
```

## 🎮 Usage

### Voice Commands

- **Light:** "turn on light" / "turn off light"
- **Fan:** "fan on" / "fan off"
- **Door:** "open door" / "close door"
- **TV:** "turn on tv" / "turn off tv"

### Controls

- 🖱️ **Mouse:** Drag to orbit camera, scroll to zoom
- ⌨️ **Keyboard:** 
  - WASD / Arrow keys to move person
  - Space / E to sit on sofa (when near)
- 🎛️ **Manual Toggles:** Use the side panel switches

## 🔥 Firebase Setup

1. Create a Firebase project at [console.firebase.google.com](https://console.firebase.google.com)
2. Enable Firestore Database
3. Copy your Firebase config to `src/firebase.ts`
4. Deploy:
   ```bash
   npm run build
   npx firebase-tools@latest deploy --only hosting
   ```

## 🧪 Testing

```bash
# Run tests
npm test

# Run tests with coverage
npm run test:coverage
```

## 📁 Project Structure

```
src/
├── components/          # React components
│   ├── room/           # 3D room components
│   ├── landing/        # Landing page components
│   ├── VoiceController.tsx
│   ├── CommandHistory.tsx
│   └── ...
├── hooks/              # Custom React hooks
├── utils/              # Utilities (reducers, parsers)
├── pages/              # Page components
├── firebase.ts         # Firebase configuration
├── types.ts            # TypeScript type definitions
└── App.tsx             # Main application component
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

MIT License - feel free to use this project for learning or building your own smart home dashboard.

## 👤 Author

**Mukeshram**
- GitHub: [@Mukeshram-07](https://github.com/Mukeshram-07)

---

Built with ❤️ using React, Three.js, and Firebase
