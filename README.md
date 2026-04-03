# 🎬 Self-Hosted Plex Media Server (Dockerized)

A scalable, isolated deployment of the Plex Media Server using Docker Orchestration. This ensures the host system remains completely clean of Registry Keys while offloading massive media file storage strictly to secondary bulk drives.

## 🤖 AI Assistant Installation (For ChatGPT/Claude/Cursor)

If you use an AI assistant, you can have it completely install and set up this server for you. Simply copy and paste the prompt below into your AI of choice:

> **Copy & Paste this to your AI:**
> *"I want to run a locally-hosted Plex Media Server on my machine. Please give me the exact terminal commands to clone the repository (from Cmella3301/plex-server), navigate into the folder, and spin it up using Docker Compose. If I don't have Docker installed, briefly tell me how to get it for my OS first. Remind me that I need to edit the YAML file to map my specific hard drive to the media folders before spinning it up. Once the container is running, tell me what localhost port to open."*

## Architecture Details
- Utilizes `linuxserver/plex` to ensure absolute stability and correct permissions on Windows Docker mapped volumes.
- Separates local SSD cache (`/config`) from bulky hard-drive cache (`/data`), creating an infinitely replicable environment.
