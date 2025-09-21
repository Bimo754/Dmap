# 🤔 What is this?

![](/Video/dmap.gif)

Dmap is a port scanning script designed to quickly discover open TCP ports <ins>with haste</ins>, utilizing the tool [nmap](https://github.com/nmap/nmap)

<br>

# ✨ Features

Dmap is mostly used on HTB and TryHackMe machines, where speed is important to get “first blood.”

Simply supply an IP address, and let it do the rest. ;)

It will probe all open TCP ports and then perform version and script scans.


# 🛠️ Installation

1. Ensure [nmap](https://github.com/nmap/nmap) is installed on your system.
2. Clone the repository and run the installer
```sh
git clone https://github.com/Bimo754/Dmap
cd Dmap
chmod +x install.sh
sudo ./install.sh
```

<br>

# 📖 Usage

```sh
dmap -h
```
**Usage**
```sh
Usage:
	dmap -a <ip> [options]

Options:
	-a <ip>	Target IP address to scan
	-s <min_rate>	Minimum packet rate for scanning (default: 500)
	-A		Enable OS detection, version detection, script scanning, and traceroute
	-T<0-5>		Timing template for scan speed (default: 3)
```

## Scan a target

```sh
dmap -a <ip>
```

# Examples

Scan 127.0.0.1

```sh
dmap -a 127.0.0.1
```

Scan 127.0.0.1 with `-A`

```sh
dmap -a 127.0.0.1 -A
```

Scan 127.0.0.1 with `-A` and `-T5`

```sh
dmap -a 127.0.0.1 -A -T5
```
