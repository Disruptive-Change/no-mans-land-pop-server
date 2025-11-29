<!-- Banner -->
<p align="center">
  <img src="assets/banner.png" alt="No Mans Land — Plains of Pain Dedicated Server" width="100%">
</p>

<h1 align="center">🔥 No Mans Land — Plains of Pain Dedicated Server 🔥</h1>
<p align="center">A fully-synced, non-floating, correctly hashed Windows Server 2022 Plains of Pain world.</p>

---

## 🏷️ Badges

<p align="center">
  <img src="https://img.shields.io/badge/Server%20Status-Online-brightgreen?style=for-the-badge&logo=windows" />
  <img src="https://img.shields.io/badge/Game-Plains%20of%20Pain-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Version-v0.6-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/World-No%20Mans%20Land-orange?style=for-the-badge" />
</p>

---

## 🌍 World Information

**Server Name:** `No Mans Land`  
**World Type:** Wasteland (Map ID 0)  
**World Size:** XL recommended  
**Difficulty:** True Wastelander  
**Host OS:** Windows Server 2022  
**Dedicated Server:** SteamCMD App 2227360  

This repo includes:

- The correct cryptographic hash for this world  
- A PDF guide for generating valid Plains of Pain world identity keys  
- A banner and screenshots from gameplay  
- Instructions for launching the dedicated server  

---

## 🔐 World Sync Hash (Required)

This world uses the permanent identity hash generated from the GUI setup.

**Correct hash (must include the = sign):**



Example Hash: 4DIeBZqOIG38ALUK0cEdlk8QXtXR6usLUFEZ2oaO8HM=


⚠️ *Wrong or missing hash causes floating terrain, broken physics, and client desync.*

---

## 📘 PDF Guide

Download the full PDF explaining the correct hash generation process:

👉 **[Download the PDF](docs/No_Mans_Land_Server_Hash_Guide.pdf)**  


---

## 🖥️ How This World Was Created (Correct Method)

1. Launch Plains of Pain GUI  
2. Choose:
   - Seed  
   - Server name  
   - Map size  
   - Difficulty  
   - Map ID  
3. Start the GUI server **once**  
4. Stop GUI server  
5. Copy the generated hash  
6. Use that hash forever with the dedicated server  

This is the *only* way to generate a valid world identity token.

---

## ⚙️ Dedicated Server Startup

Place your server files in:



C:\PoPServer\


Run with:



run_server.bat


Then connect via client using:



Example Hash: 4DIeBZqOIG38ALUK0cEdlk8QXtXR6usLUFEZ2oaO8HM=


---

## 🖼️ Screenshots

<p align="center">
  <img src="assets/screenshot1.png" width="45%">
  <img src="assets/screenshot4.png" width="45%">
</p>




---

## 🤝 Contributions

Feel free to open issues or PRs if you'd like to add:

- automation scripts  
- Windows Server helper scripts  
- Docker containers  
- enhanced configuration  

---

## 🎮 Welcome to No Mans Land  
A harsh wasteland, but a stable one — because the hash is correct.  

📥 Plains of Pain Dedicated Server — Download & Install Instructions

Follow these steps to install and run the Plains of Pain dedicated server for No Mans Land on Windows Server 2022.

🔧 1. Install SteamCMD

Download SteamCMD from Valve:

👉 https://developer.valvesoftware.com/wiki/SteamCMD#Windows

Extract it to:

C:\SteamCMD\


Run once to let it update:

C:\SteamCMD\steamcmd.exe

📦 2. Download the Plains of Pain Dedicated Server

Inside SteamCMD, enter:

login anonymous
app_update 2227360 validate
quit


Your server files will appear in:

C:\SteamCMD\steamapps\common\PlainsOfPainDedicated\


Move them where you want your live server to live:

C:\PoPServer\

⚙️ 3. Configure the Server (World Settings Must Match GUI Setup)

Your world No Mans Land uses a specific seed, map size, difficulty, and worldId.

These MUST match what was used when the GUI server generated your permanent hash.

You can configure via:

Option A — custom.json

Edit:

C:\PoPServer\configs\custom.json


Example:

{
  "serverName": "No Mans Land",
  "worldId": 1,
  "mapId": 0,
  "seed": 12345,
  "difficulty": 2,
  "worldSize": 41,
  "port": 7777,
  "queryPort": 27016,
  "maxPlayers": 10
}

Option B — run_server.bat

Your batch file must include:

PlainsOfPain.exe -nographics -batchmode -ignorecompilererrors -config "configs/custom.json"

🔐 4. Use the Correct World Sync Hash

When joining the server, enter:

4DIeBZqOIG38ALUK0cEdlk8QXtXR6usLUFEZ2oaO8HM=


This hash:

✔ Identifies your exact world
✔ Must remain unchanged
✔ Prevents floating terrain & physics desync
✔ Was generated correctly from your GUI setup

Never modify this hash.

▶️ 5. Start the Dedicated Server

Double-click:

run_server.bat


Or create a shortcut for easier launching.

You should see:

World loads

Networking initializes

Ports open (7777 + 27016)

No GUI

Headless mode running

🎮 6. Join the Server

In Plains of Pain:

Open Multiplayer

Enter your Windows server’s public IP & port

When prompted, paste the hash:

4DIeBZqOIG38ALUK0cEdlk8QXtXR6usLUFEZ2oaO8HM=


Boom — you’re in the real No Mans Land world.

🛠️ 7. (Optional) Windows Firewall Rules

Allow inbound:

UDP 7777
UDP 27016

🧪 8. (Optional) Test Connectivity

From another Windows machine:

Test-NetConnection -ComputerName <SERVER_IP> -Port 7777

