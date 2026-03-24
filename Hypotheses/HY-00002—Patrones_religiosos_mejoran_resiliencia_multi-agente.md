---
id: HY-00002
title: "Patrones religiosos mejoran la resiliencia de sistemas multi-agente"
status: active
created: 2026-03-25
idea: ID-00002
tags: [resiliencia, patrones, multi-agente, coordinación]
prediction: "Sistemas multi-agente que implementan patrones religiosos (API mínima, garbage collection periódico, protocolo de consenso) muestran mayor resiliencia que los que no"
metric: "tasa_recuperacion_ante_fallos"
success_criteria: "Recuperación ante fallos ≥30% más rápida y ≥25% menos fallos en cascada vs. grupo de control, medido en 100 simulaciones"
---

## Hypothesis

Si un sistema de coordinación multi-agente implementa al menos 3 patrones extraídos de arquitecturas religiosas (API mínima tipo Decálogo, garbage collection tipo Confesionario, protocolo de consenso tipo Liturgia), entonces mostrará mayor resiliencia ante fallos que un sistema con coordinación convencional.

## Rationale

Las religiones han coordinado millones de agentes autónomos durante milenios sin servidor central y sin downtime total. Sus mecanismos de coordinación han sido seleccionados evolutivamente — los que no funcionaban desaparecieron junto con las religiones que los usaban. Si estos patrones sobrevivieron miles de años de "producción", contienen información sobre resiliencia que los sistemas modernos podrían aprovechar.

## Testing Plan

1. Implementar un sistema multi-agente de referencia con coordinación estándar (message passing, leader election)
2. Implementar una variante que incorpore 3 patrones religiosos:
   - API mínima: cada agente expone máximo 10 operaciones
   - Garbage collection: proceso periódico donde agentes reportan y limpian estado inconsistente
   - Protocolo de consenso: secuencia fija de pasos para decisiones colectivas
3. Ejecutar 100 simulaciones introduciendo fallos aleatorios (agentes caídos, mensajes perdidos, particiones de red)
4. Medir tiempo de recuperación, fallos en cascada y consistencia del estado final

## Success Criteria

- Tiempo de recuperación ante fallos ≥30% menor
- Fallos en cascada ≥25% menos frecuentes
- Consistencia del estado final ≥95% en ambos casos (no sacrificar correctitud por resiliencia)

## Risks

- La analogía puede ser superficial — que los patrones funcionen para humanos no garantiza que funcionen para agentes de software
- Los patrones religiosos evolucionaron en contextos de baja velocidad de comunicación; agentes de IA operan a velocidades radicalmente distintas
- Riesgo de cherry-picking: seleccionar solo los patrones que confirman la hipótesis e ignorar los que no aplican
