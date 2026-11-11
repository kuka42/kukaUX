# KNS Tablet – Player Guide

## What is it?

**KNS (Kuka Neighbouring System)** is a field tablet for Arma Reforger. Take it out of your inventory and you get a small computer in your hands, running its own system, **kukaUX**.

With the tablet you can:

- **watch your teammates' helmet cams** (KNS) – live view from their perspective,
- open a **map** right on the tablet, follow yourself or a teammate,
- **scan for drones** and look through their cameras (AIRCRACK),
- check **players, stats, weather, events, vehicles and health**,
- place your own **CCTV camera** and watch it from up to 300 m,
- **take photos** with the tablet camera,
- play small games (yes it kinda runs it), hunt bugs with **BugGO**, listen to sounds, take notes,
- and type commands in a **terminal**, just like on a real computer.

Everything happens on your screen only – other players don't see what you do on your tablet.

---

## Getting started

| Action | Default key |
|---|---|
| Take out / put away the tablet | **Ctrl + M** |
| Take out the tablet straight into the terminal, ready to type | **Ctrl + Alt + T** |
| Toggle input in the terminal | **ENTER** |
| Tablet actions (map, camera, list…) | **F** on the tablet |
| Screen brightness | **scroll** on the tablet button |
| Volume of KNS sounds / radio | **F + scroll** on the tablet button (Volume / Radio volume action) |
| Back / close a program | **ESC** |

All keys can be changed in **Settings → Controls → KUKA**.

The first time you switch the tablet on in a life, it boots up – give it a second.

**The tablet remembers where you were.** If you put it away (e.g. to sprint) and take it out again, the map, AIRCRACK, the KNS camera, LIST, STATS, STATUS and BugGO come back exactly as you left them. Other programs return to the terminal.

---

## Main screens

### KNS – helmet cameras
Live view from a teammate's camera. Your own faction only.
- **Ctrl + I / Ctrl + Y** – next / previous camera
- **Ctrl + U** – full screen and back
- No camera available → *NO SIGNAL* (it keeps trying).

### MAP
The game map on your tablet.
- **Num 8/4/6/2** – move, **+ / -** – zoom, **Num 5** – center on you
- **Hold Num 5** – follow (auto-center)
- `map <id>` in the terminal – map on a teammate, following him
- Opening the big map (M) switches the tablet off.
- Saved map options (type them in the terminal):
  - `map autocenter on` / `off` – the map starts following you right away
  - `map height <m>` – starting zoom (e.g. `map height 800`)
  - `map marker on` / `off` – your own arrow on the map
  - `map marker size 1` / `2` / `3` – arrow size
  - `map marker color black` / `blue` / `red` / `other` – arrow color

### LIST, STATS, STATUS
- **LIST** – players by faction: kills, deaths, teamkills, score.
- **STATS** – your stats for this session and in total (time, distance, kills, deaths, taxi distance, caught bugs, best game scores…).
- **STATUS** – time, wind, weather and a log of events.

TIP:  use **Num 8 / Num 2** to scroll.

### AIRCRACK
Scans for drones nearby and connects to their cameras. **Ctrl + I / Ctrl + Y** switch between drones.

### kukaOS screen
The **kukaUX** button switches between the terminal and the kukaOS screen. From kukaOS you get quick actions: **Manual, BugGO, CPTR (game), Camera, Selfie**. It also shows time, your FPS, server FPS and ping.

---

## Taxi

Need a ride, or want to drive for your team? The tablet has a taxi service – for **your own faction** only.

### Calling a taxi
- `taxi` – call a taxi to where you stand. Drivers on duty get your call with a sound and see you on their map.
- `taxi cancel` – cancel your call (or the ride).
- While a taxi is coming, you see it on your tablet map.
- After a call or a cancel you have to wait a moment before calling again.

### Working as a driver
- `taxi start` – go on duty (confirm with `taxi start yes`), `taxi stop` – off duty.
- `taxi list` – opens the **TAXI** app:
  - **Num 8 / Num 2** – select a call, **Enter** – take it
  - **Num 5** – show the call on the map (**ESC** back to TAXI)
- `taxi take <id>` – take a call by the player ID.
- During a ride the TAXI app shows **map**, **taxi done** and **taxi cancel** – select with **Num 8 / Num 2**, confirm with **Enter**.

### The ride
- It starts when you get within **3 m** of the client, or when they get into your vehicle.
- `taxi done` – finish the ride at the destination.
- It also ends by itself when you and the passenger are **100 m apart for 30 s** (they got out and walked away).
- Finished rides add the distance you drove to **TAXI** in **STATS**.

