# 🤖 Comandos

> 🌍 [English version → Commands](../en/commands.md)

---

## Leyenda de Permisos

| Badge | Significado |
|-------|------------|
| 🟢 Todos | Cualquier miembro puede usarlo |
| 🟡 Admin | Requiere permiso de Administrador o Gestionar Servidor |
| 🔴 Mod | Requiere permiso de Moderar Miembros o Banear |

---

## 🛠️ Utilidad

| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/help` | 🟢 Todos | Muestra la guía del bot con todos los comandos | `/help` |
| `/update` | 🟢 Todos | Muestra la última actualización del bot | `/update` |

---

## 🏛️ Administración

### Gestión del Servidor
| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/dashboard-server` | 🟡 Admin | Ver el panel de control del servidor | `/dashboard-server` |
| `/edit-server` | 🟡 Admin | Editar nombre o descripción del servidor | `/edit-server nombre:Mi Servidor` |

### Canales
| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/create-channel` | 🟡 Admin | Crear un nuevo canal de texto o voz | `/create-channel nombre:anuncios tipo:texto` |
| `/edit-channel` | 🟡 Admin | Editar la configuración de un canal | `/edit-channel canal:#general nombre:chat` |
| `/delete-channel` | 🟡 Admin | Eliminar un canal del servidor | `/delete-channel canal:#canal-viejo` |

### Categorías
| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/create-category` | 🟡 Admin | Crear una nueva categoría | `/create-category nombre:Moderación` |
| `/edit-category` | 🟡 Admin | Editar nombre de una categoría | `/edit-category categoría:General nombre:Principal` |
| `/delete-category` | 🟡 Admin | Eliminar una categoría | `/delete-category categoría:Antigua` |

### Roles
| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/create-role` | 🟡 Admin | Crear un rol con nombre y color | `/create-role nombre:VIP color:#ffb6c1` |
| `/edit-role` | 🟡 Admin | Editar nombre o color de un rol | `/edit-role rol:@VIP nombre:Premium` |
| `/delete-role` | 🟡 Admin | Eliminar un rol | `/delete-role rol:@RolAntiguo` |

### Eventos
| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/create-event` | 🟡 Admin | Crear un evento programado | `/create-event nombre:Torneo fecha:2026-04-01` |
| `/edit-event` | 🟡 Admin | Editar un evento existente | `/edit-event evento:Torneo nombre:Gran Torneo` |
| `/delete-event` | 🟡 Admin | Cancelar un evento | `/delete-event evento:Torneo` |

### Emojis y Stickers
| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/create-emoji` | 🟡 Admin | Añadir un emoji al servidor | `/create-emoji nombre:caatffee imagen:url` |
| `/create-sticker` | 🟡 Admin | Añadir un sticker al servidor | `/create-sticker nombre:cafe imagen:url` |

---

## ⚙️ Configuración

| Comando | Permisos | Descripción |
|---------|----------|-------------|
| `/set-welcome activar` | 🟡 Admin | Activa el sistema de bienvenida |
| `/set-welcome desactivar` | 🟡 Admin | Desactiva la bienvenida |
| `/set-welcome ver` | 🟡 Admin | Muestra la configuración actual |
| `/set-goodbye activar` | 🟡 Admin | Activa el sistema de despedida |
| `/set-goodbye desactivar` | 🟡 Admin | Desactiva la despedida |
| `/set-goodbye ver` | 🟡 Admin | Muestra la configuración actual |
| `/set-logs` | 🟡 Admin | Configura el canal de logs del servidor |

> 📖 Ver guía completa: [Bienvenida y Despedida](bienvenida-y-despedida.md) · [Moderación y Logs](moderacion.md)

---

## 🛡️ Moderación

| Comando | Permisos | Descripción | Ejemplo |
|---------|----------|-------------|---------|
| `/ban` | 🔴 Mod | Banear permanentemente a un usuario | `/ban usuario:@User razón:Spam` |
| `/unban` | 🔴 Mod | Desbanear a un usuario por su ID | `/unban id:123456789` |
| `/kick` | 🔴 Mod | Expulsar a un usuario del servidor | `/kick usuario:@User razón:Comportamiento` |
| `/warn` | 🔴 Mod | Dar una advertencia formal a un usuario | `/warn usuario:@User razón:Insultos` |
| `/timeout` | 🔴 Mod | Silenciar temporalmente a un usuario | `/timeout usuario:@User duración:10m` |
| `/unmute` | 🔴 Mod | Quitar el silencio a un usuario | `/unmute usuario:@User` |
| `/lock` | 🔴 Mod | Bloquear el canal actual | `/lock razón:Flood` |
| `/unlock` | 🔴 Mod | Desbloquear el canal | `/unlock` |
| `/slowmode` | 🔴 Mod | Activar modo lento en un canal | `/slowmode segundos:10` |
| `/purge` | 🔴 Mod | Borrar mensajes en masa | `/purge cantidad:50` |
| `/purge-user` | 🔴 Mod | Borrar mensajes de un usuario específico | `/purge-user usuario:@User cantidad:20` |

---

## 💡 Tips

> - Todos los comandos usan `/` (slash commands), no requieren prefijo de texto.
> - Puedes ver los parámetros de cada comando directamente en Discord al escribir `/`.
> - Si un comando no responde, verifica que el bot tenga los permisos necesarios en ese canal.

---

← [Guía de Inicio](guia-de-inicio.md) | [Moderación →](moderacion.md)
