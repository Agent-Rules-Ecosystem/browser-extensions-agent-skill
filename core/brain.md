# 🧠 Motor de Decisiones — Browser Extensions

| Situación | Decisión |
|---|---|
| Extensión apunta a Chrome + Firefox | Usar skill unificada (~85% API WebExtensions compartida) con `manifest.chrome.json` y `manifest.firefox.json`. |
| Empaquetado en Windows para AMO | Prohibir `Compress-Archive`; usar stream .NET `[System.IO.Compression.ZipArchive]` con `/` POSIX. |
| Firefox + soporte Android + `data_collection_permissions` | Exigir `strict_min_version >= 142.0` en `browser_specific_settings.gecko`. |
| Renderizado dinámico en popup/sidepanel/content script | Prohibir `innerHTML` interpolado; usar `createElement`, `textContent`, `append()`, `replaceChildren()`. |
