# Mx Template

This folder contains the standard 4-page structure used by M1 and M2.

## Files

- `mx.qmd`
- `mx-component-description.qmd`
- `mx-standalone-module.qmd`
- `mx-platform-module.qmd`

## How to create a new module (example: M3)

1. Copy this folder to `catalog/m3`.
2. Rename files:
   - `mx.qmd` -> `m3.qmd`
   - `mx-component-description.qmd` -> `m3-component-description.qmd`
   - `mx-standalone-module.qmd` -> `m3-standalone-module.qmd`
   - `mx-platform-module.qmd` -> `m3-platform-module.qmd`
3. Replace all `MX` and `Module Name` placeholders in frontmatter and content.
4. Add a Catalog sidebar section in `_quarto.yml`:

```yaml
- section: M3 - Your Module Name
  contents: catalog/m3/*.qmd
```

5. Add links in `catalog/overview.qmd` if you want the Catalog page to list M3 entries.
6. Render:

```powershell
quarto render
```

## PowerShell helper (optional)

```powershell
Copy-Item -Recurse catalog/_templates/mx catalog/m3
Rename-Item catalog/m3/mx.qmd m3.qmd
Rename-Item catalog/m3/mx-component-description.qmd m3-component-description.qmd
Rename-Item catalog/m3/mx-standalone-module.qmd m3-standalone-module.qmd
Rename-Item catalog/m3/mx-platform-module.qmd m3-platform-module.qmd
```
