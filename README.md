# Red Hat Enterprise Linux Technical Overview (RH024) — Learning & Practice Log

A hands-on technical log documenting my journey through the **Red Hat Enterprise Linux Technical Overview (RH024)** course, terminal configuration practice, and foundational Linux system administration skills.

---
### WTC tracking code
WTC-YF84PH2W

## Overview

This repository serves as a public record of my practical learning with Enterprise Linux concepts, core system tools, system management workflows, and text manipulation utilities.

* **Course:** Red Hat Enterprise Linux Technical Overview (RH024)
* **OS Environment:** Linux / Red Hat Enterprise Linux (RHEL)
* **Focus Areas:** Core CLI Navigation, Vim Editing, System Services, Storage Basics, and Package Management

---

## Key Topics Covered & Hands-On Practice

### 1. Command Line Foundations & Text Editing
- **Terminal Navigation:** Executing fundamental Linux file manipulation, directory traversal, and process inspection commands.
- **Learning how to use VIM (`vimtutor`):** Completed full interactive Vim practice sessions, this gave the basics of vim:
    - Navigation keys (`h`, `j`, `k`, `l`) and word movement (`w`, `b`).
    - Text insertion, deletion (`x`, `dw`, `dd`), and replacement (`r`, `cw`).
    - Search, replace patterns (`/`, `?`), and visual line selection.
    - File saving, quitting (`:w`, `:q!`, `:wq`), and buffer management.

### 2. System Architecture & Management
- **Image Mode & Containerized RHEL:** Understanding `bootc` for transactional OS updates and containerized image-based Linux deployments.
- **RHEL Web Console (Cockpit):** Managing system performance, network interfaces, storage, and system services via the web GUI interface.
- **System Services (`systemd`):** Monitoring system logs, inspecting service statuses, and starting/stopping system daemons.

### 3. Monitoring & Security Fundamentals
- **Red Hat Insights:** Using Vulnerability Management and Image Builder to inspect system health, track security vulnerabilities, and construct customized deployment images.
- **User & File Permissions:** Managing user access levels, basic file ownership, and execution rights.

---

## Repository Structure

```text
├── README.md                           # Course overview & learning summary
├── 01-cli-and-vim/
│   ├── vimtutor-notes.md              # Vim shortcut reference & command log
│   └── cli-navigation-cheat-sheet.md  # Core bash/RHEL command summaries
├── 02-rhel-systemd-and-console/
│   └── web-console-notes.md           # Cockpit & system service configurations
└── 03-labs-and-terminal-output/
    └── terminal-logs.txt              # Captured terminal output and execution logs
    
```    

## What is Red Hat Enterprise Linux  ? 
Red Hat Enterprise Linux (RHEL) is a Linux operating system designed mainly for businesses and large companies.
Unlike Linux Mint or regular Ubuntu, which are often used on personal computers, RHEL is mainly used on servers and cloud systems.
It helps companies run websites, databases, business applications, and other important services. It is built to be stable, secure, and reliable.
RHEL can run on physical servers, virtual machines, and cloud platforms such as AWS, Microsoft Azure, and Google Cloud.
In simple terms, RHEL is a version of Linux made for businesses that need their computer systems to work safely and reliably.
