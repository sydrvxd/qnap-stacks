# QNAP Docker Stacks

Docker Compose Stacks für QNAP NAS (192.168.1.100).

## Stacks

| Stack | Beschreibung | Secrets |
|-------|-------------|---------|
| audiobookshelf | Audiobook & Podcast Server | - |
| chromium-browser | Webtop mit GPU (NVIDIA) | ✅ |
| eclipse-mosquitto | MQTT Broker | - |
| gluetun | VPN (Mullvad) + *arr Stack | ✅ |
| home-assistant | Smart Home | - |
| immich-app | Photo Management (GPU) | ✅ |
| jellyfin | Media Server (GPU) | - |
| my-sql | MySQL 8.4 + Adminer | ✅ |
| netcup | DNS Updater + Cleaner | ✅ |
| nginx-proxy-manager | Reverse Proxy | - |
| searxng-mcp-server | Privacy Search Engine | - |
| teamspeak | Voice Server | - |
| vaultwarden | Password Manager | - |
| zigbee2mqtt | Zigbee Bridge | - |

## Setup

1. `.env.example` kopieren nach `.env`
2. Secrets eintragen
3. `docker compose up -d`

## Netzwerk

Einige Stacks nutzen `qnet-static-eth0-79e6cc` (QNAP Bridge Network) mit festen IPs:
- Home Assistant: 192.168.1.9
- Jellyfin: 192.168.1.38
- MySQL: 192.168.1.19
- MQTT: 192.168.1.165
- Nginx Proxy Manager: 192.168.1.5
- TeamSpeak: 192.168.1.130
- Vaultwarden: 192.168.1.71
