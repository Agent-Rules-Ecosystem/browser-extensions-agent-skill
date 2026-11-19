# 🔀 Divergencias MV3: Chrome vs Firefox

## Arquitectura Multi-Manifest
No mezclar propiedades exclusivas de cada navegador en un único `manifest.json`. Mantener `manifest.chrome.json` y `manifest.firefox.json` y ensamblar en staging (`dist/chrome/`, `dist/firefox/`).

| Capacidad | Chrome / Edge MV3 | Firefox MV3 |
|---|---|---|
| Background | `background.service_worker` | `background.scripts` (o event page) |
| Panel lateral | `chrome.sidePanel` (`side_panel`) | `sidebar_action` |
| ID y compatibilidad | Clave de Web Store | `browser_specific_settings.gecko` (`id`, `strict_min_version`, `data_collection_permissions`) |

- **Firefox 140+ / Android 142+ (2025+)**: `data_collection_permissions` requiere `strict_min_version >= 142.0` si se soporta Firefox para Android.
