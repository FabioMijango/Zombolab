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

**Zombolab** allows you to host a **Project Zomboid Dedicated Server** for free. It uses **LocalToNet** as a tunnel to expose an IP address and connect to the server, while saving your world data persistently in **Google Drive**.

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

1.  **Set up:** Run the `Set up` cell. It will install everything it needs to run the server. Wait for the installation to finish.
    > *If an error occurs during installation, try running the cell again.*

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
