# Linux Mint Home Server Installation

## Objective

Build a Home Linux Server using Linux Mint in VMware Workstation to learn Linux administration, networking, SSH, Samba, Docker, and server management.

---

## Software Used

- Linux Mint
- VMware Workstation
- PuTTY
- Windows 11

---

## Virtual Machine Configuration

| Setting | Value |
|---------|-------|
| Operating System | Linux Mint |
| RAM | 4 GB |
| CPU | 2 Cores |
| Storage | 40 GB |
| Network Adapter | Bridged |
| IP Configuration | Static IP |

---

## Installation Steps

1. Download the Linux Mint ISO.
2. Create a new virtual machine in VMware Workstation.
3. Allocate CPU, RAM, and storage.
4. Configure the network adapter to **Bridged Mode**.
5. Install Linux Mint.
6. Create a user account.
7. Update the operating system.
8. Install OpenSSH Server.
9. Configure a static IP address.
10. Restart the virtual machine.

---

## Verification

Check the operating system:

```bash
cat /etc/os-release
```

Check the IP address:

```bash
ip addr
```

Check the hostname:

```bash
hostname
```

Verify the SSH service:

```bash
systemctl status ssh
```

---

## Result

Linux Mint was successfully installed in VMware Workstation using a Bridged network adapter. A static IP address was configured, and the system is ready for remote administration and additional server services.
