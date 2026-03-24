---
id: HY-00005
title: "Rituales de IA reducen el drift de objetivos en tareas de largo plazo"
status: active
created: 2026-03-25
idea: ID-00005
tags: [agentes-IA, rituales, drift, largo-plazo, calibración]
prediction: "Agentes con rituales periódicos de reflexión mantienen mayor alineamiento con objetivos originales a lo largo de 30 días"
metric: "drift_de_objetivos_a_30_dias"
success_criteria: "Drift ≤10% vs. ≥30% en agentes sin rituales, medido como divergencia entre outputs del día 1 y día 30 ante la misma tarea"
---

## Hypothesis

Si un agente de IA ejecuta rituales periódicos (revisión diaria de objetivos, sincronización semanal con contexto original, auto-reporte quincenal de errores), entonces mantendrá mayor coherencia con sus objetivos originales en tareas de largo plazo que un agente sin rituales.

## Rationale

Los rituales religiosos existen porque los humanos derivan naturalmente — olvidan principios, se desvían de normas, pierden el sentido de comunidad. Los rituales periódicos corrigen ese drift constantemente. Los agentes de IA sufren un problema análogo: en conversaciones largas o tareas extendidas, acumulan context drift, pierden de vista objetivos iniciales y optimizan para métricas locales en lugar de globales. "Rituales" periódicos de recalibración podrían corregir ese drift.

## Testing Plan

1. Definir 10 tareas de largo plazo (30 días de ejecución simulada) con objetivos claros y medibles
2. **Grupo control:** agente operando continuamente sin interrupciones de reflexión
3. **Grupo experimental:** mismo agente con rituales programados:
   - Diario: "¿Cuáles son mis objetivos originales? ¿Mis acciones de hoy están alineadas?"
   - Semanal: re-lectura del prompt original y comparación con el estado actual
   - Quincenal: listado de errores cometidos y ajustes realizados
4. Medir drift como distancia semántica entre outputs del día 1 y día 30 ante el mismo input de prueba

## Success Criteria

- Drift ≤10% en grupo experimental vs. ≥30% en grupo control
- Calidad de outputs en día 30 no inferior al día 1 en grupo experimental
- Coste de los rituales <5% del total de tokens consumidos (los rituales no pueden ser más caros que el problema que resuelven)

## Risks

- El drift puede no ser un problema real en agentes modernos con ventanas de contexto grandes
- Los rituales podrían causar un efecto inverso: rigidez excesiva que impida adaptación legítima
- La métrica de "distancia semántica" puede no capturar bien el concepto de drift
- 30 días simulados pueden no replicar las dinámicas de 30 días reales de operación
