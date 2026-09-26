# Linux Networking & System Administration Lab

A hands-on lab covering core Linux system administration and network services,
built from scratch across multiple VMs — from initial setup through DHCP, DNS,
NTP, shell scripting/automation, SSH, and firewall configuration. Built for
IE2012 (Systems and Network Programming), SLIIT.

## Overview

Everything here was configured and tested on real virtual machines (Kali Linux +
2x Ubuntu, connected via bridged networking so they could communicate with each
other and the internet), not just theory — each section documents the actual
commands run, the config files edited, and the verification steps used to
confirm each service worked (e.g. confirming DHCP leases were issued correctly,
testing DNS resolution against an external server, pinging between VMs).

## Contents

1. **VM Setup** — Installing VirtualBox and Kali Linux, allocating resources
2. **Command Line Introduction** — Core Linux commands (navigation, file ops, editors)
3. **System Information & User Management** — `uname`, `useradd`, `usermod`, permissions, process management
4. **DHCP Server** — Installing and configuring `isc-dhcp-server`, static IP assignment, subnet/scope configuration, verifying leases across multiple VMs
5. **DNS** — Configuring a BIND9 server, zone files, SOA/NS/A records, testing resolution against an external resolver
6. **NTP** — Time synchronization configuration
7. **Shell Scripting & Security** — Bash scripting for automated system reporting (uptime, memory, disk usage), scheduled via `crontab`
8. **SSH** — Secure remote access setup
9. **Iptables & ACLs** — Firewall rules and access control
10. **Best Practices** — Closing recommendations

## What This Repo Contains

- `networking-lab-report.pdf` — full write-up with screenshots, configuration
  file contents, command-by-command explanations, and troubleshooting notes
  (e.g. resolving a DHCP server restart failure caused by an unconfigured
  network interface)

## Why This Is Here

This was built to get hands-on with the services that actually run the network
layer most developers only interact with indirectly — useful grounding for
security-adjacent work, since DHCP/DNS misconfiguration and firewall rules are
common attack surfaces.
