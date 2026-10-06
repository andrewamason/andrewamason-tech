+++
authors = ["Andrew Amason"]
title = "My HomeLab"
date = "2025-03-05"
description = "A Guide to my HomeLab environment and the apps that I use every day."
tags = [
    "Homelab",
    "SelfHosting"
]
categories = [
    "HomeLab",
    "SelfHosting",
]
series = ["SelfHosting"]
+++

## Servers & Hardware

- Synology [DS918+](https://global.download.synology.com/download/Document/Hardware/DataSheet/DiskStation/18-year/DS918+/enu/Synology_DS918_Plus_Data_Sheet_enu.pdf) & [DS517](https://www.synology.com/en-us/products/DX517#features) Expansion Bay
  - Name: **Grimlock**
  - CPU: **INTEL Celeron J3455**
  - RAM: **16 GB**
  - Total Storage: **24.9 TB**
- ASUS RS720 - Unraid 7
  - Name: **CyberTron**
  - CPU: **2x Intel Xeon E5-2620 v4**
  - RAM: **256 GB**
  - Total Storage: **55.5 TB**

I enjoy experimenting with different services to see how they work and interact. Nearly all of them run as containers on CyberTron, my Unraid server, behind the SWAG reverse proxy — so the only port ever exposed for these services is HTTPS/443. Some of my most used services are listed below:

## Infrastructure Containers

- [Technitium](https://technitium.com/dns/): Serves internal split-scope DNS; two of these containers run using a single git repo with 2 different .env files
- [SWAG](https://docs.linuxserver.io/general/swag/): Internal reverse proxy hosting a ZeroSSL wildcard certificate.
- [Traefik](https://traefik.io/traefik/): External reverse proxy using individual Let's Encrypt certificates.
- [Cloudflare-DDNS](https://hub.docker.com/r/oznu/cloudflare-ddns/): Dynamic DNS updater
- [flaresolverr](https://github.com/FlareSolverr/FlareSolverr): Solves Cloudflare challenges
- [Komodo](https://komo.do/): Docker stack management; every stack is a Git repo on Gitea that deploys via webhook
- [Gitea](https://about.gitea.com/): Open-source, lightweight Git hosting

## App Containers

### Watching, Reading, & Listening

- [Plex](https://www.plex.tv/): Video streaming
- [Audiobookshelf](https://www.audiobookshelf.org/): Podcasts and audiobooks
- [FreshRSS](https://freshrss.org/): RSS aggregation
- [Hoarder](https://hoarder.app/): Bookmark and link storage
- [Glance](https://github.com/glanceapp/glance): News dashboard
- [RomM](https://romm.app/?ref=selfh.st): ROM manager and web-based player

### Dashboards & Monitoring

- [Homarr](https://homarr.dev/): Internal dashboard (evaluating against Heimdall; I'll eventually consolidate to one)
- [Heimdall](https://heimdall.site/): Internal dashboard (evaluating against Homarr)
- [Tautulli](https://tautulli.com/): Plex monitoring

### Tech Support

- [KASM Workspace](https://kasmweb.com/): Ephemeral workspaces for investigations
- [RustDesk](https://rustdesk.com/): Remote desktop support
- [ntfy.sh](https://ntfy.sh/) / [apprise](https://hub.docker.com/r/caronc/apprise) / [notifiarr](https://notifiarr.com/?ref=selfh.st) : Self-hosted notification services

### SmartHome

- [HomeAssistant](https://www.home-assistant.io/): Smart home hub

### Media Download & Management Apps

- [Tdarr](https://home.tdarr.io/): Distributed media transcoding that tracks the library and follows defined "flows"
- [Immich](https://immich.app): Photo management — a self-hosted Google Photos
  - [Immich Frame](https://github.com/immichFrame/ImmichFrame) Picture-frame app for Immich; I run the Google TV app on my living room tv which connects to this service.

## Apps In Testing

- [ChangeDetection.io](https://changedetection.io): Self-hosted website change detection
- [CrowdSec Blocklists](https://www.crowdsec.net/): Customized IP blocklists
- [Wazuh XDR](https://wazuh.com/): Self-hosted XDR and SIEM for endpoints
- [authentik](https://goauthentik.io/): Identity provider (SSO)

A great source for discovering more self-hosted apps: <https://selfh.st/>

## Apps Retired

- [YoutubeDL-Material](https://hub.docker.com/r/tzahi12345/youtubedl-material): Worked well, but I moved on as updates slowed
- [lidarr](https://lidarr.audio): Music collection manager; I just didn't use it
- [Bitwarden On-Prem](https://bitwarden.com/help/install-on-premise-linux/): Migrated to Bitwarden Cloud; self-hosting wasn't worth the effort
- [Pi-Hole](https://pi-hole.net): Worked well for ad blocking but caused frustrating Google search issues for the family. I wanted more control, so I moved to Technitium.
- [GitLab](https://about.gitlab.com/platform/): Far more than I needed for Git hosting, and very memory-hungry.
- [Wallabag](https://wallabag.org/): Didn't love the interface; may revisit it later
- [Portainer](https://portainer.io): Used it for a long time, but disliked how it handled stack file locations and change tracking. Moved to [Komodo](https://komo.do/).

## App Investigation Backlog

### Techy

- [HomeBox](https://homebox.software/en/?ref=selfh.st)
- [Haptic](https://www.haptic.md/?ref=selfh.st)
- [Web Check](https://web-check.xyz/?ref=selfh.st)
- [Your Spotify](https://github.com/Yooooomi/your_spotify?ref=selfh.st)
- [Dash](https://getdashdot.com/?ref=selfh.st)
- [Petio](https://petio.tv/?ref=selfh.st)
- [Adminer Evo](https://docs.adminerevo.org/?ref=selfh.st)
- [Solid Time](https://www.solidtime.io/?ref=selfh.st)
- [Cal.com](https://cal.com/?ref=selfh.st)
- [Dillinger](https://dillinger.io/)
- [AirTrail](https://airtrail.johan.ohly.dk/docs/overview/introduction)
- [LinkStack](https://linkstack.org/?ref=selfh.st)
- [Sink](https://sink.cool/?ref=selfh.st)

### Home Improvement

- [Mealie](https://docs.mealie.io/?ref=selfh.st)
- [Manyfold](https://manyfold.app/?ref=selfh.st)
- [Community Christmas](https://github.com/Wingysam/Christmas-Community?ref=selfh.st)
- [Tandoor](https://docs.tandoor.dev/?ref=selfh.st)
- [Grocy](https://grocy.info/?ref=selfh.st)
- [SharedMoments](https://github.com/tech-kev/SharedMoments?ref=selfh.st)
