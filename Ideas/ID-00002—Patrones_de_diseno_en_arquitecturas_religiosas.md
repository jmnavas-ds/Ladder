---
id: ID-00002
title: "Patrones de diseño extraídos de arquitecturas religiosas"
status: active
created: 2026-03-25
sources:
  - SR-00002
phase: steal
domain: "arquitectura de sistemas"
tags: [patrones, resiliencia, religión, software-design]
scores:
  feasibility: 80
  novelty: 85
  impact: 75
  elegance: 90
---

## Description

Mapear las religiones principales como si fueran arquitecturas de software y extraer patrones de diseño reutilizables. Por ejemplo:

- **Patrón Decálogo** (API pública mínima): Reducir las reglas de interacción a un set mínimo y memorable. Los 10 mandamientos, las 5 Pilares del Islam, el Noble Óctuple Sendero — todos limitan la superficie de la API para maximizar adopción.
- **Patrón Confesionario** (garbage collection): Mecanismo periódico para liberar culpa acumulada y restaurar estado limpio del individuo.
- **Patrón Profeta** (single source of truth): Un nodo autoritativo que resuelve ambigüedades en la interpretación del sistema.
- **Patrón Liturgia** (protocolo de consenso): Secuencia fija de acciones que garantiza que todos los nodos estén sincronizados.

## Provenance

Fase STEAL: tomar la ingeniería de software y aplicarla como lente analítica sobre sistemas religiosos, luego invertir la dirección — traer los patrones descubiertos de vuelta al diseño de software y sistemas sociales.

## Connection

Aborda el problema de SR-00002: ¿cómo se diseñan sistemas de coordinación social que escalen sin autoridad central? Las religiones lo han resuelto durante milenios — sus soluciones son patrones probados en producción a escala civilizatoria.

## Next Steps

Hipótesis: "Los sistemas de coordinación multi-agente que implementan al menos 3 patrones religiosos (API mínima, garbage collection periódico, protocolo de consenso) muestran mayor resiliencia que los que no los implementan."
