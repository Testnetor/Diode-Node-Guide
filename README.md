# 🛰️ Diode Node Guide

<p align="center">
  <img src="https://pbs.twimg.com/profile_images/1843447218130276352/IMDW6sot_400x400.png" height="250" alt="Diode Logo" />
</p>

<h1 align="center">🚀 Run a Diode Node in 5 Minutes</h1>

<p align="center">
  <b>Decentralized internet starts with you.</b><br>
  Set up your Diode node and start earning rewards💸
</p>

---
# ⚡ Diode Node Setup Guide (Snap Method)

This guide explains how to install and manage a Diode node using Snap.  
Tested on Ubuntu and Debian-based Linux systems.

## 📦 Requirements

Minimum setup to run a Diode node:

```bash
✅ Linux system (Ubuntu 20.04+, Debian, etc.)
✅ 1 vCPU & 1 GB RAM
✅ 10 GB free storage
✅ Internet connection
✅ Basic terminal knowledge
```

---

## 🌐 Optional: Open Required Ports

Some environments may require opening these ports on your firewall:

```bash
sudo ufw allow 22
sudo ufw allow 38537
sudo ufw allow 51055
sudo ufw allow 41046
sudo ufw allow 443
sudo ufw allow 993
sudo ufw allow 1723
sudo ufw allow 10000
sudo ufw allow 8545
sudo ufw allow 8443
```

---

## 🔄 1. Update & Upgrade the System

```bash
sudo apt update && sudo apt upgrade -y
```

---

## 🧩 2. Ensure Snap is Installed

Snap is required to install the Diode node. Most Ubuntu systems already have it.

```bash
sudo apt install snapd -y
```

---

## 📦 3. Install Diode Node (Snap)

```bash
sudo snap install diode-node
```

After installation, `diode-node` runs automatically in the background.

---
## 🧾 Register on Diode Collab (Required!)

Once your node is running and your wallet is funded, you must register both with the Diode Collab platform using the **Telegram bot**.

---

### 1️⃣ Register Your Wallet

In the Telegram bot (e.g., `@diode_registrar_bot`), send the following:

```bash
set wallet 0xYOURWALLETADDRESS
```

✅ You only need to do this **once per wallet**.  
(Replace `0xYOURWALLETADDRESS` with the address you got from `diode info`.)

---

### 2️⃣ Register Your Node(s)

Each node must be registered manually.  
To do that, run `diode-node.info` or `diode info` and get your `NodeID`.

Then in the same bot chat, send:

```bash
register node NODEID MyNodeName
```

🔹 `NODEID` is a long string shown in your node info  
🔹 `MyNodeName` is a name you choose (e.g. `vps-france-1`)

📌 You can register **multiple nodes**, no limit.

---

📸 *If needed, refer to the pinned message or image in the Collab bot group for an example.*

⚠️ **Reminder:**  
Nodes that are not registered will **not earn rewards** — even if they are online and funded!


### 🚨 Required: Fund Your Node Wallet

```bash
# You must send 1–10 DIODE tokens to your node wallet (starts with 0x...)
# Without this balance, your node will NOT accumulate points or rewards
# Send from your MetaMask or other EVM-compatible wallet
```


## 🔍 4. View Node Info

Check your node’s status, ID, and connection info with:

```bash
diode-node.info
```

---

## 🛠️ Useful Commands

| Description | Command |
|------------|---------|
| 📥 Install Diode Node | `sudo snap install diode-node` |
| 🔎 View Node Info | `diode-node.info` |
| ♻️ Restart the Node | `snap restart diode-node` |
| 📄 View Live Logs | `sudo snap logs diode-node -f` |

---
