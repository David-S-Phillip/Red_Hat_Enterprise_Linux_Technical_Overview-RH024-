# Red Hat Web Console (Cockpit) & Systemd Service Management

Summary of system management workflows, server monitoring via the Red Hat Web Console (Cockpit), and service management using `systemctl` covered during RH024.

---

## 1. Red Hat Web Console (Cockpit) Overview

The Red Hat Web Console is a web-based management interface designed for inspecting and administering RHEL servers remotely.

* **Default Access Port:** `https://<server-ip>:9090`
* **Service Name:** `cockpit.socket`

### Core Capabilities
- **System Overview:** Monitor CPU, memory, disk I/O, and network usage in real time.
- **Service & Logs Management:** Inspect systemd services, inspect journal logs, and start/stop daemons.
- **Storage Management:** Configure storage pools, RAID arrays, LVM logical volumes, and mount points.
- **Networking:** Manage firewall settings (`firewalld`), network interfaces, and bonded interfaces.
- **Account Management:** Add, modify, or lock local user accounts.
- **Terminal Access:** Access an integrated full-featured root/user terminal directly inside the browser.

### Service Activation
```bash
# Enable and start the Cockpit web service immediately
sudo systemctl enable --now cockpit.socket