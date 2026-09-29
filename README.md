# ⚔️ Black Desert Online — Slumbering Origin Enhancement Simulator
<img width="1299" height="911" alt="image" src="https://github.com/user-attachments/assets/a3643ea4-2087-4ad6-bf2f-dd55341ded94" />


An interactive, high-fidelity web simulator that accurately models the probabilistic mechanics, pity systems, and economic impact of enhancing endgame **Slumbering Origin (Fallen God)** equipment in *Black Desert Online*.

Built with vanilla JavaScript, HTML5 Canvas particle physics, Web Audio API procedural synthesis, and Tailwind CSS.

---

## 🌐 Live Interactive Demo

* **Live Web App:** https://izzatzulh.github.io/bdo-enhancement-simulator/index.html
* **GitHub Repository:** https://github.com/IzzatZulH/bdo-enhancement-simulator
* **Author / Developer:** Izzat Zul

The Slumbering Origin gear set represents the absolute pinnacle of gear progression in *Black Desert Online*. Because in-game enhancement attempts require billions of silver in resources and carry severe downgrade penalties, this simulator was engineered to provide players with a mathematically rigorous sandboxed environment to test failstack strategies, evaluate Cron Stone efficiency, and monitor long-term economic expenditure.

---

## ✨ Key Features

### 1. 🧮 Mathematically Precise Probability Engine
* **Tier-by-Tier Scaling:** Implements authentic base success rates and linear failstack scaling across all enhancement tiers (Base → PRI → DUO → TRI → TET → PEN).
* **Softcap Modeling:** Accurately switches scaling slopes beyond the official 340 Failstack (FS) softcap, simulating reduced marginal rate returns (an 80% drop in gain per stack) for extreme failstacks:

$$
\text{Success Rate} = 
\begin{cases} 
\text{Base Rate} + (\text{FS} \times \text{Gain}_{\text{base}}), & \text{if } \text{FS} \le 340 \\
\text{Rate}_{340} + ((\text{FS} - 340) \times \text{Gain}_{\text{post}}), & \text{if } \text{FS} > 340 
\end{cases}
$$

* **Agris Essence Pity System:** Full support for independent per-tier Agris Essence pools (12, 15, 20, 50, 1,000) guaranteeing 100% success upon hitting tier capacity.

### 2. ⚡ Autonomous Simulation & Smart Failstacking
* **Smart Tier FS Thresholds:** Configurable target failstacks per tier that dynamically assign appropriate stacks during automated testing.
* **Auto-Enhance Engine:** Asynchronous loop testing thousands of taps in seconds.
* **Blacksmith Repair Station:** Automatic durability recovery using Memory Fragments and Artisan's Memory when durability drops below the safety threshold (< 20).

### 3. 🎨 Immersive Visuals & Procedural Web Audio
* **HTML5 Canvas Particle Engine:** Custom multi-threaded `requestAnimationFrame` loop rendering atmospheric dark spirit smoke and rotating arcane rune overlays.
* **Zero-Dependency Web Audio Synthesizer:** Pure procedural audio synthesis via Web Audio API oscillators and gain envelopes for UI clicks, charge hums, chromatic victory chords, and deep failure rumbles.
* **Responsive Dark Fantasy UI:** Crafted with Tailwind CSS and Cinzel/Inter typography evoking authentic MMORPG interface aesthetics.

### 4. 📊 Economic Telemetry & History Analytics
* **Silver Expenditure Estimation:** Tracks real-time silver equivalent costs across raw taps, Cron Stones (3M silver/stone equivalent), and Memory Fragments.
* **Detailed Log & Audit Trail:** Searchable, filterable event log recording timestamps, target tier, failstacks, mathematical probability, protection status, and outcomes.

---

## 📋 Enhancement Mechanics Reference Table

| Target Level | In-Game Subtitle | Base Chance (0 FS) | Gain per FS (≤ 340) | Gain Post-Softcap (> 340) | Agris Essence Pity Cap | Base Cron Cost |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **PRI (I)** | Desperate | 2.00% | +0.20% | +0.04% | 12 | 1,500 |
| **DUO (II)** | Distorted | 1.00% | +0.10% | +0.02% | 15 | 2,100 |
| **TRI (III)** | Silent | 0.50% | +0.05% | +0.01% | 20 | 2,700 |
| **TET (IV)** | Wailing | 0.20% | +0.02% | +0.004% | 50 | 4,000 |
| **PEN (V)** | Obliterating | 0.00% | +0.01% | +0.002% | 1,000 | 35,000 |

---

## 🛠️ Tech Stack

* **Language:** JavaScript (ES6+), HTML5, CSS3
* **Graphics & Animation:** HTML5 2D Canvas API, CSS Keyframes
* **Audio Synthesis:** Web Audio API (`AudioContext`, `OscillatorNode`, `GainNode`)
* **Styling:** Tailwind CSS CDN, Google Fonts (Cinzel, Inter)

---

## 📬 Contact & Portfolio

* **Developer:** Izzat Zul
* **GitHub:** https://github.com/IzzatZulH
* **Email:** izzatzulh2000@gmail.com

