# 🛡️ Moderation & Logs

> 🌍 [Versión en español → Moderación](../es/moderacion.md)

---

## Moderation System

Caatffee includes a full moderation system with logging for all actions.

---

## 🔨 Moderation Commands

### `/ban` — Ban a user
Permanently bans a user and prevents them from rejoining.

```
/ban user:@User reason:Reason for ban
```

| Parameter | Required | Description |
|-----------|----------|-------------|
| `user` | ✅ Yes | The user to ban |
| `reason` | ❌ No | Reason (appears in logs) |

> ⚠️ You can only ban users with a **lower** role than yours.

---

### `/unban` — Unban a user
Revokes a ban using the user's Discord ID.

```
/unban id:123456789012345678
```

> 💡 To get an ID: Discord → Settings → Advanced → Enable Developer Mode → right-click the user → "Copy ID"

---

### `/kick` — Kick a user
Removes the user from the server (they can rejoin with an invite).

```
/kick user:@User reason:Reason
```

---

### `/warn` — Warn a user
Issues a formal warning. Warnings are saved in the database.

```
/warn user:@User reason:Reason for warning
```

---

### `/timeout` — Temporarily mute
Prevents the user from sending messages for a set amount of time.

```
/timeout user:@User duration:10m reason:Flooding
```

**Valid duration formats:** `60s`, `10m`, `2h`, `1d`

---

### `/unmute` — Remove timeout
Removes the active timeout from a user.

```
/unmute user:@User
```

---

### `/lock` — Lock channel
Prevents members (without special permissions) from sending messages in the current channel.

```
/lock reason:Heated argument, pause needed
```

---

### `/unlock` — Unlock channel
Restores normal channel permissions.

```
/unlock
```

---

### `/slowmode` — Slow mode
Sets a cooldown between messages in the channel.

```
/slowmode seconds:30
```

> Use `/slowmode seconds:0` to disable it.

---

### `/purge` — Bulk delete messages
Deletes multiple messages from the channel at once.

```
/purge amount:50
```

> ⚠️ Only works on messages less than 14 days old (Discord limitation).

---

### `/purge-user` — Delete a user's messages
Deletes recent messages from a specific user.

```
/purge-user user:@User amount:20
```

---

## 🔔 Log System

Logs automatically record moderation actions and server events.

### Setup

```
/set-logs channel:#log-channel
```

### What gets logged?

| Event | Description |
|-------|-------------|
| 🔨 Ban / Unban | Who banned whom and why |
| 👢 Kick | Kicks with reason |
| ⚠️ Warn | Warnings issued |
| 🔇 Timeout / Unmute | Muted users and duration |
| 🔒 Lock / Unlock | Locked and unlocked channels |
| 📝 Deleted messages | Content of the deleted message |
| ✏️ Edited messages | Before and after the edit |
| 📥 Member joined | With user info |
| 📤 Member left | With roles they had |
| 🎭 Role changes | Roles assigned or removed |
| 📁 Channel created/deleted | Name and type |

### Log example

```
🔨 BAN — ElJose banned SpamUser
Reason: Mass spam in #general
User ID: 123456789012345678
```

---

## 💡 Best Practices

1. **Always add a reason** when banning or warning — it appears in logs and the user can see it.
2. **Use timeout before ban** for minor infractions — give a second chance.
3. **Set up a dedicated log channel** with access only for moderators.
4. **Review warnings** before escalating to a ban using `/dashboard-server`.

---

← [Commands](commands.md) | [Welcome & Goodbye →](welcome-and-goodbye.md)
