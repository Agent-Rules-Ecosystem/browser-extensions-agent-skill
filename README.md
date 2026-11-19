# 🌐 Browser Extensions Agent Skill

> **WebExtensions Multi-Browser (Chrome, Firefox, Edge)** — Arquitectura MV3 dual-manifest, empaquetado ZIP POSIX multiplataforma y seguridad DOM para Chrome Web Store y Mozilla AMO.

## 📌 Propósito y Alcance
1. 🧩 **Arquitectura Multi-Manifest MV3**: Separación limpia de `manifest.chrome.json` (`service_worker`, `sidePanel`) y `manifest.firefox.json` (`browser_specific_settings.gecko`, `sidebar_action`, `data_collection_permissions`).
2. 📦 **Empaquetado ZIP POSIX**: Generación de paquetes `.zip`/`.xpi` con forward-slashes `/` compatibles con AMO desde Windows/Linux/macOS.
3. 🛡️ **Seguridad DOM para AMO (`web-ext lint`)**: Cero `innerHTML` con interpolación; construcción segura vía `createElement`, `textContent`, `append()` y `replaceChildren()`.

## 📦 Instalación como Submódulo
```bash
git submodule add git@github.com:Agent-Rules-Ecosystem/browser-extensions-agent-skill.git .skill/browser-extensions-agent-skill
```
