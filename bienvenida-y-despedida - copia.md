# 🌸 Bienvenida y Despedida

> 🌍 [English version → Welcome & Goodbye](../en/welcome-and-goodbye.md)

---

## ¿Qué es este sistema?

Caatffee puede enviar automáticamente un mensaje en un canal cuando:
- 📥 **Alguien entra** al servidor → mensaje de **bienvenida**
- 📤 **Alguien sale** del servidor → mensaje de **despedida**

Cada mensaje se envía como un **embed** con el avatar del usuario, estadísticas del servidor y el texto que tú configures.

---

## 🌸 Configurar la Bienvenida

### Desde Discord (comando)

**Activar:**
```
/set-welcome activar canal:#bienvenidas
```

**Con opciones completas:**
```
/set-welcome activar canal:#bienvenidas titulo:¡Nuevo miembro! mensaje:¡Bienvenido/a a {servidor}, {usuario}! 🎉 color:#ffb6c1
```

**Desactivar:**
```
/set-welcome desactivar
```

**Ver configuración actual:**
```
/set-welcome ver
```

---

### Desde la Web Oficial

1. Ve a [caatffee.github.io/Caatffee](https://caatffee.github.io/Caatffee/)
2. Inicia sesión con Discord
3. Abre el panel de tu servidor
4. Haz clic en **🌸 Bienvenida**
5. Rellena los campos y haz clic en **✅ Activar**

---

## 👋 Configurar la Despedida

### Desde Discord (comando)

**Activar:**
```
/set-goodbye activar canal:#despedidas
```

**Con opciones completas:**
```
/set-goodbye activar canal:#despedidas titulo:Un miembro se fue... mensaje:Hasta luego, {usuario}. ¡Te echaremos de menos en {servidor}! 👋 color:#9b8ea8
```

**Desactivar:**
```
/set-goodbye desactivar
```

**Ver configuración actual:**
```
/set-goodbye ver
```

---

## 📝 Variables Disponibles

Puedes usar estas variables en el campo **mensaje**:

| Variable | Se reemplaza por |
|----------|----------------|
| `{usuario}` | Mención del miembro (`@Usuario`) en bienvenida, nombre en despedida |
| `{servidor}` | Nombre del servidor |

**Ejemplo:**
```
¡Bienvenido/a a {servidor}, {usuario}! Ya somos una familia enorme ☕
```
Se convierte en:
```
¡Bienvenido/a a Mi Servidor, @ElJose! Ya somos una familia enorme ☕
```

---

## 🎨 Opciones del Embed

| Campo | Descripción | Obligatorio |
|-------|-------------|-------------|
| `canal` | Canal donde se enviará el mensaje | ✅ Sí |
| `mensaje` | Texto del embed (soporta variables) | ❌ No (tiene uno por defecto) |
| `titulo` | Título del embed | ❌ No |
| `imagen` | URL de imagen que aparece en el embed | ❌ No |
| `color` | Color del borde lateral en HEX (`#ffb6c1`) | ❌ No |

---

## 📋 Lo que muestra el embed

### Bienvenida
- 🖼️ Avatar del nuevo miembro (miniatura)
- 💬 Tu mensaje personalizado con `{usuario}` y `{servidor}`
- 👤 Tag del usuario
- 👥 Número total de miembros tras la entrada
- 📅 Hace cuánto fue creada su cuenta

### Despedida
- 🖼️ Avatar del miembro que se fue
- 💬 Tu mensaje personalizado
- 👤 Tag del usuario
- 👥 Número de miembros que quedan
- 📅 Hace cuánto se unió al servidor

---

## ⚠️ Requisitos

- El bot debe estar en el servidor
- El bot debe tener **Enviar Mensajes** e **Insertar enlaces** en el canal configurado
- Solo **administradores y el dueño** del servidor pueden configurar este sistema

---

## 🛠️ Solución de Problemas

| Problema | Solución |
|----------|---------|
| No se envía el mensaje de bienvenida | Verifica que esté activado con `/set-welcome ver` |
| El bot no tiene permisos | Dale permisos de Enviar Mensajes e Insertar enlaces en el canal |
| El canal no aparece en la web | El bot no puede ver ese canal — revisa los permisos del canal |
| Aparece "Bot no disponible" en la web | El bot está offline o reiniciándose |

---

← [Moderación](moderacion.md) | [Panel Web →](panel-web.md)
