<div align="center">
  <img src="https://raw.githubusercontent.com/FabioMijango/Zombolab/refs/heads/main/Zombolab-Logo.png" alt="Zombolab Logo" width="300">

  <h1>Zombolab</h1>

  <p>
    <strong>Run a persistent Project Zomboid Dedicated Server using Google Colab & Google Drive.</strong>
  </p>

  <p>
    <a href="LICENSE">
      <img src="https://img.shields.io/github/license/FabioMijango/Zombolab" alt="License"/>
    </a>
  </p>
</div>

---

## 🧟 What is Zombolab?

**Zombolab** allows you to host a **Project Zomboid Dedicated Server** for free in Google Colab. It uses **LocalToNet** as a tunnel to expose an IP address and connect to the server, while saving your world data persistently in **Google Drive**.

Inspired by [Minecolab project](https://github.com/thecoder-001/MineColab) and [MineColab_Improved](https://github.com/N-aksif-N/MineColab_Improved).

---

## 🌐 1. Prerequisite: Tunnel Setup (Localtonet)

Before running the code, you need to configure the UDP connection.

1.  Register at [localtonet.com](https://localtonet.com/).
2.  Go to **TCP - UDP Tunnels**.
3.  Create a tunnel with these **settings**:
    * **Protocol:** `UDP`
    * **Local Address:** Leave as default (`127.0.0.1`)
    * **Local Port:** `16261`
    * **Server**: Select the server closest to you.
    * **Auth Token**: You can use the `Default Token`.
4.  Click **Create**.

---

## 🚀 2. How to Run

1.  **Set up:** Select your desired game version from the dropdown menu (**Stable** for Build 41 or **Unstable** for Build 42 Beta). Then, run the `Set up` cell. It will install all necessary dependencies and the game files.
    > *If an error occurs during installation, try running the cell again.*

    > ⚠️ **Warning:** Switching versions (e.g., from Stable to Unstable) while having an existing save file **may cause the server to fail**. If you change versions, you must backup your saves and empty the `ZomboidSaves` folder in your Google Drive to avoid database conflicts.

2.  **Put Token:** Once the setup is finished, scroll down to the configuration block and paste your Token in the `TOKEN = "YOUR_TOKEN"` variable.
    > You can find your **AUTH TOKEN** in the `Dashboard` section at [localtonet.com](https://localtonet.com/).

3.  **Run Server:** Execute the `Run server` cell.

4.  **Activate Tunnel:** Watch the logs. When you see a message like this:
    ```
    ⏳ Waiting for tunnel connection...
    State: 2025-12-07 01:19:38 AuthTokenName loaded: Default...
    ```
    Go to [**TCP - UDP Tunnels**](https://localtonet.com/tunnel/tcpudp) on the website and click the **Start** button on your tunnel to bring it Online.

5.  **Success:** If everything connects correctly, you will see something like this in the output:
    ```text
    ✅ TUNNEL SUCCESSFULLY CONNECTED!
    👇 YOUR IP TO ENTER THE GAME 👇
    --------------------------------------------------
    🚀 URL: someip.localto.net
    📦 PORT: somePort
    --------------------------------------------------
    ```
    > You can also copy the IP address directly from the **TCP - UDP Tunnels** section on the website.
> ⚠️ **Note:** The server takes about **5-10 minutes** to download and start. Wait for the `SERVER STARTED` message in the logs before trying to join.

---

## 📚 Resources & Useful Links

Here are some useful links to help you configure your server settings, manage mods, and understand the tools used in this project.

### 🧟 Project Zomboid Server Management
* **[PZ Wiki - Dedicated Server](https://pzwiki.net/wiki/Dedicated_Server):** The official guide.
* **[Server Settings (servertest.ini)](https://pzwiki.net/wiki/Server_Settings):** **Highly Recommended.** Explains what every single line in the configuration file does (Zombie population, loot rarity, PVP, etc.).
* **[Settings and mods](https://pzwiki.net/wiki/Dedicated_server#Linux_4):** Learn how to add Workshop IDs and Mod IDs to your configuration to play with mods.

* **[Project Zomboid Server Setup Tutorial | Linux Guide](https://youtu.be/jvduDZ-vE4c):** Video tutorial how to create your own server. 
* **[SteamCMD Wiki](https://developer.valvesoftware.com/wiki/SteamCMD):** Valve's official wiki for SteamCMD
---
