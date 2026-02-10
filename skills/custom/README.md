# Custom Skills

Esta carpeta contiene skills personales que no forman parte del repositorio upstream.

## Convenciones

- **Naming**: Usa nombres descriptivos en lowercase con guiones: `my-workflow-name`
- **Formato**: Todas las skills deben tener un archivo `SKILL.md` con frontmatter YAML
- **Organización**: Puedes crear subcarpetas por dominio si lo prefieres (ej: `frontend/`, `backend/`)

## Ejemplo de SKILL.md

```markdown
---
name: my-custom-skill
description: "Descripción breve de tu skill personalizada"
author: sealca
version: "1.0"
metadata:
  tags: custom, personal, workflow
---

# Mi Skill Personalizada

## Cuándo usar

Describe cuándo usar esta skill...

## Cómo funciona

Explica el funcionamiento...
```

## Actualización

Las skills en esta carpeta se mantienen en tu fork personal y no se ven afectadas por las actualizaciones automáticas del upstream.
