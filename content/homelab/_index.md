+++ 
title = 'Homelab'
+++

# Homelab

I've realized in my career that I learn best when I can get my hands on something and try it for myself. I've been homelabbing since 2015 and utilize it both to reinforce existing skills as well as learn new ones that may be outside my current role.

The homelab has taken many forms over the years, sometimes with the "lab" part taking over the "home" part. When I was trying to break into the networking field from deskside support, I had a labrynth of VLANs through my home network which was a nice learning experience as well as a giant pain with little practical benefit to a home network. Now, I keep the "home" side a lot simpler for mine and my husband's sanity. :)

The "lab" side is hosted by an older Dell workstation obtained from a colleague with a 24 core Westmere Xeon CPU and 48GB of RAM running Proxmox VE. The lab uses entirely free and open-source software as it is both budget-friendly and my personal preference to work with Linux/Unix-based systems. My OS of choice for server applications is generally Debian due to ease-of-use and stability, but I also have an Arch system for gaming and personal use.

Here's a list of services provided:

- DNS (internal)
    - PiHole for internal hosts providing recursive resolution and ad blocking
- DNS (dn42) (planned)
    - PowerDNS authoritative server for jsanders.dn42 domain
- NTP (Planned)
    - Stratum 1 time server via GPS
- Monitoring
    - LibreNMS for SNMP-based monitoring
    - Oxidized for router config version control
    - OpenBMP monitoring for dn42 (currently disabled due to RAM concerns...)
- Routing
    - VyOS router/firewall for connectivity to jsanders.dn42 backbone
- Automation
    - Ansible control node
    - NetBox source of truth
- Development
    - Web server
