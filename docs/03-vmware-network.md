# VMware Bridged Network Configuration

## Objective

Configure the Linux Mint virtual machine to communicate directly with the local network using VMware Bridged Networking.

---

## Environment

- Host Operating System: Windows 11
- Virtualization Software: VMware Workstation
- Guest Operating System: Linux Mint
- Network Mode: Bridged

---

## Network Diagram

```text
                Internet
                    │
              Home Router
                    │
        ┌───────────┴───────────┐
        │                       │
   Windows 11 PC         Linux Mint VM
      (Host)              (Guest)
        │                       │
        └──── VMware Bridged ───┘
```

---

## Why Bridged Mode?

Bridged mode allows the virtual machine to appear as a separate device on the same local network as the host computer.

Benefits:

- Receives its own IP address from the router (DHCP)
- Can communicate with other devices on the LAN
- Allows SSH connections from the host computer
- Useful for testing network services

---

## Verify Network Configuration

Display the IP address:

```bash
ip addr
```

Display the default gateway:

```bash
ip route
```

Test internet connectivity:

```bash
ping 8.8.8.8
```

Test DNS resolution:

```bash
ping google.com
```

---

## Notes

- The VM receives its IP address automatically using DHCP.
- The IP address may change after restarting the VM or router.
- SSH is available only within the local network.

---

## Result

The Linux Mint virtual machine was successfully connected to the local network using VMware Bridged Networking.
