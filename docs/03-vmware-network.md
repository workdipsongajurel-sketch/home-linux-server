# VMware Bridged Network Configuration

## Objective

Configure VMware Bridged Networking to allow a Windows virtual machine to connect to the Linux Mint host using SSH.

---

## Environment

- Host Operating System: Linux Mint
- Virtualization Software: VMware Workstation
- Guest Operating System: Windows
- Network Mode: Bridged
- Remote Access Tool: PuTTY

---

## Network Diagram

```text
                 Internet
                     │
               Home Router
                     │
          ┌──────────┴──────────┐
          │                     │
    Linux Mint Host       Windows Virtual Machine
     (SSH Server)             (PuTTY Client)
          │                     │
          └──── VMware Bridged ─┘
```

---

## How It Works

- Linux Mint runs the OpenSSH Server.
- Windows runs PuTTY as the SSH client.
- Both systems are connected through VMware Bridged Networking.
- Windows connects to the Linux Mint host using its local IP address.

---

## Verify the Connection

Find the Linux Mint IP address:

```bash
ip addr
```

Check the SSH service:

```bash
sudo systemctl status ssh
```

From Windows, open PuTTY and connect to:

- Host Name: Linux Mint IP address
- Port: 22
- Connection Type: SSH

---

## Result

The Windows virtual machine successfully connected to the Linux Mint host using SSH over the local network.
