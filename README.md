✅ COPY-THIS-INTO-README.md (Dark Theme)
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



4DIeBZqOIG38ALUK0cEdlk8QXtXR6usLUFEZ2oaO8HM=


⚠️ *Wrong or missing hash causes floating terrain, broken physics, and client desync.*

---

## 📘 PDF Guide

Download the full PDF explaining the correct hash generation process:

👉 **No_Mans_Land_Server_Hash_Guide.pdf**  
(Place it in `/docs/` inside repo once uploaded)

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



4DIeBZqOIG38ALUK0cEdlk8QXtXR6usLUFEZ2oaO8HM=


---

## 🖼️ Screenshots

<p align="center">
  <img src="assets/screenshot1.png" width="45%">
  <img src="assets/screenshot4.png" width="45%">
</p>

More screenshots can go into `assets/screenshots/`.

---

## 📂 Repository Structure



/assets/
banner.png
screenshot1.png
screenshot4.png

/docs/
No_Mans_Land_Server_Hash_Guide.pdf

/README.md


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
