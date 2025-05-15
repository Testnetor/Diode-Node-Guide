![banner](https://diode.io/assets/img/diode_og_image.png)

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
### 🚨 Required: Fund Your Node Wallet

```bash
# You must send 1–10 DIODE tokens to your node wallet (starts with 0x...)
# Without this balance, your node will NOT accumulate points or rewards
# Send from your MetaMask or other EVM-compatible wallet
```
---

## 🧾 Register on Diode Collab App (REQUIRED)

Running a node is **not enough** — you must register your wallet and each node inside the **Diode Collab desktop app** in order to receive points and rewards.

---

### 🧱 Step 1: Download the Collab App

Download and install the Diode Collab application from:

🔗 https://diode.io/#download-app

Supports: Windows, macOS, Linux

---

### 🧠 Step 2: Register Your Wallet

1. Open the app  
2. Connect the wallet you used on your node  
3. Go to the **Registrar** bot tab  
4. Enter the following command:

```bash
set wallet 0xYOUR_WALLET_ADDRESS
```

✅ Only needed once per wallet

---

### 🖥️ Step 3: Register Your Node(s)

1. On your server, run the command:

```bash
diode-node.info
```

2. Copy your **NodeID**

3. In the **Registrar bot** inside the app, write:

```bash
register node NODEID MyNodeName
```

📌 `NODEID`: from your server (it's a long string)  
📌 `MyNodeName`: any nickname for the node (e.g., `vps-france-1`)  
✅ You can register unlimited nodes

---

⚠️ If you skip this step, your node will **NOT be tracked**, even if it's online and funded.


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
