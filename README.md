# KNS Tablet – Player Guide

## What is it?

**KNS (Kuka Neighbouring System)** is a field tablet for Arma Reforger. Take it out of your inventory and you get a small computer in your hands, running its own system, **kukaUX**.

With the tablet you can:

- **watch your teammates' helmet cams** (KNS) – live view from their perspective,
- open a **map** right on the tablet, follow yourself or a teammate,
- **scan for drones** and look through their cameras (AIRCRACK),
- check **players, stats, weather, events, vehicles and health**,
- **call other players** by voice and join shared voice channels,
- **call a taxi** or work as a driver for your team,
- place your own **CCTV camera** and watch it from up to 300 m,
- **take photos** with the tablet camera,
- play games (yes it kinda runs it) – **BATTLE** against other players, **BLOX**, **HANGMAN**, **MOTO**, **FPV**, **DREAM**, even a **CHIP-8 emulator** – hunt bugs with **BugGO**, listen to sounds, take notes,
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

**The tablet remembers where you were.** If you put it away (e.g. to sprint) and take it out again, the map, AIRCRACK, the KNS camera, LIST, STATS, STATUS, SCANNER, TAXI, PHONE and BugGO come back exactly as you left them. Other programs return to the terminal. A BATTLE game keeps going in the background – type `battle` to get back to it.

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
- **LIST** – players by faction: kills, deaths, score.
- **STATS** – your stats for this session and in total: time, distance, kills, deaths, taxi distance, caught bugs, BATTLE wins and your best game scores (CPTR flight, HELL, BLOX, MOTO, FPV).
- **STATUS** – time, wind, weather, your deployment time (with the whole scenario time in brackets) and a log of events.

TIP:  use **Num 8 / Num 2** to scroll.

### AIRCRACK
Scans for drones nearby and connects to their cameras. **Ctrl + I / Ctrl + Y** switch between drones.

### LIDAR
`lidar` – the world in front of you drawn from laser rays, in ASCII, up to 200 m. **ESC** back. PC only.

### kukaOS screen
The **kukaUX** button (or `kukaux` in the terminal) switches between the terminal and the kukaOS screen. It shows your FPS, server FPS and ping, the time, day and date.

At the bottom there is a bar of quick actions (**F** on the icon):
- **Phone** – the PHONE app (who you can call); during a call it becomes **Hang up**
- **Camera**, **Selfie** – tablet cameras
- **Taxi** – calls a taxi; if you are a driver on duty, it opens your taxi calls
- **BugGO**, **CPTR** (copter game)
- **Manual**

### Themes and wallpapers
- `theme` – terminal colors, `wallpaper` – backgrounds of the kukaOS screen. Both list what you have; `theme green` / `wallpaper mucha` switches (saved).
- Some are **locked**. Catch a very rare **StackOverflow** with BugGO and type `stackoverflow` – it unlocks a random theme or wallpaper you don't have yet.

---

## Phone & channels

Talk to other players through your tablet – voice, any distance, without a radio.

### Who can call you
Before your first call, choose who can reach you (saved):
- `phone off` – nobody, your phone is off
- `phone faction` – your own faction only
- `phone all` – everyone, enemies too

`phone` shows your current setting.

### Calling
- `phone list` (or the **Phone** icon on the kukaOS screen) – the **PHONE** app with everyone you can call right now: **Num 8 / Num 2** – select, **Enter** – call.
- `call <id>` – call a player directly (IDs: `players` / `ids`). Your screen shows **Calling NAME..** – **ESC** cancels.
- The other player hears a ring and sees **NAME calling..**:
  - **Enter** – answer, **ESC** – decline
  - or type `answer` / `decline`
- If the tablet is put away, it rings anyway – take it out (**Ctrl + M**) and the call screen is there.
- No answer in 30 s and the call ends.

### During a call
- Your **microphone is on all the time** – just talk, like on a phone.
- The tablet works as usual (map, KNS, terminal…), the call keeps going.
- Your normal radio / voice keys still work – after you release them, you're back on the call.
- `hangup` (or **Hang up** on the kukaOS screen) – end the call. It also ends when one of you dies, leaves the server or loses the tablet.
- If someone can't be reached, you only see *not available* – you never know why.

### Shared channels
A voice channel for a whole group – everyone on the same number hears each other.
- `channel <1-9999>` – join a channel
- `channel talk` – microphone on / off (any voice key turns it off)
- `channel off` – leave
- `channel` – which channel you're on

