+++ 
title = 'Homelab'
+++

# Homelab

I've realized in my career that I learn best when I can get my hands on something and try it for myself. I've been homelabbing since 2015 and utilize it both to reinforce existing skills as well as learn new ones that may be outside my current role.

The homelab has taken many forms over the years, sometimes with the "lab" part taking over the "home" part. When I was trying to break into the networking field from deskside support, I had a labrynth of VLANs through my home network which was a nice learning experience as well as a giant pain with little practical benefit to a home network. Now, I keep the "home" side a lot simpler for mine and my husband's sanity. :)

The "lab" side is hosted by an older Dell workstation obtained from a colleague with a 24 core Westmere Xeon CPU and 48GB of RAM running Proxmox VE. The lab uses entirely free and open-source software as it is both budget-friendly and my personal preference to work with Linux/Unix-based systems. My OS of choice for server applications is generally Debian due to ease-of-use and stability, but I also have an Arch system for gaming and personal use.

Here's a list of services provided:

- DNS (internal)
    - [PiHole](https://pi-hole.net/) for internal hosts providing recursive resolution and ad blocking
- DNS (dn42)
    - [PowerDNS](https://www.powerdns.com/) authoritative server for jsanders.dn42 domain
- NTP
    - Stratum 1 time server via GPS
    - [Chrony](https://chrony-project.org/) fed by [gpsd](https://gpsd.io/)
    - Accurate to ~10ms
- Monitoring
    - [LibreNMS](https://www.librenms.org/) for SNMP-based monitoring
    - [Oxidized](https://github.com/ytti/oxidized) for router config version control
    - (planned) dn42 traffic flow accounting exporting to Prometheus/Grafana
- Routing
    - [VyOS](https://vyos.io/) router/firewall for connectivity to jsanders.dn42 backbone
- Automation
    - [Ansible](https://github.com/ansible/ansible) control node
    - [NetBox](https://netboxlabs.com/) source of truth
- Development
    - Web server
- Media
    - [Plex](https://www.plex.tv/), mainly for my Grateful Dead collection :)
