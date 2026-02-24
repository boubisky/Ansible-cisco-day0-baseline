# Cisco C9300 Day-0 Base Configuration via Ansible

This repository contains a **minimal Ansible deployment template** for pushing
initial secure configurations to Cisco Catalyst 9300 switches.

Designed for:

- Network automation portfolios
- Day-0 provisioning labs (EVE-NG / physical switches)
- Secure baseline configuration enforcement

---

## What This Deploys

The template configures:

- Hostname + domain
- Secure local admin account
- Enable secret
- SSH-only management
- RSA key generation
- Logging + timestamps
- Disabled insecure services:
  - HTTP server
  - HTTPS server
  - CDP

---

## Repository Layout

cisco-day0-ansible/
├── README.md
├── inventory.yml
├── generate-configs.yml
├── deploy-configs.yml
├── rendered/
│   └── (configs will be created here)
└── templates/
    └── base_config.j2

---

## Requirements

- Ansible 2.12+
- Python 3
- `cisco.ios` collection

Install collection:

```bash
ansible-galaxy collection install cisco.ios

---
