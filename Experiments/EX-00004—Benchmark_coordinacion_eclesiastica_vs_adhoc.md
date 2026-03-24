---
id: EX-00004
title: "Benchmark de coordinación eclesiástica vs ad-hoc en agentes LLM"
status: draft
created: 2026-03-25
hypothesis: HY-00004
algorithm: ""
tags: [benchmark, multi-agente, coordinación, eclesiástico, LLM]
methodology: "Benchmark comparativo con evaluación humana y automática"
duration: "2 semanas"
success_criteria: "≥40% más consistencia y ≥50% menos conflictos sin resolver"
---

## Objective

Comparar la calidad de outputs y la resolución de conflictos entre un sistema multi-agente con coordinación ad-hoc y uno con coordinación inspirada en la estructura eclesiástica (credo, jerarquía, concilios).

## Methodology

1. **Diseñar benchmark (3 días):**
   - 50 tareas que requieran coordinación entre 5 agentes:
     - 15 tareas de análisis (múltiples perspectivas sobre un problema)
     - 15 tareas de creación (diseño colaborativo de soluciones)
     - 10 tareas con conflicto deliberado (requisitos contradictorios)
     - 10 tareas de planificación (secuenciación de acciones)

2. **Implementar grupo control (2 días):**
   - 5 agentes Claude con roles genéricos
   - Comunicación libre entre todos
   - Sin jerarquía ni protocolo de resolución de conflictos
   - Prompt: "Colaborad para resolver esta tarea"

3. **Implementar grupo experimental (3 días):**
   - **Credo:** Prompt compartido con 5 principios innegociables del colectivo
   - **Jerarquía:**
     - 1 Orquestador (descompone tarea, asigna subtareas, sintetiza resultado)
     - 2 Supervisores (revisan calidad, detectan inconsistencias)
     - 2 Ejecutores (producen el trabajo concreto)
   - **Concilio:** Cuando ≥2 agentes divergen:
     1. Cada parte expone su posición con evidencia
     2. Supervisores evalúan ambas posiciones
     3. Orquestador toma decisión final documentando el razonamiento
     4. Decisión se registra como precedente

4. **Ejecutar y evaluar (4 días):**
   - Ejecutar las 50 tareas con ambos sistemas (100 ejecuciones total)
   - 3 evaluadores humanos puntúan consistencia (1-5) y completitud (1-5)
   - Script automático cuenta conflictos sin resolver y tiempo total

## Setup

- **LLM:** Claude Sonnet para los 5 agentes (consistencia entre ejecuciones)
- **Framework:** Script TypeScript/Bun de orquestación
- **Evaluación humana:** 3 evaluadores con rúbrica estandarizada
- **Tareas:** Extraídas de problemas reales (code review, diseño de APIs, análisis de requisitos)

## Algorithm

No aplica aún — si el modelo eclesiástico funciona, se documenta como Algorithm de coordinación multi-agente.

## Success Criteria

- Consistencia de outputs ≥40% superior (media de evaluación humana)
- Inter-rater reliability ≥0.8 (Krippendorff's alpha)
- Conflictos sin resolver ≥50% menos frecuentes
- Latencia total ≤120% de la del grupo control (toleramos hasta 20% más de tiempo)
- Tokens totales ≤150% del grupo control (el overhead de coordinación no puede ser excesivo)

## Data Collection

| Métrica | Método | Frecuencia |
|---------|--------|------------|
| Consistencia | Evaluación humana 1-5 | Por tarea |
| Completitud | Evaluación humana 1-5 | Por tarea |
| Conflictos sin resolver | Detección automática (divergencias no reconciliadas en output) | Por tarea |
| Tiempo total | Timestamps | Por tarea |
| Tokens consumidos | API usage | Por tarea |
| Satisfacción del "credo" | % de outputs que respetan los 5 principios | Por tarea |

## Results

(Pendiente de ejecución)

## Analysis

(Pendiente de ejecución)

## Next Steps

- Si positivo: iterar sobre la composición óptima de la jerarquía (¿3 niveles o 2? ¿cuántos supervisores?)
- Si negativo: analizar si el overhead burocrático anula los beneficios (como en organizaciones reales)
- Variante interesante: probar modelo "judío" (sin jerarquía, solo texto compartido) vs modelo "católico" (con jerarquía)