Channels and phone calls never mix – nobody on a channel can listen to a call. While you're on a channel, others can't call you; `call` takes you off the channel first.

### Good to know
- Calling the same player again after a decline or no answer needs a short wait.
- `call help`, `channel help` – a short summary in the terminal.

---

## Taxi

Need a ride, or want to drive for your team? The tablet has a taxi service – for **your own faction** only.

### Calling a taxi
- `taxi` (or the **Taxi** icon on the kukaOS screen) – call a taxi to where you stand. Drivers on duty get your call with a sound and see you on their map.
- `taxi cancel` – cancel your call (or the ride).
- While a taxi is coming, you see it on your tablet map.
- After a call or a cancel you have to wait a moment before calling again.

### Working as a driver
- `taxi start` – go on duty (confirm with `taxi start yes`), `taxi stop` – off duty.
- `taxi list` (or the **Taxi** icon on the kukaOS screen while on duty) – opens the **TAXI** app:
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

## Games

`games` (or `help games`) lists them all. `<name> help` gives a short summary in the terminal. **ESC** always takes you back.

### BATTLE – battleships against other players
Classic battleships, played over the server against another player – or against the tablet.
- `battle <id>` – invite a player (IDs: `players` / `ids`), `battle quit` – cancel the invite
- The invited player sees the invite in the terminal: `battle accept` or `battle decline`
- `battle cpu` – play against the tablet
- **Num 5** – new random fleet, **Enter** – ready, then **Num 8/2/4/6** aim and **Enter** fire
- **ESC** hides the game – it keeps going in the background, even if you die. `battle` brings it back; the terminal tells you when it's your turn.
- `battle quit` – end the game (leaving the server ends it too)
- Who can invite you (saved): `battle off` – nobody, `battle faction` – your faction only (default), `battle all` – everyone, enemies too. `battle settings` shows it.
- Wins against other players count as **BATTLE WINS** in STATS.

### BLOX – falling blocks
`blox` – **Num 4/6** move, **Num 8** rotate, **Num 2** faster, **Num 5** drop. Full rows disappear, the game gets faster. Best score in STATS.

### HANGMAN
`hangman` – guess the word letter by letter. **Num 4/6** choose a letter, **Num 8/2** other row, **Enter** or **Num 5** guess. 7 mistakes and you hang.

### MOTO – motorcycle trial (PC only)
`moto` – ride a track high above a valley, first-person, to the finish gate. **Num 8** gas, **Num 2** brake / reverse, **Num 4/6** steer. Drops, kickers and gap jumps – take them with enough speed. Fall off the track and you lose a life (3 per run). Every finish gate is a new level. Best level in STATS.
- `moto sandbox` – free ride on flat ground full of jumps, no lives, no record.

### FPV – drone racing (PC only)
`fpv` – fly an FPV drone through the rings. The **yellow** ring is the one you need, the **orange-red** ones come next. Miss a ring and you have to turn back – the next ones don't count until you fly through it.
- **Num 8** nose down (faster), **Num 2** nose up, **Num 4/6** turn, **Num + / Num -** up / down, **Enter** short boost
- The battery drains all the time – every ring adds a few seconds.
- Hit the ground or a rock and the drone explodes (the crater stays) – *NO SIGNAL*. Empty battery – *BATTERY EMPTY*.
- Most rings in one flight – **BEST FPV** in STATS.

### DREAM (PC only)
`dream` – walk through dreams: islands in the void, empty cities, hills, forests of pillars. **Num 8/2** walk, **Num 4/6** turn. Find the glowing crystals – collect enough and you wake up in a new dream. Walk into the void and you fall… And sometimes you are not alone in the dream – keep your distance.

### CPTR, HELL, BugGO
- `cptr` – fly a copter through a tunnel (**Num 8 / Num 2**), best flight in STATS
- `hell` – ASCII HELL shooter (PC only), best time in STATS
- `buggo` – a bug hides nearby; find it with **BugGO** (kukaOS) or `buggo cam` and catch it with **Enter**. Caught bugs count in STATS – some are very rare…

