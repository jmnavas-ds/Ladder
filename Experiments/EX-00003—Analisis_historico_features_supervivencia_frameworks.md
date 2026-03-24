---
id: EX-00003
title: "Análisis histórico de features de supervivencia en frameworks"
status: draft
created: 2026-03-25
hypothesis: HY-00003
algorithm: ""
tags: [análisis, frameworks, adopción, supervivencia, histórico]
methodology: "Estudio observacional retrospectivo con scoring ciego"
duration: "3 semanas"
success_criteria: "Correlación ≥0.6 entre features de supervivencia y adopción a 10 años"
---

## Objective

Determinar si las features de supervivencia identificadas en religiones longevas (bajo acoplamiento, mecanismo de reset, narrativa de propósito, escalabilidad de uso) predicen la adopción sostenida de frameworks de software a 10 años.

## Methodology

1. **Selección de muestra (3 días):**
   - Identificar 30 frameworks lanzados entre 2005-2015
   - 15 que siguen activos y adoptados ("supervivientes")
   - 15 que fueron abandonados o marginalizados ("extintos")
   - Criterio de inclusión: ≥1000 stars al pico, documentación pública suficiente

2. **Scoring ciego (5 días):**
   - 3 evaluadores independientes puntúan cada framework en las 4 features (0 o 1):
     - **Bajo acoplamiento:** ¿se adapta a múltiples contextos culturales/técnicos sin modificación del core?
     - **Mecanismo de reset:** ¿permite deshacer errores fácilmente? (undo, rollback, migration)
     - **Narrativa de propósito:** ¿tiene una misión clara que trasciende la funcionalidad? ("Learn once, write anywhere")
     - **Escalabilidad de uso:** ¿funciona igual de bien para 1 persona que para 1000?
   - Evaluadores no saben si el framework es "superviviente" o "extinto"
   - Inter-rater reliability: Cohen's kappa ≥0.7 requerido

3. **Medición de adopción (3 días):**
   - Descargas npm/pip/maven a 10 años del lanzamiento
   - Stars y contributors activos actuales
   - Menciones en Stack Overflow (tendencia 10 años)
   - Normalizar todas las métricas a escala 0-100

4. **Análisis estadístico (3 días):**
   - Correlación de Spearman entre score total (0-4) y adopción normalizada
   - Regresión logística: ¿qué features son más predictivas?
   - Análisis de outliers: frameworks que desafían el modelo

## Setup

- **Datos:** GitHub API, npm/PyPI stats, Stack Overflow Data Explorer, Wayback Machine para datos históricos
- **Herramientas:** Python/pandas para análisis, o TypeScript si se prefiere mantener coherencia con Ladder
- **Evaluadores:** 3 personas con conocimiento de ecosistema de software (pueden ser agentes LLM con prompts distintos para simular evaluadores independientes)

## Algorithm

No aplica aún — si se confirma, las features de supervivencia se documentarán como un Algorithm de evaluación.

## Success Criteria

- Correlación de Spearman ≥0.6 (p<0.01) entre score y adopción
- Los 5 frameworks más longevos tienen score ≥3
- Los 5 más abandonados tienen score ≤2
- Al menos 2 de las 4 features son individualmente significativas (p<0.05)

## Data Collection

| Métrica | Fuente | Formato |
|---------|--------|---------|
| Score features (0-4) | Evaluación ciega por 3 jueces | CSV: framework, feature1, feature2, feature3, feature4, total |
| Descargas a 10 años | npm/PyPI/Maven stats | Número absoluto + tendencia |
| Stars actuales | GitHub API | Número |
| Contributors activos | GitHub API (commits último año) | Número |
| Menciones Stack Overflow | SO Data Explorer | Número por año |

## Results

(Pendiente de ejecución)

## Analysis

(Pendiente de ejecución)

## Next Steps

- Si positivo: crear un "Checklist de Supervivencia" como Algorithm, aplicable al diseño de nuevos frameworks y productos
- Si negativo: investigar qué variables omitidas explican mejor la longevidad (timing, ecosistema, funding)
- Análisis de outliers como nuevo Source: ¿por qué algunos frameworks sobreviven sin las features esperadas?
