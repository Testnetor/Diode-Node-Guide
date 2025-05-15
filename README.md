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
## 🧾 Register on Diode Collab Platform (MANDATORY)

Once your node is running and your wallet is funded, you **must** register both on the [Diode Collab](https://collab.diode.io/) platform.  
Otherwise, your node **will not be tracked** and you will **receive no points or rewards**.

---

### 1️⃣ Register Your Wallet

➡️ Go to [https://collab.diode.io](https://collab.diode.io)  
➡️ Open the **Registrar** app in the sidebar

Then enter the following command in the bot interface:

```bash
set wallet 0xYOUR_WALLET_ADDRESS
```

✅ Replace `0xYOUR_WALLET_ADDRESS` with the wallet you got from `diode info`  
✅ This step only needs to be done **once per wallet**

---

### 2️⃣ Register Each Node

Every node must be manually registered.

To get your `NodeID`, run the following on your server:

```bash
diode-node.info
```

Then copy the `Node ID` and register it using this format **in the Registrar bot**:

```bash
register node NODEID NodeName
```

📌 `NODEID`: the full string shown in your node info  
📌 `NodeName`: any name you want (e.g. `vps-turkey-1`)

✅ You can register **unlimited nodes** under the same wallet.

---

⚠️ **Important:**  
Nodes that are not registered through Diode Collab will NOT earn rewards — even if they are online and funded.


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
