# Homelab

I run my own infrastructure on a Proxmox VE host: real services, in daily production use, administered end to end by me.

## What runs on it

- **A production SaaS** — ClientFoyer (https://clientfoyer.com), a client portal and invoicing tool for freelancers that I built and operate. It is the only service exposed to the public internet.
- **Workflow automation** — an n8n instance running daily jobs (digests, sync checks, scheduled reports).
- **A remote development environment** — a browser-based code server plus a Windows dev/test VM, reachable from anywhere on my tailnet.
- **Supporting utilities** — file sync between my machines and a daily digest service.
- Project and experiment machines stay powered down when they are not in active use.

## How it is run

- **Private by default.** Administrative surfaces are reachable only over Tailscale. The single public path (the SaaS) goes through a Cloudflare Tunnel — nothing else is published.
- **One container per service**, each independently startable, stoppable, and documented.
- **Runbooked.** The full operational documentation exists and is kept current — privately, on purpose (see below).
- **State is snapshotted weekly** to off-site storage.

## Skills this represents

Proxmox VE administration · LXC and VM lifecycle management · Linux system administration · Tailscale-based private networking · Cloudflare Tunnel and DNS · workflow automation (n8n) · production deployment and day-to-day operations of a live web application · backup discipline

## What is deliberately not here

Operational detail — addresses, ports, versions, topology, and the internals of the production application — is not published. This page demonstrates the capability; the runbook stays private.

## The previous lab

Before this, the same hardware ran a study lab simulating a generic corporate enterprise environment (Windows Server, Active Directory, Group Policy, DNS/DHCP, WDS). That lab was retired in October 2026 and its documentation is preserved in [Homelab-docs](https://github.com/EricLottman/Homelab-docs).
