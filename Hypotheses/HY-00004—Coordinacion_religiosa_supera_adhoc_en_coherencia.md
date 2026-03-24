---
id: HY-00004
title: "Coordinación tipo eclesiástica produce mayor coherencia en sistemas multi-agente"
status: active
created: 2026-03-25
idea: ID-00004
tags: [multi-agente, coordinación, coherencia, eclesiástico]
prediction: "Un sistema multi-agente con credo, jerarquía y concilios produce outputs más coherentes que uno con coordinación ad-hoc"
metric: "consistencia_de_outputs"
success_criteria: "≥40% más consistencia en outputs y ≥50% menos conflictos sin resolver, medido en 50 tareas complejas"
---

## Hypothesis

Si un sistema multi-agente implementa coordinación tipo eclesiástica (credo compartido como prompt de sistema, jerarquía de roles orquestador/supervisor/ejecutor, y mecanismo de concilio para resolver conflictos), entonces producirá resultados más coherentes y con menos conflictos sin resolver que un sistema con coordinación ad-hoc.

## Rationale

La Iglesia Católica ha coordinado una organización global de ~1.400 millones de personas durante 2000 años con notable coherencia doctrinal, a pesar de la enorme diversidad cultural. Su modelo — credo inmutable, jerarquía clara, concilios para resolver disputas — es el sistema de coordinación distribuida más longevo de la historia. Si funciona para humanos a esa escala, los principios subyacentes deberían ser transferibles a agentes de IA.

## Testing Plan

1. Diseñar un benchmark de 50 tareas complejas que requieran coordinación entre 5+ agentes
2. **Grupo control:** 5 agentes con coordinación estándar (message passing, sin roles fijos)
3. **Grupo experimental:** 5 agentes con:
   - Credo: prompt compartido con valores y objetivos del colectivo
   - Jerarquía: 1 orquestador, 2 supervisores, 2 ejecutores
   - Concilio: cuando 2+ agentes divergen, proceso formal de debate y votación
4. Evaluar coherencia de outputs (juicio humano + métricas automáticas) y conflictos no resueltos

## Success Criteria

- Consistencia de outputs ≥40% superior (evaluada por 3 jueces humanos con inter-rater reliability ≥0.8)
- Conflictos sin resolver ≥50% menos frecuentes
- Tiempo de resolución de conflictos ≤ tiempo del grupo control (la estructura no debe añadir latencia neta)

## Risks

- La jerarquía puede crear un cuello de botella en el orquestador (punto único de fallo, como un papa incompetente)
- El credo puede ser demasiado rígido y limitar la creatividad de los agentes
- El mecanismo de concilio puede ser lento para tareas que requieren decisiones rápidas
- Comparación injusta si el grupo control no tiene ninguna estructura vs. una estructura muy elaborada
