# Chronos Protocol: Story Edition

A immersive Windows 95-style cyberpunk hacking simulator built as a single HTML file. Players investigate Dr. Aris Thorne's disappearance, uncover a rogue satellite threat, and execute a daring EMP counterstrike within a 60-minute timer.

##  Gameplay Overview

Experience a fully functional retro OS interface where you:
- Navigate desktop icons (My Computer, Outlook Mail, MS-DOS Prompt, SatUplink)
- Explore file systems with hidden clues and password-protected folders
- Execute terminal commands like `ping` and `telnet` to hack remote servers
- Decrypt coordinates using a specialized decoder tool
- Align a satellite dish and broadcast an EMP to save the world

**Key Features:**
- Typewriter-effect boot sequence and story intro
- Realistic Win95 windows with drag, resize, and close functionality
- Achievement system with toast notifications
- Clippy-style hint assistant
- 60-minute countdown timer with mission HUD
- Audio feedback (requires `typeSound.wav` for typing SFX)

##  Mission Briefing

1. **Investigate Documents**: Search My Documents for initial clues about suspicious IP activity.
2. **Unlock System Logs**: Use IP from `encrypted_note.txt` (68.17.221.101).
3. **Network Recon**: Analyze `net_activity.log` for target IP (216.58.192.142).
4. **Terminal Hacking**: `ping` then `telnet` the IP; use 'chronos' as server password.
5. **Decrypt Coordinates**: Find decoder in Recycle Bin, use key from `config.sys` (1420).
6. **Satellite Alignment**: Azimuth 210°, Elevation 45° for 95%+ signal lock.
7. **Fire EMP**: Detonate charge to neutralize the satellite.

**Pro Tip**: Typing 'abort' on the remote server triggers failsafe with new encrypted file.

##  Quick Start

1. Save code as `chronos-protocol.html`
2. (Optional) Add `typeSound.wav` in same directory for typing sounds
3. Open in browser
4. Click to power on → Watch story → Click to boot → Play!

**Browser Compatibility**: Chrome/Firefox/Edge. Audio unlocks on first click (user gesture policy).

##  Technical Details

- **Single-file**: Pure vanilla JS/CSS/HTML (~1500 LOC)
- **State Management**: Global variables track progress (e.g., `systemLogsUnlocked`, `level4Complete`)
- **File System**: Simulated via JS object `files` with recursive folder navigation
- **Terminal**: Stateful command parser with ping/telnet simulation and remote shell
- **Uplink Mini-game**: Real-time sliders with signal strength calculation
- **Responsive**: Fullscreen desktop with taskbar and multi-window support

##  Secrets & Easter Eggs

- Clippy provides random hints: Click the paperclip 📎
- New emails arrive dynamically based on progress
- Multiple failure paths (wrong passwords, timer expiry, incomplete alignment)
- Achievement unlocks: HACKER, BLACK HAT, CRYPTOGRAPHER, SAVIOR

##  Customization

Edit these sections to mod the game:
- `storyLines` / `bootLines`: Change narrative
- `missions`: Update HUD objectives
- `files`: Add/remove clues or folders
- `emails`: Expand inbox story
- Timer: Adjust `timeLeft = 60 * 60` (seconds)

##  License

MIT License - Free to use, modify, and distribute. Credit appreciated!

##  Credits

- Built for interactive storytelling and retro computing enthusiasts
- Inspired by 90s point-and-click adventures and cyberpunk hacking sims
- Tested on modern browsers (2026)

**Playtime**: 15-45 minutes depending on puzzle-solving speed.

---

*\"REMEMBER: 'chronos' is the ultimate key\"*
