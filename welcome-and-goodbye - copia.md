# 🌸 Welcome & Goodbye

> 🌍 [Versión en español → Bienvenida y Despedida](../es/bienvenida-y-despedida.md)

---

## What is this system?

Caatffee can automatically send a message in a channel when:
- 📥 **Someone joins** the server → **welcome** message
- 📤 **Someone leaves** the server → **goodbye** message

Each message is sent as an **embed** with the user's avatar, server stats, and the text you configure.

---

## 🌸 Setting Up Welcome

### From Discord (command)

**Enable:**
```
/set-welcome activar channel:#welcome
```

**With all options:**
```
/set-welcome activar channel:#welcome title:New member! message:Welcome to {server}, {user}! 🎉 color:#ffb6c1
```

**Disable:**
```
/set-welcome desactivar
```

**View current config:**
```
/set-welcome ver
```

---

### From the Official Website

1. Go to [caatffee.github.io/Caatffee](https://caatffee.github.io/Caatffee/)
2. Sign in with Discord
3. Open your server's panel
4. Click **🌸 Bienvenida** (Welcome)
5. Fill in the fields and click **✅ Activar**

---

## 👋 Setting Up Goodbye

### From Discord (command)

**Enable:**
```
/set-goodbye activar channel:#goodbye
```

**With all options:**
```
/set-goodbye activar channel:#goodbye title:A member left... message:Goodbye, {user}. We'll miss you in {server}! 👋 color:#9b8ea8
```

**Disable:**
```
/set-goodbye desactivar
```

**View current config:**
```
/set-goodbye ver
```

---

## 📝 Available Variables

You can use these variables in the **message** field:

| Variable | Replaced with |
|----------|--------------|
| `{usuario}` | Member mention (`@User`) in welcome, username in goodbye |
| `{servidor}` | Server name |

**Example:**
```
Welcome to {servidor}, {usuario}! We're so happy to have you ☕
```
Becomes:
```
Welcome to My Server, @ElJose! We're so happy to have you ☕
```

---

## 🎨 Embed Options

| Field | Description | Required |
|-------|-------------|----------|
| `canal` | Channel where the message will be sent | ✅ Yes |
| `mensaje` | Embed text (supports variables) | ❌ No (has a default) |
| `titulo` | Embed title | ❌ No |
| `imagen` | Image URL shown in the embed | ❌ No |
| `color` | Side border color in HEX (`#ffb6c1`) | ❌ No |

---

## 📋 What the embed shows

### Welcome
- 🖼️ New member's avatar (thumbnail)
- 💬 Your custom message with `{user}` and `{server}`
- 👤 User tag
- 👥 Total member count after joining
- 📅 How long ago their account was created

### Goodbye
- 🖼️ Leaving member's avatar
- 💬 Your custom message
- 👤 User tag
- 👥 Remaining member count
- 📅 How long ago they joined the server

---

## ⚠️ Requirements

- The bot must be in the server
- The bot must have **Send Messages** and **Embed Links** in the configured channel
- Only **administrators and the server owner** can configure this system

---

## 🛠️ Troubleshooting

| Problem | Solution |
|---------|---------|
| Welcome message not sending | Check it's enabled with `/set-welcome ver` |
| Bot doesn't have permissions | Give it Send Messages and Embed Links in the channel |
| Channel doesn't appear on the website | The bot can't see that channel — check channel permissions |
| "Bot not available" on website | The bot is offline or restarting |

---

← [Moderation](moderation.md) | [Web Panel →](web-panel.md)
