# 🏰 The Mortal Kombat Media Cluster

A fully automated, self-healing media procurement and playback stack orchestrated via Docker Compose.

## 🤖 AI Assistant Deployment (For Claude/ChatGPT/Cursor)

If you ever need to move this server to a new computer or fix it instantly, simply copy and paste the prompt below into your AI of choice:

> **Copy & Paste this to your AI:**
> *"I have a locally-hosted media server located in `C:\Users\Mella\Documents\plex-server`. It uses a 6-container Docker Compose stack (Plex, Radarr, Deluge, Prowlarr, FlareSolverr). Please check my `docker-compose.yml` to ensure the volumes for `D:\PlexMedia` are mapped correctly. Check the `deluge-config` for the correct password and ensure the internal download paths are set to `/data/downloads` in the `core.conf`. If I am having difficulty with 'Host not found' errors, verify my host VPN status and add `dns: 1.1.1.1` to the containers if necessary. Once everything is running, tell me the ports for Plex (32400), Radarr (7878), and Deluge (8112)."*

## 📦 Included Services
- **Plex:** Media playback and library management.
- **Radarr:** Automated movie discovery and management.
- **Deluge (The Tank):** High-speed automated downloader.
- **Prowlarr:** Centralized indexer/search brain.
- **FlareSolverr:** Automated Cloudflare bypass proxy.

## ⚙️ Storage Strategy
This cluster uses a **Hardlink** strategy. The host directory `D:\PlexMedia` is mapped to `/data` in all containers, allowing for near-instant file moves and zero-copy library organization.

## ⚠️ Important Note on VPNs
**Crucial:** If you have a system-wide VPN running on your Windows host, it may block the internal Docker DNS, leading to 'Host not found' errors for trackers. Ensure your host VPN is **OFF** when initiating new downloads, or configure a split-tunnel / internal Docker VPN.
