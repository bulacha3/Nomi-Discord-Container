# Nomi-Kin Discord Integration (Cloud Run Version)
This wouldn't be possible without d3tourrr hard work. 
Also for more in depth configurations you should go there: https://github.com/d3tourrr/NomiKin-Discord

This repository contains a Dockerized integration for Nomi and Kindroid bots with Discord, specifically designed to run on Google Cloud Run. With this setup, you can easily deploy the bot without the need for local configurations or manual environment variable setups.

## Overview

- **[Nomi](https://nomi.ai)**: A platform offering AI companions for human users to chat with. This bot enables you to integrate Nomi directly into your Discord server.
- **[Kindroid](https://kindroid.ai)**: Another platform offering AI companions. This bot also supports Kindroid integration, allowing them to chat within your server.

By hosting on **Google Cloud Run**, you benefit from high availability and simplified deployment processes.

---

## Features

- **Fully Dockerized**: Simplifies deployment to any container-supporting platform.
- **Runs on Google Cloud Run**: No local infrastructure or manual environment management needed.
- **Supports Nomi and Kindroid Bots**: Flexible integration for both platforms.
- **Discord Integration**: Easily integrates with your Discord server to bring AI companions to your community.

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/bulacha3/Nomi-Discord-Container.git
cd Nomi-Discord-Container
```
2. Build the Docker Image
   ```
   docker build -t gcr.io/YOUR_PROJECT_ID/nomi-discord .
   ```
   Replace YOUR_PROJECT_ID with your Google Cloud Project ID.
3.  Push the Docker Image to Google Container Registry
   ```
   docker push gcr.io/YOUR_PROJECT_ID/nomi-discord

   ```
4. Deploy to Google Cloud Run
   ```
   gcloud run deploy nomi-discord \
    --image gcr.io/YOUR_PROJECT_ID/nomi-discord \
    --platform managed \
    --region YOUR_REGION \
    --allow-unauthenticated

   ```
   Replace:
   - YOUR_PROJECT_ID with your Google Cloud Project ID.
   - YOUR_REGION with your preferred region (e.g., us-central1, southamerica-east1).
