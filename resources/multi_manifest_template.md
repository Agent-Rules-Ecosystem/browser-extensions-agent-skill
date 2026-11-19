# 📄 Plantillas Multi-Manifest MV3

## `manifest.chrome.json`
```json
{
  "manifest_version": 3,
  "name": "Extension Name",
  "version": "1.0.0",
  "background": { "service_worker": "background.js", "type": "module" },
  "side_panel": { "default_path": "sidepanel.html" }
}
```

## `manifest.firefox.json`
```json
{
  "manifest_version": 3,
  "name": "Extension Name",
  "version": "1.0.0",
  "browser_specific_settings": {
    "gecko": {
      "id": "ext@example.org",
      "strict_min_version": "142.0",
      "data_collection_permissions": { "required": ["none"] }
    }
  },
  "sidebar_action": { "default_panel": "sidepanel.html" }
}
```
