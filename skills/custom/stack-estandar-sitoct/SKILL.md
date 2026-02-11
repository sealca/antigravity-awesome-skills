---
name: stack-estandar-sitoct
description: Stack tecnológico estándar para todos los proyectos. Define las tecnologías, plataformas de deployment y arquitectura recomendada basada en las mejores prácticas de 2026. Usar siempre que se inicie un nuevo proyecto o se necesite asesoramiento sobre tecnologías.
---

# Stack Tecnológico Estándar 2026

> **Filosofía**: Usar siempre el mismo stack estándar para todos los proyectos. Esto garantiza consistencia, facilita el mantenimiento y aprovecha las mejores prácticas del mercado.

---

## 🎯 Stack Estándar (Usar SIEMPRE)

### Frontend
**Plataforma: VERCEL** ⭐

**Stack Técnico:**
- **Framework**: Next.js (App Router)
- **Lenguaje**: TypeScript
- **Styling**: Tailwind CSS + shadcn/ui
- **State Management**: TanStack Query (React Query)
- **Routing**: Next.js App Router

**Por qué:**
- ✅ Líder del mercado (usado por Uber, Netflix, TikTok)
- ✅ Deploy automático desde GitHub (git push)
- ✅ CDN global (app 10x más rápida)
- ✅ SSL automático
- ✅ Preview deployments (cada PR tiene su URL)
- ✅ Tier gratuito muy generoso
- ✅ Mejor Developer Experience del mercado

---

### Backend (APIs Custom)
**Plataforma: GOOGLE CLOUD RUN** ⭐

**Stack Técnico:**
- **Lenguaje**: .NET 8+ / Node.js (según proyecto)
- **Contenedores**: Docker
- **Escalado**: Automático (0 a infinito)

**Por qué:**
- ✅ Estándar enterprise para contenedores serverless
- ✅ Soporta CUALQUIER lenguaje (incluido .NET)
- ✅ Escalado automático probado en producción
- ✅ Solo pagas por uso real (cuando recibe peticiones)
- ✅ Tier gratuito: 2M peticiones/mes
- ✅ Integración perfecta con Google Cloud

**Cuándo usar:**
- Proyectos con backend .NET existente
- APIs con lógica de negocio compleja
- Cuando necesitas control total del backend

---

### Base de Datos
**Plataforma: SUPABASE** ⭐

**Stack Técnico:**
- **Base de datos**: PostgreSQL (gestionado)
- **Auth**: Supabase Auth (incluido)
- **Storage**: Supabase Storage (incluido)
- **Realtime**: Suscripciones a cambios (incluido)

**Por qué:**
- ✅ PostgreSQL (el estándar open-source más usado)
- ✅ Crecimiento explosivo (alternativa open-source a Firebase)
- ✅ Tier gratuito muy generoso (500MB-5GB)
- ✅ Auth + Storage + Realtime incluidos
- ✅ API REST automática generada desde schema
- ✅ Row Level Security (RLS) integrado

**Cuándo usar:**
- Todos los proyectos nuevos
- Cuando necesitas base de datos + auth + storage
- Proyectos pequeños a medianos

---

### Archivos/Storage (Opcional)
**Plataforma: CLOUDFLARE R2** ⭐

**Stack Técnico:**
- **Object Storage**: Compatible con S3
- **CDN**: Global incluido

**Por qué:**
- ✅ Compatible con S3 (estándar de facto)
- ✅ SIN costos de egress (S3 cobra por descargas)
- ✅ CDN global incluido
- ✅ Más barato que S3

**Cuándo usar:**
- Archivos grandes (videos, imágenes de alta resolución)
- Muchos archivos (miles/millones)
- Si Supabase Storage no es suficiente

---

### CI/CD
**Plataforma: GITHUB ACTIONS** ⭐

**Por qué:**
- ✅ Integrado en GitHub (donde ya está el código)
- ✅ Usado por el 80%+ de proyectos open-source
- ✅ Gratis para repos públicos
- ✅ 2000 minutos/mes gratis para privados
- ✅ Marketplace gigante de actions

---

### Monitoreo
**Plataformas:**
- **Errores**: Sentry (estándar de facto)
- **Analytics**: Vercel Analytics (gratis e integrado)

---

## 🏗️ Arquitectura Estándar

### Para Proyectos Nuevos (Desde Cero)

```
┌─────────────────────────────────────┐
│  Frontend (Next.js)                 │
│  Hosting: VERCEL                    │
│  - Deploy automático desde GitHub   │
│  - CDN global                       │
│  - SSL automático                   │
└─────────────────────────────────────┘
              ↓ HTTPS
┌─────────────────────────────────────┐
│  Base de datos + Auth + Storage     │
│  Hosting: SUPABASE                  │
│  - PostgreSQL gestionado            │
│  - Auth incluido                    │
│  - API REST automática              │
└─────────────────────────────────────┘
```

**Tiempo de setup**: 30 minutos
**Costo**: 0€ (tier gratuito)

---

### Para Proyectos con Backend .NET Existente

