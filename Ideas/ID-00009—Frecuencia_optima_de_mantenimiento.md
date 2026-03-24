---
id: ID-00009
title: "Frecuencia óptima de rituales de mantenimiento en sistemas sociales y técnicos"
status: active
created: 2026-03-25
sources:
  - SR-00003
  - SR-00002
phase: contemplate
domain: "optimización de sistemas"
tags: [frecuencia, mantenimiento, rituales, optimización, cron]
scores:
  feasibility: 85
  novelty: 65
  impact: 75
  elegance: 80
---

## Description

Las religiones han calibrado empíricamente la frecuencia de sus rituales durante siglos — ¿hay principios universales detrás de esa calibración que apliquen a sistemas técnicos?

**Observaciones:**
- Diario (5x): rezo islámico, meditación budista → mantenimiento de estado individual
- Semanal (1x): misa, shabbat → sincronización grupal
- Mensual/estacional: ayunos, festividades → reset profundo y renovación
- Anual: peregrinación, festividades mayores → realineamiento con el propósito global
- Vital (1x en la vida): bautismo, bar mitzvah → inicialización del nodo

**Hipótesis implícita:** la frecuencia óptima depende del scope del proceso:
- Scope individual → alta frecuencia, bajo coste
- Scope grupal → frecuencia media
- Scope sistémico → baja frecuencia, alto coste

Esto mapea directamente a: health checks (segundos), stand-ups (diarios), sprints (semanales), retrospectivas (quincenales), planificación estratégica (trimestral).

## Provenance

Fase CONTEMPLATE: análisis de las frecuencias rituales como un problema de optimización — demasiado frecuente desperdicia recursos, demasiado infrecuente pierde coherencia.

## Connection

Extiende SR-00003 preguntando no solo si los rituales son daemons, sino si la frecuencia milenariamente calibrada contiene información útil para el diseño de sistemas modernos.

## Next Steps

Hipótesis: "Equipos de desarrollo que ajustan la frecuencia de sus ceremonias (stand-ups, retros, planificación) al patrón diario-individual/semanal-grupal/trimestral-sistémico reportan mayor satisfacción y menor overhead que los que usan frecuencias arbitrarias."
