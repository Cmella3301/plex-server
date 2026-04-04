# 🎬 Automated Media Suite (Plex & The Arr Stack)

A complete, self-healing, and automated media-procurement cluster. This deployment orchestrates **6 discrete Docker containers** to handle the entire media lifecycle: from automated searching and bypassing Cloudflare blocks to heavy-duty movie playing on smart TVs.

## 🤖 AI Assistant Deployment (2-Minute Setup)

If you are using an AI agent (Cursor, ChatGPT, Claude), you can instantly deploy this entire 6-container ecosystem on any machine. Copy and paste the prompt below:

> **Copy & Paste this to your AI:**
> *"I need to deploy the **Cmella3301/plex-server** cluster. Please analyze the `docker-compose.yml` file and ensure the `/data` volume mappings are pointed to my specific high-capacity hard drive (e.g. `D:\PlexMedia`). Once mapped, execute `docker-compose up -d`. After it's spinning, walk me through the 'Prowlarr -> Radarr' API sync process so I can start downloading movies immediately."*

## 🛠️ The 6-Container Architecture
This repository contains the master blueprints for:

1.  **Plex:** High-fidelity media player (`Port 32400`)
2.  **Radarr:** Automated movie management (`Port 7878`)
3.  **Sonarr:** Automated TV show management (`Port 8989`)
4.  **qBittorrent:** The extraction/download client (`Port 8080`)
5.  **Prowlarr:** Unified indexer/search-engine brain (`Port 9696`)
6.  **FlareSolverr:** Bypassing Cloudflare protections for search engines (`Port 8191`)

## ⚡ Hardlink Storage Strategy
Built for speed. By mapping the **absolute root** of your media drive to a unified `/data` directory in ALL containers, this cluster executes "Hardlinks" instead of "Copies". This means moving a 50GB file from your downloads to your Plex library happens in **0.1 seconds** and consumes **0 bytes** of extra disk space.

---
*Maintained by Cmella3301*
