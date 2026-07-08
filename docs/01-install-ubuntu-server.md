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
| IP Configuration | Dynamic (DHCP) |

---

## Installation Steps

1. Download the Linux Mint ISO.
2. Create a new virtual machine in VMware Workstation.
3. Allocate CPU, RAM, and storage.
4. Configure the network adapter to Bridged Mode.
5. Install Linux Mint.
6. Create a user account.
7. Update the operating system.
8. Install OpenSSH Server.
9. Connect from Windows using PuTTY over the local network.

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

Check the SSH service:

```bash
systemctl status ssh
```

---

## Notes

- The server receives its IP address automatically using DHCP.
- SSH access is available only within the local network.
- No port forwarding, DDNS, VPN, or SSH tunneling has been configured.

---

## Result

Linux Mint was successfully installed in VMware Workstation using a Bridged network. The server can be managed remotely from another computer on the same local network using SSH.
