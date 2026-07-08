# SSH Configuration

## Objective

Configure Secure Shell (SSH) to remotely manage the Linux Mint server from a Windows computer using PuTTY.

---

## Software Used

- Linux Mint
- OpenSSH Server
- PuTTY
- Windows 11

---

## Installation

Update the package list:

```bash
sudo apt update
```

Install the OpenSSH Server:

```bash
sudo apt install openssh-server
```

---

## Check SSH Status

Verify that the SSH service is running:

```bash
sudo systemctl status ssh
```

Enable SSH to start automatically:

```bash
sudo systemctl enable ssh
```

---

## Find the Server IP Address

```bash
ip addr
```

Example:

```
192.168.1.100
```

---

## Connect Using PuTTY

1. Open PuTTY on Windows.
2. Enter the Linux server IP address.
3. Use port **22**.
4. Select **SSH** as the connection type.
5. Click **Open**.
6. Log in using your Linux username and password.

---

## Verification

Check the hostname:

```bash
hostname
```

Check the current user:

```bash
whoami
```

Display the current directory:

```bash
pwd
```

---

## Notes

- The server is accessible only on the local network.
- The server uses a dynamic IP address assigned by DHCP.
- No port forwarding or SSH tunneling has been configured.

---

## Result

Remote SSH access from Windows to the Linux Mint server was successfully configured using PuTTY.
