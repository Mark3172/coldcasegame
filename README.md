# THE COLD FILE
> *An internal corporate mystery & deduction game disguised as a sleek log-analysis tool.*

## Overview
**THE COLD FILE** is a 100% turn-based deduction web game where you step into the shoes of an internal SecOps threat intelligence analyst. A serious corporate crime has taken place (IP exfiltration, wire fraud, liquid cooling sabotage, or root cryptographic key theft). You must cross-reference keycard badge swipes, intercepted employee chat snippets, and network telemetry logs to find the culprit.

At a glance from 5 feet away, the UI looks like an authentic enterprise APM / SIEM monitoring console (Datadog / Grafana / Sentinel).

---

## Key Features

### 1. 100% Turn-Based Core Mechanics (Zero Timers)
- **Zero Real-Time Timers:** Take as long as you want. Nothing occurs until you take an action.
- **Action Points (AP):** Start each case with 8 AP (expandable to 10 via upgrades).
  - Basic profile reviews, reading unredacted logs, switching tabs: **0 AP (Free)**
  - Forensic Deep Scan on log entries: **1 AP**
  - Tactical Gadget deployment: **1 AP**
- **Full State Auto-Save:** Every action automatically persists to `localStorage`. You can close the tab or reload at any second and resume seamlessly.

### 2. Procedural Case Generator & Contradiction Engine
- **Infinite Procedural Replayability:** Every case generates a unique crime archetype, 4 suspects with distinct departments, roles, access levels, employee badges, and stated alibis.
- **The Contradiction Engine:**
  - The actual culprit **MUST have 2 subtle, decisive contradictions** between their stated Alibi and the Evidence Streams (e.g. keycard location mismatch, rogue encrypted socket, or unauthorized network exfiltration authenticated by their token).
  - Innocent suspects have 0 or 1 red herring that is cleared upon deep scan or interrogation.

### 3. Tactical Retro-Tech Detective Gadgets
1. **Signal Tracker:** Pinpoints a suspect's actual room location at the incident timestamp via campus Wi-Fi & RFID trilateration, testing against their stated alibi.
2. **Voice Modulator (Interrogate):** Opens an encrypted VoIP interrogation channel with 3 tactical vectors (Alibi integrity, Motive/Finances, Technical token anomalies), measuring real-time stress and extracting psychological slips.
3. **Packet Decryptor:** Uses a retro matrix decipher subroutine to unscramble `[REDACTED]` hashes, tokens, and payloads in evidence logs.

### 4. Surprise Plot Twists ("Live Leaks")
Every time 2–3 AP are spent, a high-priority intercept alert triggers:
- **Cover-Up Attempt:** A conspirator runs a log-shredding script. Spend 1 AP to intercept and salvage smoking-gun evidence, or let it burn.
- **Encrypted Drive Cracked:** Forensics cluster decrypts an SSD sector, verifying an innocent suspect's alibi.
- **Anonymous Whistleblower:** A classified PGP drop gives a critical hint about the culprit's department or security clearance level.

### 5. Emergency "Boss Key" (`[SYS_MODE]` or `Escape`)
- Press **Escape** or click **`[SYS_MODE]`** in the top right at any moment.
- The screen instantly swaps to a realistic, mundane **Grafana SRE Kubernetes Cluster Monitoring Dashboard** complete with simulated p50/p95/p99 latency graphs, pod health tables, and Envoy access logs.
- Press **Escape** again to return seamlessly to your investigation state.

### 6. Built-in Web Audio API Synthesizer
- Generates retro-tech clicks, radar sonar pings, packet decrypt audio chatter, alert sirens, and verification fanfare directly in the browser—with zero external audio files. Includes a one-click mute toggle.

---

## How to Play

### Quick Start (Double-Click or Local Server)
1. **Option A (Direct File):** Simply open `index.html` in any modern web browser (Google Chrome, Microsoft Edge, Brave, Firefox).
2. **Option B (Dev Server):**
   ```bash
   npm start
   # or
   node server.js
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser.

### Investigation Steps
1. Read the **Case Briefing** ticker at the top to note the critical incident window (e.g., `22:00 - 22:30`) and the compromised asset.
2. Review the **4 Suspect Dossiers** on the left. Pay close attention to their **Stated Alibis**.
3. Browse the **3 Evidence Streams** on the right:
   - **Keycard Logs:** Look for entries inside the restricted crime scene.
   - **Intercepted Chats:** Look for suspicious communications or decrypt `[REDACTED]` tokens.
   - **Network Traces:** Look for high-volume exfiltration from static workstation IPs.
4. Use **Deep Scan (1 AP)** on suspicious entries to reveal forensic metadata and verify contradictions.
5. Deploy **Tactical Gadgets (1 AP)** if you need to confirm room locations or pressure suspects.
6. Once you've identified the culprit and their 2 contradictions, click **LOCK IN ACCUSATION SHOWDOWN** to convict them and earn XP, Creds, and Detective Rank promotions!
