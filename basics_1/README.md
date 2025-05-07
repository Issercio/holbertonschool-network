# Network Basics

<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu"/>
  <img src="https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="Bash"/>
</p>

## 📋 Description

This repository contains a collection of Bash scripts for network configuration and monitoring in Ubuntu environments. These scripts demonstrate fundamental network operations such as modifying host resolutions, displaying active IP addresses, and creating network listeners.

## 📁 Project Structure

| Script | Description |
|--------|-------------|
| [`0-change_your_home_IP`](./basics_1/0-change_your_home_IP) | Configures host resolution: `localhost` → `127.0.0.2` and `facebook.com` → `8.8.8.8` |
| [`1-show_attached_IPs`](./basics_1/1-show_attached_IPs) | Displays all active IPv4 addresses on the machine |
| [`2-port_listening_on_localhost`](./basics_1/2-port_listening_on_localhost) | Creates a listener on port 98 of localhost |

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/username/holbertonschool-network.git

# Navigate to the project directory
cd holbertonschool-network/basics_1

# Make scripts executable
chmod +x 0-change_your_home_IP 1-show_attached_IPs 2-port_listening_on_localhost
```

## 💻 Usage

### Change Home IP

Modifies host resolutions in the `/etc/hosts` file:

```bash
sudo ./0-change_your_home_IP
```

⚠️ **Warning**: This will modify your system's network configuration. Remember to revert changes to `localhost` to avoid system issues.

**Before:**
```
ping localhost    # resolves to 127.0.0.1
ping facebook.com # resolves to actual Facebook IP
```

**After:**
```
ping localhost    # resolves to 127.0.0.2
ping facebook.com # resolves to 8.8.8.8
```

### Show Attached IPs

Displays all active IPv4 addresses:

```bash
./1-show_attached_IPs
```

**Example output:**
```
10.0.2.15
127.0.0.1
```

### Port Listening

Creates a network listener on port 98:

```bash
# Terminal 1: Start the listener
sudo ./2-port_listening_on_localhost

# Terminal 2: Connect to the listener
telnet localhost 98
```

Any text entered in Terminal 2 will appear in Terminal 1.

## 🛠️ Requirements

- Ubuntu operating system
- Bash shell
- Root privileges (for certain scripts)
- Network utilities (`nc`, `ifconfig` or `ip`)

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

- **Your Name** - [GitHub Profile](https://github.com/yourusername)