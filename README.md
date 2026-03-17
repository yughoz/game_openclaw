# 🎮 Agent Colony - Multi-Agent Dashboard

Game-style dashboard untuk monitoring multi-agent OpenClaw system.

## 🌐 Live Demo

**URL:** http://89.21.85.164:19001

## ✨ Features

- 🎮 **Game-style UI** - Pixel art aesthetic dengan animasi
- 📊 **Real-time monitoring** - Status update setiap 3 detik
- 🏢 **Zone-based visualization**:
  - 💼 Work Area - Agent yang sedang bekerja
  - ☕ Rest Area - Agent yang idle
  - 👥 Collaboration - Agent yang kolaborasi
  - 🐛 Debug Zone - Agent yang error
  - 📋 Task Queue - Daftar task pending
  - 🎮 Orchestrator - Clawtron sebagai coordinator
- 🎭 **Animated agents** - Karakter bergerak sesuai status
- 💬 **Tooltips** - Info detail saat hover
- 📈 **HUD Stats** - Active, Idle, Tasks, Done

## 🔧 Configuration

Edit `CONFIG` in `index.html`:

```javascript
const CONFIG = {
    starOfficeUrl: 'http://89.21.85.164:19000',
    refreshInterval: 3000,
    agents: {
        'Clawtron': { emoji: '🍄', color: '#ff6b6b', role: 'Orchestrator' },
        'Flashclaw': { emoji: '⚡', color: '#feca57', role: 'Server Agent' },
    }
};
```

## 🚀 Deployment

```bash
# Quick start
python3 -m http.server 19001
```

## 📁 File Structure

```
game_openclaw/
├── index.html      # Single-file dashboard
└── README.md       # Documentation
```

## 🔌 API Requirements

Dashboard connects to Star Office UI API:
- `GET /agents` - List all agents with status
- CORS enabled required

---

*Part of the OpenClaw Multi-Agent Ecosystem*
