Vuln-OS

Vuln-OS is a one-VM intentionally vulnerable cybersecurity training platform designed for isolated VirtualBox labs.

Current build status

This repository contains the working application source, challenge framework, CLI, reset/backup/restore logic, health checks, tests, systemd units, documentation, and a VirtualBox project definition.

Important: the supplied .vbox is a project definition/template. A bootable Linux disk must be produced by the build script on a real Linux/VirtualBox host. This environment cannot honestly claim to have booted VirtualBox, so VM boot/reboot verification remains a required host-side gate.

Architecture
Base OS: Debian-family Linux
Python + Flask
SQLite
systemd
Vanilla HTML/CSS/JS
Host-only networking recommended

No Docker/Kubernetes/Redis/PostgreSQL required.

Quick start on an installed Linux VM

sudo ./scripts/install.sh

sudo systemctl enable --now vuln-os.target
vuln-health

Dashboard: http://127.0.0.1:8080

For a VirtualBox lab, bind the dashboard to the host-only interface and keep the vulnerable services off bridged/public networking.
Safety

Use only in an isolated, authorized laboratory. 

Do not expose the vulnerable services to the public Internet.