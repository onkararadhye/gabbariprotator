
# 🚀 GabbarIPRotator V-1.0 - Tor-Based IP Rotator

**GabbarIPRotator** is a Bash-based tool that automatically changes your public IP address using the Tor network at custom intervals. It allows you to appear from different countries by rotating IPs through Tor circuits.

> ⚠️ Requires root privileges.  
> ⚠️ Works only if Tor is installed and configured correctly.

---

## 🛠️ Features

- 🔄 Change your IP address on a timed loop
- 🌐 Get current location using `curl` + `ipinfo.io` or `ip-api.com`
- 🧅 Integrates with Tor network using the ControlPort
- 🗝️ Prompts for authentication password for Tor
- 📦 Installs required packages (`curl`, `jq`, `tor`, `netcat-traditional`) automatically
- 📑 Simple, interactive shell interface
- ✅ Root user validation and dependency checks

---

## 🔧 Installation

Clone this repository and run the script:

```bash
git clone https://github.com/onkararadhye/gabbariprotator.git
cd gabbariprotator
chmod +x gabbar.sh
sudo ./gabbar.sh
```

It will install:

- `tor`
- `jq`
- `curl`
- `netcat-traditional`

---

## ⚙️ Usage

```bash
sudo ./gabbar.sh
```

Then follow the prompts:

- **Enter interval (in seconds)**: Time between IP changes
- **Enter number of changes**: `0` = infinite

**Example output:**

```
🔁 Changing IP 1 of 5...
🌐 Current IP: 185.220.101.131
📍 Location: Croatia, Sisak
⏳ Waiting 10 seconds...
```


---

## 🧪 Use Cases

- ✅ IP rotation for scraping or automation
- 🔐 Basic anonymity for CLI traffic
- 🌍 Testing geo-restricted services
- 🛡️ Cybersecurity researchers and pen-testers

---

## 🧯 Troubleshooting

| Problem | Solution |
|--------|----------|
| `tor.service not found` | Install `tor` with `sudo apt install tor` |
| `Connection refused on port 9051` | Ensure `ControlPort` is enabled in `torrc` |
| `Too many arguments to AUTHENTICATE` | Avoid spaces or use double quotes around the password |
| `jq: command not found` | Install using `sudo apt install jq` |
| IP doesn’t change | Tor sometimes rotates within same subnet. Use bridges or wait longer. |

---

## ⚠️ Root Permission Required

The script needs to:

- Install packages
- Restart Tor
- Bind to privileged ports

Use `sudo` to run it. Do **not** run as a regular user.

---

## 👤 Author

**Onkar Aradhye**  
Ethical Hacker | Android Dev | Linux Enthusiast

📧 onkararadhye.2004@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/onkararadhye)

---

## 📄 License

MIT License

```
MIT License

Copyright (c) 2025 Onkar Aradhye

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction...
```

---

## 🙏 Acknowledgements

- The Tor Project (https://www.torproject.org/)
- ipinfo.io & ip-api.com for location APIs
- Open-source Linux CLI community
