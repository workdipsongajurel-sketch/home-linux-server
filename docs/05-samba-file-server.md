# Samba File Server

## Objective

Install and configure Samba on Linux Mint to share files with Windows computers on the local network.

---

## Environment

| Component | Value |
|----------|-------|
| Host OS | Windows 11 |
| Guest OS | Linux Mint |
| Network | Bridged (DHCP) |
| File Sharing | Samba |

---

## Install Samba

Update packages:

```bash
sudo apt update
```

Install Samba:

```bash
sudo apt install samba
```

Check the Samba version:

```bash
smbd --version
```

---

## Check Samba Status

```bash
sudo systemctl status smbd
```

Enable Samba at startup:

```bash
sudo systemctl enable smbd
```

---

## Result

Samba was successfully installed and is ready for configuration.