```
┌─────────────────────────────────────┐
│  Frontend (React/Next.js)           │
│  Hosting: VERCEL                    │
└─────────────────────────────────────┘
              ↓ HTTPS
┌─────────────────────────────────────┐
│  Backend (.NET API)                 │
│  Hosting: GOOGLE CLOUD RUN          │
│  - Contenedor Docker                │
│  - Escala automáticamente           │
└─────────────────────────────────────┘
              ↓
┌─────────────────────────────────────┐
│  Base de datos (PostgreSQL)         │
│  Hosting: SUPABASE                  │
└─────────────────────────────────────┘
```

**Tiempo de setup**: 4-6 horas
**Costo**: 0-10€/mes (pequeñas apps)

---

## 📊 VPS Tradicional vs Cloud Moderno

### ❌ VPS Tradicional (NO usar para proyectos nuevos)

**Contras:**
- ⚠️ Tiempo de mantenimiento (4-6h/mes)
- ⚠️ Sin escalado automático
- ⚠️ Sin CDN (usuarios lentos)
- ⚠️ Costo fijo aunque no se use
- ⚠️ Deploy manual (SSH, build, restart)
- ⚠️ Tú gestionas seguridad, backups, SSL

**Cuándo usar:**
- Proyectos legacy ya en producción
- Requisitos muy específicos que no se pueden cumplir en cloud

---

### ✅ Cloud Moderno (Usar SIEMPRE para proyectos nuevos)

**Pros:**
- ✅ Cero mantenimiento
- ✅ Escalado automático
- ✅ CDN global (app 5-10x más rápida)
- ✅ Pagas solo por uso real
- ✅ Deploy automático (git push)
- ✅ Seguridad, backups, SSL automáticos
- ✅ Tier gratuito muy generoso

**Comparativa de costos (clínica pequeña, 50 pacientes/día):**

| Concepto | VPS | Cloud Moderno |
|---|---|---|
| Hosting | 20€/mes | 0€ (tier gratuito) |
| SSL | Gratis (manual) | Gratis (automático) |
| CDN | No incluido | Gratis (incluido) |
| Backups | Manual | Automático gratis |
| **Total** | **20€/mes** | **0-5€/mes** |
| **Tiempo mantenimiento** | **4-6h/mes** | **0h/mes** |

---

## 🚀 Workflow de Deployment

### Frontend (Vercel)
```bash
# 1. Conectar repo a Vercel (una sola vez)
# 2. Cada push a main = deploy automático
git push origin main

# Listo! Deploy en 30 segundos
```

### Backend (Cloud Run)
```bash
# 1. Crear Dockerfile (una sola vez)
# 2. Configurar GitHub Actions (una sola vez)
# 3. Cada push a main = build + deploy automático
git push origin main

# Listo! Deploy en 2-3 minutos
```

---

## 🎯 Reglas de Decisión

### ¿Cuándo usar qué?

**Proyecto nuevo sin backend complejo:**
→ Next.js + Supabase (todo en uno)

**Proyecto nuevo con backend .NET:**
→ Next.js (Vercel) + .NET (Cloud Run) + Supabase

**Proyecto legacy en VPS:**
→ Migrar frontend primero a Vercel (beneficio inmediato)
→ Migrar backend después cuando tengas tiempo

**Archivos grandes/muchos:**
→ Cloudflare R2 (en vez de Supabase Storage)

---

## 📝 Checklist para Nuevos Proyectos

### Fase 1: Setup Inicial (30 min)
- [ ] Crear repo en GitHub
- [ ] `npx create-next-app@latest` (Next.js)
- [ ] Conectar a Vercel (deploy automático)
- [ ] Crear proyecto en Supabase
- [ ] Configurar variables de entorno

### Fase 2: Desarrollo (variable)
- [ ] Implementar features
- [ ] Configurar Supabase Auth
- [ ] Crear schema de base de datos
- [ ] Deploy automático en cada push

### Fase 3: Producción (1 hora)
- [ ] Configurar dominio custom
- [ ] Configurar variables de producción
- [ ] Configurar Sentry (monitoreo de errores)
- [ ] Verificar SSL y CDN

---

## 🔗 Referencias Rápidas

### Documentación Oficial
- [Vercel Docs](https://vercel.com/docs)
- [Cloud Run Docs](https://cloud.google.com/run/docs)
- [Supabase Docs](https://supabase.com/docs)
- [Next.js Docs](https://nextjs.org/docs)

### Templates de Inicio Rápido
- Next.js + Supabase: `npx create-next-app@latest --example with-supabase`
- Next.js + Tailwind: `npx create-next-app@latest`

---

## ⚠️ Excepciones al Stack Estándar

**SOLO desviarse del stack estándar si:**
1. Cliente requiere tecnología específica (contractual)
2. Proyecto legacy con stack establecido
3. Requisitos técnicos muy específicos que no se pueden cumplir

**En todos los demás casos: USAR EL STACK ESTÁNDAR**

---

## 💡 Principios Clave

1. **Consistencia**: Mismo stack = menos curva de aprendizaje
2. **Mantenibilidad**: Stack moderno = menos tiempo de mantenimiento
3. **Escalabilidad**: Cloud = escalado automático sin esfuerzo
4. **Economía**: Tier gratuito + pago por uso = más barato que VPS
5. **Velocidad**: CDN global = usuarios felices

---

**Última actualización**: Febrero 2026
**Versión**: 1.0
