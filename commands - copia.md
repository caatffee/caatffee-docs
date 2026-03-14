# 🤖 Commands

> 🌍 [Versión en español → Comandos](../es/comandos.md)

---

## Permission Legend

| Badge | Meaning |
|-------|---------|
| 🟢 Everyone | Any member can use it |
| 🟡 Admin | Requires Administrator or Manage Server |
| 🔴 Mod | Requires Moderate Members or Ban Members |

---

## 🛠️ Utility

| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/help` | 🟢 Everyone | Shows the bot guide with all commands | `/help` |
| `/update` | 🟢 Everyone | Shows the latest bot update | `/update` |

---

## 🏛️ Administration

### Server Management
| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/dashboard-server` | 🟡 Admin | View the server control panel | `/dashboard-server` |
| `/edit-server` | 🟡 Admin | Edit server name or description | `/edit-server name:My Server` |

### Channels
| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/create-channel` | 🟡 Admin | Create a new text or voice channel | `/create-channel name:announcements type:text` |
| `/edit-channel` | 🟡 Admin | Edit a channel's settings | `/edit-channel channel:#general name:chat` |
| `/delete-channel` | 🟡 Admin | Delete a channel from the server | `/delete-channel channel:#old-channel` |

### Categories
| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/create-category` | 🟡 Admin | Create a new category | `/create-category name:Moderation` |
| `/edit-category` | 🟡 Admin | Edit a category name | `/edit-category category:General name:Main` |
| `/delete-category` | 🟡 Admin | Delete a category | `/delete-category category:Old` |

### Roles
| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/create-role` | 🟡 Admin | Create a role with name and color | `/create-role name:VIP color:#ffb6c1` |
| `/edit-role` | 🟡 Admin | Edit a role's name or color | `/edit-role role:@VIP name:Premium` |
| `/delete-role` | 🟡 Admin | Delete a role | `/delete-role role:@OldRole` |

### Events
| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/create-event` | 🟡 Admin | Create a scheduled event | `/create-event name:Tournament date:2026-04-01` |
| `/edit-event` | 🟡 Admin | Edit an existing event | `/edit-event event:Tournament name:Grand Tournament` |
| `/delete-event` | 🟡 Admin | Cancel an event | `/delete-event event:Tournament` |

### Emojis & Stickers
| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/create-emoji` | 🟡 Admin | Add an emoji to the server | `/create-emoji name:caatffee image:url` |
| `/create-sticker` | 🟡 Admin | Add a sticker to the server | `/create-sticker name:coffee image:url` |

---

## ⚙️ Configuration

| Command | Permission | Description |
|---------|------------|-------------|
| `/set-welcome activar` | 🟡 Admin | Enable the welcome system |
| `/set-welcome desactivar` | 🟡 Admin | Disable the welcome system |
| `/set-welcome ver` | 🟡 Admin | Show current welcome config |
| `/set-goodbye activar` | 🟡 Admin | Enable the goodbye system |
| `/set-goodbye desactivar` | 🟡 Admin | Disable the goodbye system |
| `/set-goodbye ver` | 🟡 Admin | Show current goodbye config |
| `/set-logs` | 🟡 Admin | Set the server log channel |

> 📖 See full guide: [Welcome & Goodbye](welcome-and-goodbye.md) · [Moderation & Logs](moderation.md)

---

## 🛡️ Moderation

| Command | Permission | Description | Example |
|---------|------------|-------------|---------|
| `/ban` | 🔴 Mod | Permanently ban a user | `/ban user:@User reason:Spam` |
| `/unban` | 🔴 Mod | Unban a user by ID | `/unban id:123456789` |
| `/kick` | 🔴 Mod | Kick a user from the server | `/kick user:@User reason:Behavior` |
| `/warn` | 🔴 Mod | Give a formal warning to a user | `/warn user:@User reason:Insults` |
| `/timeout` | 🔴 Mod | Temporarily mute a user | `/timeout user:@User duration:10m` |
| `/unmute` | 🔴 Mod | Remove a user's timeout | `/unmute user:@User` |
| `/lock` | 🔴 Mod | Lock the current channel | `/lock reason:Flood` |
| `/unlock` | 🔴 Mod | Unlock the channel | `/unlock` |
| `/slowmode` | 🔴 Mod | Enable slow mode in a channel | `/slowmode seconds:10` |
| `/purge` | 🔴 Mod | Delete messages in bulk | `/purge amount:50` |
| `/purge-user` | 🔴 Mod | Delete a specific user's messages | `/purge-user user:@User amount:20` |

---

## 💡 Tips

> - All commands use `/` (slash commands) — no text prefix needed.
> - You can see each command's parameters directly in Discord as you type `/`.
> - If a command doesn't respond, check that the bot has the necessary permissions in that channel.

---

← [Getting Started](getting-started.md) | [Moderation →](moderation.md)
