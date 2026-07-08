# OpenSSH Server Configuration

## Objective

Install and configure the OpenSSH Server on a Linux Mint virtual machine to allow remote administration from a Windows computer using PuTTY.

---

## Environment

| Component | Value |
|----------|-------|
| Host OS | Windows 11 |
| Guest OS | Linux Mint |
| Virtualization | VMware Workstation |
| SSH Client | PuTTY |
| Network | Bridged |
| IP Assignment | DHCP |

---

## Install OpenSSH Server

Update the package list:

```bash
sudo apt update
```

Install OpenSSH Server:

```bash
sudo apt install openssh-server
```

---

## Check the SSH Service

Check if the service is running:

```bash
sudo systemctl status ssh
```

Start the service if necessary:

```bash
sudo systemctl start ssh
```

Enable SSH to start automatically at boot:

```bash
sudo systemctl enable ssh
```

---

## Find the Server IP Address

Run:

```bash
ip addr
```

Example:

```
192.168.1.105
```

---

## Connect from Windows

1. Open PuTTY.
2. Enter the Linux Mint IP address.
3. Use port **22**.
4. Click **Open**.
5. Log in with your Linux username and password.

---

## Verify the Connection

Display the hostname:

```bash
hostname
```

Display the current user:

```bash
whoami
```

Display the current directory:

```bash
pwd
```

---

## Result

The Windows computer successfully connected to the Linux Mint virtual machine using SSH over the local network.
