---
id: EX-00002
title: "Simulación de patrones religiosos en sistema multi-agente"
status: draft
created: 2026-03-25
hypothesis: HY-00002
algorithm: ""
tags: [simulación, multi-agente, patrones, resiliencia]
methodology: "A/B test simulado con inyección de fallos"
duration: "2 semanas"
success_criteria: "Recuperación ≥30% más rápida y ≥25% menos fallos en cascada"
---

## Objective

Validar si los patrones de diseño extraídos de arquitecturas religiosas (API mínima, garbage collection periódico, protocolo de consenso) mejoran la resiliencia de un sistema multi-agente frente a fallos.

## Methodology

1. **Implementar sistema base (3 días):**
   - 5 agentes LLM coordinados via message passing estándar
   - Tarea: resolución colaborativa de problemas complejos (code review, análisis de documentos, planificación)
   - Sin roles fijos, comunicación libre entre todos los agentes

2. **Implementar sistema experimental (3 días):**
   - Mismos 5 agentes con 3 patrones religiosos:
   - **Patrón Decálogo:** cada agente expone máximo 10 operaciones, documentadas en un "credo" compartido
   - **Patrón Confesionario:** cada 10 interacciones, cada agente ejecuta un proceso de limpieza de estado (resetear suposiciones, reportar inconsistencias detectadas)
   - **Patrón Liturgia:** las decisiones colectivas siguen una secuencia fija: propuesta → debate → votación → registro

3. **Ejecutar simulaciones (5 días):**
   - 100 ejecuciones por sistema (200 total)
   - En cada ejecución, inyectar fallos aleatorios:
     - Agente caído (no responde)
     - Mensaje corrupto (respuesta incoherente)
     - Partición (2 agentes no pueden comunicarse entre sí)
   - 1-3 fallos por ejecución, timing aleatorio

4. **Análisis (3 días):**
   - Comparar métricas entre ambos sistemas
   - Análisis estadístico de significancia

## Setup

- **Runtime:** TypeScript/Bun
- **LLM:** Claude Sonnet (coste razonable para 200 ejecuciones)
- **Framework:** Script custom de orquestación multi-agente
- **Infraestructura:** Local, sin dependencias cloud
- **Datos:** 20 problemas de complejidad media (code review de PRs reales, análisis de bugs, planificación de features)
- **Inyección de fallos:** Script que aleatoriamente desactiva agentes, corrompe mensajes o bloquea canales

## Algorithm

No aplica aún — si el experimento valida la hipótesis, los patrones se documentarán como AL-00001.

## Success Criteria

- Tiempo medio de recuperación ante fallos ≥30% menor en sistema experimental
- Frecuencia de fallos en cascada (un fallo causa otro) ≥25% menor
- Consistencia del resultado final ≥95% en ambos sistemas
- Diferencia estadísticamente significativa (p<0.05, test de Mann-Whitney)

## Data Collection

| Métrica | Cómo se mide | Frecuencia |
|---------|-------------|------------|
| Tiempo de recuperación | Timestamps desde inyección de fallo hasta output correcto | Por ejecución |
| Fallos en cascada | Contador de fallos secundarios causados por el fallo inyectado | Por ejecución |
| Consistencia de output | Comparación del resultado con golden answer por 3 jueces | Por ejecución |
| Tokens consumidos | Total tokens por ejecución | Por ejecución |
| Latencia total | Tiempo desde input hasta output final | Por ejecución |

## Results

(Pendiente de ejecución)

## Analysis

(Pendiente de ejecución)

## Next Steps

- Si positivo: documentar patrones como Algorithms (AL-00001, AL-00002, AL-00003) y probar con más agentes (10, 20)
- Si negativo: analizar si los patrones añaden overhead sin beneficio, o si la implementación fue incorrecta
- En ambos casos: registrar como Source lo aprendido sobre coordinación multi-agente
