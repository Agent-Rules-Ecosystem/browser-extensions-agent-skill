---
name: browser-extensions-agent-skill
description: Cross-browser WebExtensions MV3 skill for Chrome, Firefox (AMO), and Edge with dual-manifest staging, POSIX ZIP packaging, and DOM security.
---

# Browser Extensions Agent Skill

1. `.skill/browser-extensions-agent-skill/SKILL.md` ← Matriz de capacidades y auditoría `$ext:audit`
2. `.skill/browser-extensions-agent-skill/core/brain.md` ← Decisiones Chrome vs Firefox MV3
3. `.skill/browser-extensions-agent-skill/core/commands.md` ← Comandos `$ext`
4. `.skill/browser-extensions-agent-skill/core/path_map.md` ← Rutas de manifiestos y staging

## Reglas Inviolables
1. Nunca mezclar claves exclusivas de Chrome (`sidePanel`, `service_worker`) y Firefox (`gecko`, `sidebar_action`) en un único `manifest.json` sin staging.
2. Nunca usar `Compress-Archive` de PowerShell en Windows para paquetes AMO (genera `\`); usar siempre forward-slashes `/` (POSIX).
3. Prohibido `innerHTML` con interpolación de variables en código de extensión.
4. No modificar `.skill/` ni `.agents/` desde proyectos cliente; registrar propuestas en `overview/learning.md`.
