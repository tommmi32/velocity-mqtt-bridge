# 🚀 Velocity MQTT Bridge

<p align="center">

<img src="https://img.shields.io/badge/Minecraft-Velocity-green?style=for-the-badge&logo=minecraft">
<img src="https://img.shields.io/badge/Java-17%2B-orange?style=for-the-badge&logo=openjdk">
<img src="https://img.shields.io/badge/MQTT-Compatible-blue?style=for-the-badge&logo=eclipse-mosquitto">
<img src="https://img.shields.io/badge/Home%20Assistant-Compatible-41BDF5?style=for-the-badge&logo=homeassistant">

</p>

<p align="center">
A lightweight Velocity Proxy plugin that connects your Minecraft network with MQTT-based automation systems.
</p>

---

# 📡 About

**Velocity MQTT Bridge** is a lightweight plugin for **Velocity Proxy** that publishes Minecraft events through an MQTT broker.

It allows external applications and automation platforms to receive real-time information from your Minecraft network.

Perfect for:

🏠 Home Assistant integrations  
📱 Mobile notifications  
💡 Smart home automations  
📊 Dashboards  
🤖 Custom bots and services  

---

# ✨ Features

| Feature | Supported |
|---|---|
| 👤 Player join events | ✅ |
| 🚪 Player leave events | ✅ |
| 🔄 Server switch events | ✅ |
| 👥 Online player tracking | ✅ |
| 📡 MQTT publishing | ✅ |
| 🏠 Home Assistant integration | ✅ |
| ⚡ Lightweight performance | ✅ |
| 🔧 Configurable topics | ✅ |

---

# 🧩 Requirements

Before installation you need:

- 🟢 Velocity Proxy
- ☕ Java 17 or newer
- 📡 MQTT Broker

Recommended MQTT brokers:

- Mosquitto
- EMQX
- Home Assistant MQTT Broker

---

# 📥 Installation

### 1️⃣ Download plugin

Download the latest release:

```
velocity-mqtt-bridge.jar
```

---

### 2️⃣ Install plugin

Copy the file into:

```
velocity/plugins/
```

Restart your Velocity Proxy.

---

### 3️⃣ Configure MQTT

After first startup, the plugin creates:

```
plugins/velocity-mqtt-bridge/config.yml
```

Edit your MQTT settings:

```yaml
mqtt:
  host: "localhost"
  port: 1883
  username: ""
  password: ""

topics:
  event: "minecraft/velocity/event"
  players: "minecraft/velocity/players"
  online: "minecraft/velocity/online"
  status: "minecraft/velocity/status"
```

Restart Velocity.

---

# 📬 MQTT Topics

## 👤 Player Events

Topic:

```
minecraft/velocity/event
```

Example:

```json
{
  "event": "join",
  "player": "Steve",
  "server": "survival",
  "online": 1,
  "proxy": "main"
}
```

---

## 👥 Online Players

Topic:

```
minecraft/velocity/players
```

Example:

```json
{
  "players": [
    "Steve",
    "Alex"
  ],
  "online": 2
}
```

---

## 🟢 Proxy Status

Topic:

```
minecraft/velocity/status
```

Example:

```json
{
  "status": "online",
  "proxy": "main"
}
```

---

# 🏠 Home Assistant Integration

Velocity MQTT Bridge can be used with Home Assistant to create:

<div>

🟢 Minecraft online status sensors  
🟢 Player activity notifications  
🟢 Smart display widgets  
🟢 Voice assistant notifications  
🟢 Smart home automations  

</div>


Example automation:

```
Player joins Minecraft server
          ↓
MQTT message published
          ↓
Home Assistant receives event
          ↓
Notification / Light / Automation triggered
```

---

# 🏗️ Architecture

```
🎮 Minecraft Client
          |
          |
          v
🚀 Velocity Proxy
          |
          |
          v
📡 Velocity MQTT Bridge
          |
          |
          v
📨 MQTT Broker
          |
          |
          v
🏠 Home Assistant / Other Systems
```

---

# 🛠️ Build From Source

Clone repository:

```bash
git clone https://github.com/YOUR_USERNAME/velocity-mqtt-bridge.git
```

Build:

```bash
mvn clean package
```

Output:

```
target/velocity-mqtt-bridge.jar
```

---

# 📋 Supported Versions

| Component | Version |
|-|-|
| Velocity | 3.x |
| Java | 17+ |
| Minecraft | 1.21+ |
| MQTT | 3.1 / 5.0 |

---

# 🤝 Contributing

Contributions are welcome!

If you have ideas, improvements or bug reports:

⭐ Open an issue  
⭐ Submit a pull request  

---

# 📜 License

Released under the **MIT License**.

You are free to use, modify and distribute this project.

---

# 👨‍💻 Author

Created by:

**Tomáš Mészáros**

Minecraft + MQTT + Home Automation enthusiast.

---

<p align="center">

⭐ If this project helped you, consider giving it a star!

</p>