### CHIP-8 emulator (PC only)
The tablet runs real **CHIP-8** games – a tiny game computer from the late 70s, still loved by homebrew makers today.
- Put `.ch8` files into `profile/KNS/chip8/` on your PC
- `chip8 list` – your files, `chip8 <name>` – run one (e.g. `chip8 minefield`)
- Keys: **Num 8/2/4/6**, **Num 5**, **Enter**, **Num + / Num -** (CHIP-8 keys 5/8/7/9, 6, 4, A, 0)
- **MINEFIELD** – own free example game, with its source code, available on here on GitHub.
- Use only **free / homebrew games** or ones you have the rights to.

### Quick ones
`dice`, `dice 20`, `coin`

---

## Terminal

The heart of the tablet.

- **Enter** – start typing, **Enter** – run the command, **ESC** – stop typing
- **ESC** in the terminal (when not typing) – switches the tablet off
- **Arrow keys** – last commands, **Tab** – complete a command
- `help` – commands by topic: `help programs`, `help games`, `help players`, `help tools`, `help system`; `help all` – every command
- `<command> help` – what it does (e.g. `map help`)
- **Num 8 / Num 2** – scroll the history

### Useful commands

**Navigation and info**
- `map`, `kns`, `list`, `stats`, `status`, `aircrack`, `lidar` – open the screens above
- `kns <id>`, `map <id>` – a specific teammate; `players` / `ids` – player IDs
- `call <id>`, `phone`, `phone list`, `channel <n>` – voice calls and shared channels (see **Phone & channels** section)
- `health`, `h <id>` – your body or a teammate's: health in %, blood, consciousness, bleeding
- `taxi` – call a taxi (or work as a driver - see **Taxi** section)
- `where <id>` – distance and direction to a teammate
- `gps` / `me` – your grid position, `az <x> <y>` / `azimuth <x> <y>` – distance and direction to a grid (e.g. `az 0482 1135`)
- `compass` / `c` – the direction you are facing
- `obd` – your vehicle: engine, rpm, gear, speed, fuel, damage
- `scanner` / `scan` – deployed radios nearby (rough distance and direction)
- `material` / `mat` – what the surface you look at is made of (ballistics, up to 5 m)
- `origin` / `ori` – which mod the object you look at comes from, all mods that changed it and its base prefabs (up to 5 m)

**Server and connection**
- `net` – server name, server FPS, your FPS, ping, packet loss
- `fps`, `ping`, `ip`, `server` / `host`, `id` (your name and player ID), `mods` (server mod list)

**Camera and CCTV**
- `camera` – back camera; **hold Num 5** to take a photo
- `selfie` – front camera (mirrored)
- `camera list` – your saved photos (folder `profile/KNS/screenshots`)
- `cctv set [height] [direction]` – place your CCTV camera here (height 10-100 cm), `cctv` – connect (up to 300 m), `cctv off` – remove. One camera, gone when you die.

**Fun**
- Games – see the **Games** section (`games` lists them)
- `player list`, `player <name>`, `player next / prev / stop` – sounds that keep playing in the background; `volume 0-100`
- `video list`, `video <name>` – short videos (PC only)
- `armahints`
- `wiki <word>` – the start of a Wikipedia article (PC only, asks for permission the first time)
- `radio` – radio stations: `radio <n>`, `radio next`, `radio list`, `radio off`, `radio vol 0-100` (needs the Project Sonar mod on the server)

**Other**
- `log` – notifications, players joining / leaving, killfeed and kukaUX messages with real time
- `print <text>` – write your name, position, time and text to the STATUS log; `save` – export STATUS and terminal logs to a file
- `kpad` – new note, `kpad list` – saved notes, `kpad <n>` – open one (inside a note: Enter new line, `:q` or ESC exit)
- `theme` – terminal colors, `wallpaper` – kukaOS backgrounds, `stackoverflow` – unlock a new one (see **Themes and wallpapers**)
- `clear` – clear the terminal history, `run <program>` – same as typing the program
- `kukaux` – the kukaOS screen
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
| `az` | azimuth |
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
- Some features are **PC only** (photos, files, videos, Wikipedia, HELL, LIDAR, DREAM, MOTO, FPV, CHIP-8) – on consoles you'll see *"This is PC-exclusive feature."* BATTLE, BLOX, HANGMAN and CPTR work everywhere – PC and console players can play BATTLE together.
- Settings (brightness, volume, map options, phone, battle, theme, wallpaper…) and what you unlocked are saved on your PC in `profile/KNS/` – they stay after leaving the server or restarting the game.
- Not sure about a command? Type it with `help`, e.g. `cctv help`. Or open the **Manual** on the kukaOS screen.

Have fun! – *kukaUX, made by kuka*
