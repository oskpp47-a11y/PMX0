# 📋 Pensionados MX v23

App web progresiva (PWA) para gestión de beneficiarios de programas sociales. Funciona **100% sin internet** después de la primera carga, y se puede instalar en cualquier dispositivo como app nativa.

---

## 📱 Compatibilidad

| Dispositivo | Estado |
|-------------|--------|
| iPhone / Safari iOS 15+ | ✅ Completo |
| iPhone / Safari iOS 14 | ✅ Con fallback |
| Android / Chrome | ✅ Completo |
| Android / Firefox | ✅ Completo |
| iPad | ✅ Completo |
| Desktop (Chrome, Edge, Firefox, Safari) | ✅ Completo |

---

## 🗂️ Archivos del proyecto

```
/
├── index.html      → App completa (HTML + CSS + JS en un solo archivo)
├── sw.js           → Service Worker para modo offline
├── manifest.json   → Configuración PWA (nombre, iconos, colores)
├── icon-192.png    → Ícono 192×192 px
├── icon-512.png    → Ícono 512×512 px
└── .gitignore
```

---

## 🚀 Cómo publicar en GitHub Pages

1. Sube estos archivos a un repositorio en GitHub
2. Ve a **Settings → Pages**
3. En **Source**, selecciona `main` y carpeta `/ (root)`
4. Guarda — en unos segundos tendrás una URL del tipo:
   `https://tuusuario.github.io/pensionados-mx/`
5. Abre esa URL en tu iPhone y toca **"Agregar a pantalla de inicio"**

---

## 🔧 Correcciones y mejoras en v23

### 🐛 Bugs corregidos
- **Tab "Importar" rota** — la pantalla ya funciona correctamente al abrirla
- **Secciones/Rutas invisibles en Inicio** — el bloque de secciones ahora aparece correctamente
- **Botón ocultar secciones sin efecto** — ya colapsa y expande correctamente
- **Duplicados en Inicio sin respuesta** — el card de duplicados ya abre el filtro correcto
- **Migración de datos corregida** — recupera datos de versiones anteriores (v9, v8…)
- **Sheet de filtro rápido sin botón cerrar** — ahora tiene botón ✕ visible
- **Pantalla Estadísticas sin estilos** — números y tarjetas ya se ven correctamente
- **Búsqueda por voz sin estilos** — el cuadro de escucha ya es visible

### ✨ Mejoras
- Pantalla **Importar** con estadísticas en tiempo real y guía de formato CSV
- Estado vacío en **Inicio** con botones directos "Agregar" e "Importar CSV"
- **Marcar visitados** ahora registra en historial y actualiza el inicio
- Diseño responsive mejorado para pantallas ≤ 360 px

---

## 🔄 Cómo actualizar la app

Cuando hagas cambios al código:
1. Cambia `CACHE_NAME` en `sw.js` a la siguiente versión (ej. `pensionados-v24`)
2. Actualiza el `<title>` en `index.html`
3. Sube los archivos al repositorio
4. La próxima vez que el usuario abra la app, verá la barra azul de actualización

---

## 💾 Almacenamiento de datos

Los datos se guardan **localmente en el dispositivo** usando localStorage / IndexedDB. No se envía nada a ningún servidor. Para hacer respaldo manual, usa el botón **"Exportar JSON"** dentro de la app (pestaña Exportar).

---

## 📲 Instalar en iPhone

1. Abre Safari y ve a la URL de GitHub Pages
2. Toca el botón de compartir (cuadro con flecha)
3. Selecciona **"Agregar a pantalla de inicio"**
4. La app queda instalada como ícono nativo

> **Importante:** En iPhone, la app debe instalarse desde **Safari** (no Chrome ni otro navegador) para funcionar correctamente como PWA.
