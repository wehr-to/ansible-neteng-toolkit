# 🔧 ansible-neteng

A practical network automation toolkit using Ansible — featuring playbooks, roles, Jinja2 templates, and scripts for managing Cisco and other network infrastructure.

## 📌 Purpose

This repo automates routine and advanced network operations using Ansible. It's designed for:

- Network engineers transitioning into automation
- DevNetOps professionals maintaining hybrid environments
- Homelabbers building real-world operational muscle

## 📁 Folder Overview

| Folder         | Description                                                     |
|----------------|-----------------------------------------------------------------|
| `inventories/`  | Static/dynamic inventories for lab and prod environments       |
| `playbooks/`    | Core automation tasks: backups, baselines, ACLs, interface mgmt|
| `roles/`        | Modular reusable roles (config push, SNMP, NTP, etc.)          |
| `vars/`         | Centralized input files for ACLs, SNMP, and NTP                |
| `templates/`    | Jinja2 configs for banners, interfaces, login messages         |
| `utils/`        | Python and shell tools for parsing backups, diffing configs    |
| `docs/`         | Setup guides, playbook design notes, Ansible command cheats    |

## 🚀 Playbooks Included

- `baseline-config.yml`: Applies banner, hostname, domain name
- `backup-configs.yml`: Backs up configs from all hosts
- `interface-audit.yml`: Collects status of all physical interfaces
- `deploy-acls.yml`: Pushes ACLs to routers or switches from `vars/`

## 🧠 Features

- Jinja2 templating for reusable device configs
- Host grouping by platform, site, or region
- Role-based modular structure
- Safe, idempotent automation for Cisco-like platforms
- Scripted tools to diff pre/post state and parse configs

## 🧰 Requirements

- Ansible 2.9+
- `netmiko` or `paramiko` (for CLI-based modules)
- Cisco IOS/IOS-XE/NX-OS devices (or simulation via EVE-NG/GNS3)

## ✅ Ideal Use Cases

- Automating switch/router provisioning
- Backing up configs regularly
- Enforcing NTP, SNMP, AAA standards
- Building a DevNet or CCNP Automation lab

## 🔒 Security Notes

- Do not hardcode secrets or credentials in playbooks.
- Use Ansible Vault or `.env` injection.
- `group_vars/all.yaml` supports abstraction for sensitive values.

## 🚧 Roadmap

- [ ] Add Ansible Vault integration example
- [ ] Add NetBox dynamic inventory integration
- [ ] Add Python-based playbook validation (using `ansible-lint`)
- [ ] Add GitHub Actions pipeline for syntax validation

