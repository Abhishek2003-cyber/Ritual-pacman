# 🎮 RITUAL PACMAN — On-Chain Retro AI Arcade

> **A fully on-chain, browser-based retro arcade game powered by Ritual Network — where classic Pac-Man meets Web3 AI infrastructure.**

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Vercel-black?style=for-the-badge)](https://ritual-pacman.vercel.app)
[![GitHub](https://img.shields.io/badge/GitHub-Ritual--Pacman-181717?style=for-the-badge&logo=github)](https://github.com/Abhishek2003-cyber/Ritual-pacman)
[![Ritual Network](https://img.shields.io/badge/Chain-Ritual_Network-00ff88?style=for-the-badge)](https://ritual.net)

---

## 📌 Overview

**RITUAL PACMAN** is a Web3-native retro arcade experience that combines the timeless gameplay of Pac-Man with the power of the **Ritual decentralized AI network**. Players navigate a cryptographic maze as **JOSH**, an AI node operator, while evading four intelligent ghost characters — each representing a distinct threat model in the Ritual ecosystem.

Every completed game session records the player's score **on-chain** to the **Ritual Testnet** via a MetaMask-signed transaction, contributing to a live, transparent leaderboard — making every high score a verifiable blockchain event.

---

## ✨ Key Features

### 🕹️ Gameplay
- Classic Pac-Man maze rendered on **HTML5 Canvas** (21×22 grid)
- **4 AI-powered ghost agents** with unique behavioral modes: Ambush, Chase, Chaos, and Scatter
- **Power Pellets** trigger Scared Mode — ghosts become vulnerable for a limited time
- **3-life system** with progressive difficulty across 5 levels

### 🔗 Web3 & Blockchain
- **MetaMask wallet integration** with one-click connect
- **Ritual Network auto-configuration** (Chain ID: 1979) — auto-adds the network if not present
- **On-chain score submission** — game scores are encoded and sent as `eth_sendTransaction` payloads using **Ritual Testnet tokens**
- **Live transaction status tracking** — mining progress, tx hash, and confirmation displayed in real-time
- **Sandbox mode** — fully playable without a wallet using a simulated environment

### 📊 Leaderboard
- Scores are stored and ranked in a **persistent on-chain leaderboard**
- Auto-opens after game-over with transaction confirmation
- Player wallet addresses displayed with score rankings

### 🎨 Design & UX
- **Green neon cyberpunk theme** — inspired by Ritual Network's brand identity (`#00ff88`)
- **Looping background video** with intelligent local-first loading and online CDN fallback
- **CSS animated cyber-grid** as a graceful background fallback
- **Web Audio API synthesizer** — fully offline retro sound effects (no audio files needed)
- **Ritual Network Level Map** — cryptographic node progression visualizer
- **Character preview cards** on the start screen showcasing all 5 characters

### 🎭 Characters
| Character | Role | Behavior |
|---|---|---|
| 🟡 **JOSH** | Player — AI Node Operator | User-controlled |
| 🔴 **BITTY** | Ghost — Ambush Agent | Targets player's predicted position |
| 🩷 **RITTY** | Ghost — Chaos Agent | Random pathfinding |
| 🔵 **RITUALIST** | Ghost — Chase Agent | Direct pursuit AI |
| 🟠 **RADIENT** | Ghost — Scatter Agent | Corner-pinning strategy |

### 🏆 Level Progression
| Level | Name | Ghost Speed | Scared Duration |
|---|---|---|---|
| 1 | Genesis Node | 1.8 px/frame | 8 seconds |
| 2 | Inference Engine | 2.1 px/frame | 6.5 seconds |
| 3 | Cryptographic Maze | 2.4 px/frame | 5 seconds |
| 4 | Consensus Breach | 2.7 px/frame | 3.5 seconds |
| 5 | Sovereign AI | 3.0 px/frame | 2 seconds |

---

## 🛠️ Technical Architecture

```
┌─────────────────────────────────────────────────────┐
│                  RITUAL PACMAN                       │
│                  (Single HTML File)                  │
├──────────────┬──────────────────┬───────────────────┤
│  Game Engine │   UI / Styling   │   Web3 Layer      │
│              │                  │                   │
│ HTML5 Canvas │  Vanilla CSS     │  window.ethereum  │
│ Game Loop    │  CSS Variables   │  MetaMask EIP-1193│
│ BFS Pathfind │  Neon Animations │  Ritual Chain RPC │
│ Collision    │  Web Audio API   │  eth_sendTx       │
│ AI Behaviors │  CSS Grid Bg     │  Leaderboard      │
└──────────────┴──────────────────┴───────────────────┘
```

### Stack
- **Frontend**: Pure HTML5, Vanilla CSS, Vanilla JavaScript — zero dependencies, zero build tools
- **Rendering**: HTML5 Canvas API
- **Audio**: Web Audio API (procedural synthesis — fully offline)
- **Blockchain**: `window.ethereum` (EIP-1193 provider — MetaMask compatible)
- **Network**: Ritual Network EVM Testnet (Chain ID: 1979)

---

## 🔗 Ritual Network Configuration

| Parameter | Value |
|---|---|
| Network Name | Ritual |
| Chain ID | `1979` |
| RPC URL | `https://rpc.ritualfoundation.org` |
| Block Explorer | `https://explorer.ritualfoundation.org` |
| Native Currency | `RITUAL` |

---

## 🚀 Getting Started

### Play Instantly
Open the live deployment on Vercel — no installation required.

### Run Locally
```bash
# Clone the repository
git clone https://github.com/Abhishek2003-cyber/Ritual-pacman.git
cd Ritual-pacman

# Serve locally (any static server works)
npx serve .
# or
python -m http.server 8080

# Open in browser
http://localhost:8080
```

### Connect & Play
1. Open the game in your browser
2. Click **"CONNECT WALLET"** to link MetaMask (Ritual Testnet)
3. The game auto-configures the Ritual Network in MetaMask
4. Click **"START GAME"** and play!
5. On game over, your score is automatically submitted on-chain

> **No wallet?** Click **"CONNECT WALLET"** → choose **Sandbox Mode** to play with a simulated wallet.

---

## 📁 Project Structure

```
ritual-pacman/
├── index.html          # Complete game (HTML + CSS + JS)
├── josh.png            # Player character (JOSH)
├── bitty.png           # Ghost character (BITTY)
├── ritty.svg           # Ghost character (RITTY)
├── ritualist.png       # Ghost character (RITUALIST)
├── radient.svg         # Ghost character (RADIENT)
├── ritual-logo.jpg     # Ritual Network official logo
├── background.mp4      # Cyberpunk ambient background video
└── .gitignore          # Git configuration
```

---

## 🌟 Why RITUAL PACMAN?

RITUAL PACMAN demonstrates that **blockchain integration doesn't have to be complex or heavy**. With a single HTML file and no external libraries:

- It connects to a **real EVM blockchain** (Ritual Network)
- It submits **verifiable on-chain transactions**
- It delivers a **complete, polished gaming experience**
- It showcases **Ritual Network** to a new audience through fun, accessible gameplay

This project proves that **Web3 can be simple, fast, and fun** — and that the Ritual Network is a capable platform for consumer-facing on-chain applications.

---

## 👨‍💻 Built By

**Abhishek** — Web3 Developer & Game Builder
- GitHub: [@Abhishek2003-cyber](https://github.com/Abhishek2003-cyber)

---

*Built with ❤️ on Ritual Network — Decentralized AI Infrastructure*
