# 🛡️ Moderación y Logs

> 🌍 [English version → Moderation](../en/moderation.md)

---

## Sistema de Moderación

Caatffee incluye un sistema completo de moderación con registro de todas las acciones.

---

## 🔨 Comandos de Moderación

### `/ban` — Banear usuario
Expulsa permanentemente a un usuario e impide que vuelva a entrar.

```
/ban usuario:@Usuario razón:Motivo del ban
```

| Parámetro | Obligatorio | Descripción |
|-----------|-------------|-------------|
| `usuario` | ✅ Sí | El usuario a banear |
| `razón` | ❌ No | Motivo (aparece en los logs) |

> ⚠️ Solo puedes banear a usuarios con un rol **inferior** al tuyo.

---

### `/unban` — Desbanear usuario
Revoca el ban de un usuario usando su ID de Discord.

```
/unban id:123456789012345678
```

> 💡 Para obtener el ID: Discord → Configuración → Avanzado → Modo Desarrollador activado → clic derecho en el usuario → "Copiar ID"

---

### `/kick` — Expulsar usuario
Expulsa al usuario del servidor (puede volver a entrar con una invitación).

```
/kick usuario:@Usuario razón:Motivo
```

---

### `/warn` — Advertir usuario
Envía una advertencia formal. Las advertencias quedan registradas en la base de datos.

```
/warn usuario:@Usuario razón:Motivo de la advertencia
```

---

### `/timeout` — Silenciar temporalmente
Impide al usuario enviar mensajes durante un tiempo determinado.

```
/timeout usuario:@Usuario duración:10m razón:Flood
```

**Formatos de duración válidos:** `60s`, `10m`, `2h`, `1d`

---

### `/unmute` — Quitar silencio
Elimina el timeout activo de un usuario.

```
/unmute usuario:@Usuario
```

---

### `/lock` — Bloquear canal
Impide que los miembros (sin permisos especiales) envíen mensajes en el canal actual.

```
/lock razón:Debate acalorado, pausa necesaria
```

---

### `/unlock` — Desbloquear canal
Restaura los permisos normales del canal.

```
/unlock
```

---

### `/slowmode` — Modo lento
Establece un tiempo de espera entre mensajes en el canal.

```
/slowmode segundos:30
```

> Usa `/slowmode segundos:0` para desactivarlo.

---

### `/purge` — Borrar mensajes en masa
Elimina múltiples mensajes del canal de una sola vez.

```
/purge cantidad:50
```

> ⚠️ Solo funciona con mensajes de menos de 14 días de antigüedad (limitación de Discord).

---

### `/purge-user` — Borrar mensajes de un usuario
Elimina los mensajes recientes de un usuario específico.

```
/purge-user usuario:@Usuario cantidad:20
```

---

## 🔔 Sistema de Logs

Los logs registran automáticamente las acciones de moderación y los eventos del servidor.

### Configuración

```
/set-logs canal:#canal-de-logs
```

### ¿Qué se registra?

| Evento | Descripción |
|--------|-------------|
| 🔨 Ban / Unban | Quién baneó a quién y por qué |
| 👢 Kick | Expulsiones con razón |
| ⚠️ Warn | Advertencias emitidas |
| 🔇 Timeout / Unmute | Silenciados y duración |
| 🔒 Lock / Unlock | Canales bloqueados y desbloqueados |
| 📝 Mensajes eliminados | Contenido del mensaje borrado |
| ✏️ Mensajes editados | Antes y después de la edición |
| 📥 Miembro entró | Con información del usuario |
| 📤 Miembro salió | Con roles que tenía |
| 🎭 Cambios de rol | Roles asignados o quitados |
| 📁 Canal creado/eliminado | Nombre y tipo |

### Ejemplo de log

```
🔨 BAN — ElJose baneó a SpamUser
Razón: Spam masivo en #general
ID Usuario: 123456789012345678
```

---

## 💡 Buenas Prácticas

1. **Siempre añade una razón** al banear o advertir — aparece en los logs y el usuario puede verla.
2. **Usa timeout antes de ban** para infracciones menores — da una segunda oportunidad.
3. **Configura un canal de logs** dedicado con acceso solo para moderadores.
4. **Revisa las advertencias** antes de escalar a ban con `/dashboard-server`.

---

← [Comandos](comandos.md) | [Bienvenida y Despedida →](bienvenida-y-despedida.md)
