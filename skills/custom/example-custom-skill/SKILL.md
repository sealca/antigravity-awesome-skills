---
name: example-custom-skill
description: "Skill de ejemplo para demostrar cómo crear skills personales en la carpeta custom/"
author: sealca
version: "1.0"
metadata:
  tags: example, custom, demo, tutorial
---

# Example Custom Skill

Esta es una skill de ejemplo que demuestra cómo crear y estructurar tus propias skills personales en la carpeta `custom/`.

## Cuándo usar esta skill

- Cuando necesites un template para crear tus propias skills
- Cuando quieras entender el formato correcto de SKILL.md
- Como referencia para la estructura y secciones recomendadas

## Estructura de una Skill

### Frontmatter YAML (Obligatorio)

Todas las skills deben comenzar con frontmatter YAML que incluya:
- `name`: Nombre único de la skill (debe coincidir con el nombre de la carpeta)
- `description`: Descripción breve de una línea
- `author`: Tu nombre de usuario (opcional pero recomendado)
- `version`: Versión de la skill (opcional)
- `metadata.tags`: Tags para búsqueda y categorización (opcional)

### Secciones Recomendadas

1. **Título principal** (`# Nombre`)
2. **Cuándo usar** - Escenarios de uso
3. **Cómo funciona** - Explicación paso a paso
4. **Ejemplos** - Código o casos de uso concretos
5. **Mejores prácticas** - Recomendaciones y anti-patrones
6. **Recursos adicionales** - Links útiles (opcional)

## Cómo crear tu propia skill

### Paso 1: Crear la carpeta

```bash
cd c:\Users\sitoc\Documents\Antigravity\.agent\skills\skills\custom
mkdir mi-skill-personalizada
cd mi-skill-personalizada
```

### Paso 2: Crear SKILL.md

Copia este template y personalízalo:

```markdown
---
name: mi-skill-personalizada
description: "Descripción breve de tu skill"
author: sealca
version: "1.0"
metadata:
  tags: tu, tags, aqui
---

# Mi Skill Personalizada

## Cuándo usar

- Usa cuando [escenario 1]
- Usa cuando [escenario 2]

## Cómo funciona

Explicación detallada...

## Ejemplos

\`\`\`javascript
// Tu código de ejemplo
\`\`\`

## Mejores prácticas

- ✅ Hacer esto
- ❌ Evitar esto
```

### Paso 3: Validar (opcional)

```bash
cd c:\Users\sitoc\Documents\Antigravity\.agent\skills
python scripts\validate_skills.py
```

### Paso 4: Commitear

```bash
git add skills\custom\mi-skill-personalizada
git commit -m "feat: add custom skill mi-skill-personalizada"
git push origin main
```

### Paso 5: Usar en Antigravity

```
@mi-skill-personalizada ayúdame con [tu tarea]
```

## Ejemplos de Skills Personales

### Skill de Workflow Personal

```markdown
---
name: my-dev-workflow
description: "Mi workflow personal de desarrollo para proyectos React"
---

# My Dev Workflow

## Setup inicial

1. Crear proyecto con Vite
2. Instalar dependencias base
3. Configurar ESLint y Prettier
4. Setup de testing con Vitest

## Estructura de carpetas

\`\`\`
src/
├── components/
├── hooks/
├── utils/
└── pages/
\`\`\`
```

### Skill de Convenciones de Código

```markdown
---
name: my-code-conventions
description: "Mis convenciones de código y naming"
---

# My Code Conventions

## Naming

- Componentes: PascalCase
- Hooks: useCamelCase
- Utils: camelCase
- Constantes: UPPER_SNAKE_CASE

## Estructura de componentes

\`\`\`tsx
export function MyComponent({ prop1, prop2 }: Props) {
  // 1. Hooks
  const [state, setState] = useState()
  
  // 2. Efectos
  useEffect(() => {}, [])
  
  // 3. Handlers
  const handleClick = () => {}
  
  // 4. Render
  return <div>...</div>
}
\`\`\`
```

## Mejores Prácticas para Skills Personales

### ✅ Hacer

- **Ser específico**: Enfócate en un problema o workflow concreto
- **Incluir ejemplos**: El código habla más que las palabras
- **Documentar contexto**: Explica el "por qué", no solo el "cómo"
- **Mantener actualizado**: Revisa y actualiza tus skills regularmente
- **Usar tags relevantes**: Facilita encontrar la skill después

### ❌ Evitar

- **Skills demasiado genéricas**: Si ya existe en el upstream, úsala
- **Duplicar skills oficiales**: Mejor contribuir al upstream
- **Falta de ejemplos**: Sin ejemplos es difícil de usar
- **Información desactualizada**: Mantén las versiones y dependencias al día

## Organización Avanzada

Puedes crear subcarpetas dentro de `custom/` para organizar por dominio:

```
custom/
├── frontend/
│   ├── react-patterns/
│   └── css-utilities/
├── backend/
│   ├── api-design/
│   └── database-patterns/
└── devops/
    └── deployment-workflows/
```

## Recursos Adicionales

- [Guía oficial de contribución](file:///c:/Users/sitoc/Documents/Antigravity/.agent/skills/CONTRIBUTING.md)
- [Skills index completo](file:///c:/Users/sitoc/Documents/Antigravity/.agent/skills/skills_index.json)
- [Ejemplos de skills oficiales](file:///c:/Users/sitoc/Documents/Antigravity/.agent/skills/skills/)

---

**¡Ahora crea tu primera skill personalizada!** 🚀
