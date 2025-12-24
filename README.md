# Trae AI Rules (Web Stack Guardrails)

Repositorio de reglas/guardrails para usar en Trae IDE y mantener consistencia en arquitectura, seguridad, performance, SEO y UX/UI en proyectos con React, Astro, Next.js y NestJS.

## Objetivo
- Reducir errores comunes al programar con agentes de IA (cambios destructivos, duplicación, suposiciones).
- Asegurar buenas prácticas en frontend (TS/TSX), backend (NestJS) y diseño (UX/UI).
- Mantener un estándar único para equipos y repos.

## Qué contiene
- Reglas generales (calidad, refactor seguro, no-borrado, anti-duplicación).
- Reglas por framework:
  - React (TSX + hooks).
  - Astro (islands + directivas `client:*`).
  - Next.js (App Router + metadata/SEO + caching).
  - NestJS (arquitectura modular + seguridad + versionado + CORS + JWT).
- Reglas de UX/UI para evitar interfaces genéricas.
- Checklists rápidas (pre-commit / pre-PR).

## Estructura del repo
- `rules/00-general.md`
- `rules/02-frontend-astro.md`
- `rules/03-frontend-nextjs.md`
- `rules/04-backend-nestjs.md`
- `rules/05-ux-ui.md`
- `rules/99-checklists.md`

## Cómo usar en Trae
1. Copia el contenido del archivo de reglas que necesites (por ejemplo `rules/03-frontend-nextjs.md`).
2. Pégalo en tu configuración de “Rules” del agente en Trae.
3. Mantén solo lo necesario para tu proyecto (muchos agentes tienen límite de caracteres).

> Recomendación: usa `rules/00-general.md` como base y agrega solo 1–2 archivos por proyecto (ej. Next.js + NestJS).

## Convenciones para escribir reglas
- Cada regla debe ser accionable y verificable (evita “hazlo bonito”).
- Prefiere “DO / DON’T” o frases imperativas.
- Si una regla tiene excepción, documenta la excepción explícitamente.
- Si una regla implica riesgo (seguridad/SEO), requiere confirmación antes de aplicar cambios grandes.

## Aportar / mantener
- Si agregas una regla, incluye:
  - Motivación (qué bug evita).
  - Ejemplo corto (opcional).
  - Alcance (global / framework / módulo).
- Evita reglas duplicadas: referencia la regla general cuando aplique.

## Roadmap (opcional)
- Plantillas listas para copiar/pegar según tipo de proyecto (landing, dashboard, app con auth, etc.).
- “Rules compactas” (<1000 chars) por stack para agentes con límite estricto.