### Good to know
- Max **5 drivers on duty** per faction.
- Drivers go **off duty when they die**. If a driver dies or leaves before picking you up, your call goes back to the other drivers.
- `taxi start` cancels your own waiting call.
- `taxi help` – a short summary in the terminal.

---

## Terminal

The heart of the tablet.

- **Enter** – start typing, **Enter** – run the command, **ESC** – stop typing
- **ESC** in the terminal (when not typing) – switches the tablet off
- **Arrow keys** – last commands, **Tab** – complete a command
- `help` – list of commands, `<command> help` – what it does (e.g. `map help`)
- **Num 8 / Num 2** – scroll the history

### Useful commands

**Navigation and info**
- `map`, `kns`, `list`, `stats`, `status`, `aircrack` – open the screens above
- `kns <id>`, `map <id>` – a specific teammate; `players` / `ids` – player IDs
- `health`, `h <id>` – your body or a teammate's: health in %, blood, consciousness, bleeding
- `taxi` – call a taxi (or work as a driver - see **Taxi** section)
- `where <id>` – distance and direction to a teammate
- `gps` / `me` – your grid position, `az <x> <y>` – distance and direction to a grid (e.g. `az 0482 1135`)
- `compass` / `c` – the direction you are facing
- `obd` – your vehicle: engine, rpm, gear, speed, fuel, damage
- `scanner` / `scan` – deployed radios nearby (rough distance and direction)
- `material` / `mat` – what the surface you look at is made of (ballistics, up to 5 m)
- `origin` / `ori` – which mod the object you look at comes from (up to 5 m)

**Server and connection**
- `net` – server name, server FPS, your FPS, ping, packet loss
- `fps`, `ping`, `ip`, `server` / `host`, `id` (your name and player ID), `mods` (server mod list)

**Camera and CCTV**
- `camera` – back camera; **hold Num 5** to take a photo
- `selfie` – front camera (mirrored)
- `camera list` – your saved photos (folder `profile/KNS/screenshots`)
- `cctv set [height] [direction]` – place your CCTV camera here, `cctv` – connect (up to 300 m), `cctv off` – remove. One camera, gone when you die.

**Fun**
- `buggo` – a bug hides nearby; find it with **BugGO** (kukaOS) or `buggo cam` and catch it with **Enter**. Caught bugs count in STATS – some are very rare…
- `cptr` – fly a copter through a tunnel (**Num 8 / Num 2**), best flight in STATS
- `hell` – ASCII HELL shooter (PC only), best time in STATS
- `player list`, `player <name>`, `player next / prev / stop` – sounds that keep playing in the background; `volume 0-100`
- `video list`, `video <name>` – short videos (PC only)
- `dice`, `dice 20`, `coin`, `armahints`
- `wiki <word>` – the start of a Wikipedia article (PC only, asks for permission the first time)
- `radio` – radio stations: `radio <n>`, `radio next`, `radio list`, `radio off`, `radio vol 0-100` (needs the Project Sonar mod on the server)

**Other**
- `log` – notifications, players joining / leaving, killfeed and kukaUX messages with real time
- `print <text>` – write your name, position, time and text to the STATUS log; `save` – export STATUS and terminal logs to a file
- `kpad` – new note, `kpad list` – saved notes, `kpad <n>` – open one (inside a note: Enter new line, `:q` or ESC exit)
- `theme` – terminal colors (some are locked)
- `clear` – clear the terminal history, `run <program>` – same as typing the program
- `qr` / `kukaux` – the kukaOS screen
- `exit` / `off` – switch the tablet off

---

## Quick shortcuts

You don't have to type full commands – these short ones do the same:

| Type | Instead of |
|---|---|
| `l` | list (players by faction) |
| `m` | map |
| `s` | stats |
| `st` | status |
| `ac` | aircrack |
| `h` | health |
| `id` | your own ID |
| `ids` | player IDs |
| `cm` | camera |
| `c` | compass |

Tip: start typing and press **Tab** – the tablet completes the command for you.

Reminder: Use the arrow keys to cycle through recent commands.

---

## Good to know

- The tablet works only **in your hands** – put it away and it switches off (and remembers where you were).
- KNS cameras, map following and health of other players work only for **your own faction**.
- Some features are **PC only** (photos, files, videos, HELL, Wikipedia) – on consoles you'll see *"This is PC-exclusive feature."*
- Settings (brightness, volume, map options, theme…) are saved on your PC in `profile/KNS/`.
- Not sure about a command? Type it with `help`, e.g. `cctv help`. Or open the **Manual** on the kukaOS screen.

Have fun! – *kukaUX, made by kuka*
