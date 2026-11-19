# 🛡️ Seguridad DOM para AMO y Empaquetado POSIX

## 1. Regla de Oro DOM (Cero `innerHTML` Interpolado)
- Prohibido asignar `innerHTML` con interpolación de variables o plantillas HTML dinámicas (dispara `Unsafe assignment to innerHTML` en `web-ext lint` y retrasa revisiones en `addons.mozilla.org`).
- Usar exclusivamente APIs DOM seguras: `document.createElement()`, `textContent`, `append()` y `replaceChildren()`.

## 2. Empaquetado Multiplataforma (Windows / Unix)
- En Windows, **nunca** usar `Compress-Archive` de PowerShell para paquetes de Firefox AMO porque escribe separadores `\` en las entradas del ZIP (`Invalid file name in archive`).
- Usar streams de .NET `[System.IO.Compression.ZipArchive]` forzando forward-slashes `/` (POSIX) en cada entrada, o `web-ext build` / `zip` en Unix.
