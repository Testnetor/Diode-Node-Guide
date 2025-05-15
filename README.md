# 🛰️ Diode Node Guide

<p align="center">
  <img src="https://pbs.twimg.com/profile_images/1843447218130276352/IMDW6sot_400x400.png" height="250" alt="Diode Logo" />
</p>

<h1 align="center">🚀 Run a Diode Node in 5 Minutes</h1>

<p align="center">
  <b>Decentralized internet starts with you.</b><br>
  Set up your Diode node and start earning rewards during <code>#Epoch674</code>.
</p>

---

## 📦 Requirements

Minimum setup to run a Diode node:

```bash
✅ Linux system (Ubuntu 20.04+, Debian, etc.)
✅ 1 vCPU & 1 GB RAM
✅ 10 GB free storage
✅ Internet connection
✅ Basic terminal knowledge
```
# ⚡ Diode Node Setup Guide (Snap Method)

This guide explains how to install and manage a Diode node using Snap.  
Tested on Ubuntu and Debian-based Linux systems.

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

📝 Don’t forget to send your node wallet and participation content at the end of the epoch to earn rewards!


### 🎯 Tip: Boost Rewards

```bash
# Send 1–10 DIODE tokens to your node wallet (starts with 0x…)
# This boosts your reward score during campaigns like Epoch 674
```
