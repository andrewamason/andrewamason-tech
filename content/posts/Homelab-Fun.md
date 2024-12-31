+++
authors = ["Andrew Amason"]
title = "My HomeLab"
date = "2024-12-31"
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

## My HomeLab

## Servers & Hardware

- Synology [DS918+](https://global.download.synology.com/download/Document/Hardware/DataSheet/DiskStation/18-year/DS918+/enu/Synology_DS918_Plus_Data_Sheet_enu.pdf) & [DS517](https://www.synology.com/en-us/products/DX517#features) Expansion Bay
  - Name: **Grimlock**
  - CPU: **INTEL Celeron J3455**
  - RAM: **16 GB**
  - Total Storage: **24.9 TB**
- QNAP [TVS-463](https://www.qnap.com/en-us/product/tvs-463)
  - Name: **Snarl**
  - CPU: **AMD GX-424CC with Radeon R5E**
  - RAM: **8 GB**
  - Total Storage: **6.27 TB**
- HP ProDesk 600 G3 Mini - OS: VMware ESX 7
  - Name: **Nova**
  - CPU: **Intel(R) Core(TM) i5-7500T**
  - RAM: **16 GB**
  - VMs:
    - **BlueStreak**
      - OS: Rocky Linux 9.5
- Dell Optiplex 9020
  - OS: Rocky Linux 9.5
  - Name: **Trailbreaker**
  - CPU: **Intel(R) Core(TM) i5-4570**
  - RAM: **24 GB**

## Infrastructure Containers

- [Technitium](https://technitium.com/dns/): Serves internal Split scope DNS, 2x of these containers using a single git repo with 2 different .env files
- [SWAG](https://docs.linuxserver.io/general/swag/): Internal Reverse Proxy
- [Traefik](https://traefik.io/traefik/): external reverse proxy
- [Cloudflare-DDNS](https://hub.docker.com/r/oznu/cloudflare-ddns/): DDNS Updating Container
- [flaresolverr](https://github.com/FlareSolverr/FlareSolverr): solves cloudflare prompts
- [Komodo](https://komo.do/): Docker Stack Management, all stacks are git repos on gitea that deploy on gitea webhooks
- [Gitea](https://about.gitea.com/): OpenSource lightweight git hosting

## Apps

### Watching, Reading, & Listening

- [Plex](https://www.plex.tv/): Video Streaming
- [Audiobookshelf](https://www.audiobookshelf.org/): Podcasts & Audiobooks
- [FreshRSS](https://freshrss.org/): RSS Aggregation
- [Hoarder](https://hoarder.app/): Bookmarks & Links Storing
- [Glance](https://github.com/glanceapp/glance): News Dashboard

### Dashboards & Monitoring

- [Homarr](https://homarr.dev/): Internal Dashboard in competition with Heimdall will eventually consolidate to one or the other
- [Heimdall](https://heimdall.site/): IInternal Dashboard in competition with Homarr will eventually consolidate to one or the other
- [Tautulli](https://tautulli.com/): Plex Monitoring

### Tech Support

- [KASM Workspace](https://kasmweb.com/): Ephemeral Workspaces & Investigations
- [RustDesk](https://rustdesk.com/): Desktop Remote Support

### SmartHome

- [HomeAssistant](https://www.home-assistant.io/): Smart Home Hub
  
### Media Download & Management Apps

- [Prowlarr](https://prowlarr.com/): Centralized Index management
- [Overseerr](https://overseerr.dev/): Nice front end for Sonarr/Radarr
- [Sonarr](https://sonarr.tv/): TV Show Collection Manager
- [Radarr](https://radarr.video/): Movie Collection Manager
- [Readarr](https://readarr.com/): ebook Collection Manager
- [qBitTorrent](https://www.qbittorrent.org/): For downloading & seeding Linux Distros (obviously)
- [Metube](https://github.com/alexta69/metube): Youtube Video downloader (good for single video downloads or one off playlist downloads probably going to retire)
- [Pinchflat](https://github.com/kieraneglin/pinchflat): Youtube download tracker (alot more full featured than MeTube)
- [Tdarr](https://home.tdarr.io/): Distributed Media Transcoding, tracks library and follows designated "flows"
- [Immich](https://immich.app): Photo Management App "Selfhosted Google photos"
  - [Immich Frame](https://github.com/immichFrame/ImmichFrame) Picture Frame App for Immich
  
## Apps In Testing

- [ntfy.sh](https://ntfy.sh/) / [apprise](https://hub.docker.com/r/caronc/apprise) / [notifiarr](https://notifiarr.com/?ref=selfh.st) : selfhosted Notifications Service
- [Romm](https://romm.app/?ref=selfh.st) - Roms Manager

## Apps to Implement/Test Soon

- [ChangeDetection.io](https://changedetection.io): Self-Hosted WEBSITE CHANGE DETECTION
- [CrowdSec Blocklists](https://www.crowdsec.net/): Customized IP Blocklists
- [Wazuh XDR](https://wazuh.com/): Self-Hosted Unified XDR and SIEM protection for endpoints
- [authentik](https://goauthentik.io/): IDP

Great source of additional applications can be found here: <https://selfh.st/>

## Apps Retired

- [YoutubeDL-Material](https://hub.docker.com/r/tzahi12345/youtubedl-material): Worked well but slowly abandoned due to lack of updates
- [lidarr](https://lidarr.audio): Music Collection Manager, just didnt use this functionality
- [Bitwarden On-Prem](https://bitwarden.com/help/install-on-premise-linux/): Migrated to Bitwarden Cloud, didnt see the ROI in self-hosting
- [Pi-Hole](https://pi-hole.net): worked well for add blocking just got frustating with some google search results for family. Ultimately i wanted more control so moved to Technitium
- [GitLab](https://about.gitlab.com/platform/): Waaay overkill for what i needed in a git hosting solution. Used a ton of memory as well.
- [Wallabag](https://wallabag.org/): didn't love the interface may come back and try it again at some point
- [Portainer](https://portainer.io): used for a long time but i don't like how it hit the stack file locations and didnt track changes as well. Moved to [Komodo](https://komo.do/).
  
## App Investigation Backlog

### Andrew Amason.tech

- [hugo](https://gohugo.io/): Static Websites based on markdown. will likely build andrewamason.tech on this
- [LinkStack](https://linkstack.org/?ref=selfh.st)
- [Sink](https://sink.cool/?ref=selfh.st)

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

### Home Improvement

- [Mealie](https://docs.mealie.io/?ref=selfh.st)
- [Manyfold](https://manyfold.app/?ref=selfh.st)
- [Community Christmas](https://github.com/Wingysam/Christmas-Community?ref=selfh.st)
- [Tandoor](https://docs.tandoor.dev/?ref=selfh.st)
- [Grocy](https://grocy.info/?ref=selfh.st)
- [SharedMoments](https://github.com/tech-kev/SharedMoments?ref=selfh.st)
