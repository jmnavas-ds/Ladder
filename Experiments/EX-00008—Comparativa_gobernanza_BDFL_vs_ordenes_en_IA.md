---
id: EX-00008
title: "Comparativa de gobernanza BDFL vs órdenes en proyectos de IA open source"
status: draft
created: 2026-03-25
hypothesis: HY-00008
algorithm: ""
tags: [gobernanza, BDFL, órdenes, IA, open-source, comparativa]
methodology: "Estudio observacional cross-sectional"
duration: "3 semanas"
success_criteria: "Tasa de forks hostiles ≤50% en tipo órdenes vs tipo BDFL"
---

## Objective

Determinar si los proyectos open source de IA con gobernanza tipo "órdenes religiosas" (core estricto + extensiones autónomas) sufren menos forks hostiles que los que usan gobernanza tipo BDFL.

## Methodology

1. **Selección y clasificación de proyectos (1 semana):**
   - Identificar ≥30 proyectos open source de IA con ≥2 años de historia y ≥500 contributors
   - Clasificar cada proyecto según modelo de gobernanza:
   - **Tipo BDFL:** decisiones centralizadas en un líder o empresa. Señales: un solo approver para decisiones de diseño, roadmap definido unilateralmente, governance doc ausente o nominal
   - **Tipo órdenes:** core mantenido centralmente + ecosistema de extensiones con autonomía. Señales: plugin system, RFC process, SIGs o working groups, governance doc con roles claros
   - **Tipo descentralizado:** sin autoridad clara. Señales: múltiples forks activos sin hostilidad, decisiones por consenso informal
   - 2 clasificadores independientes, resolver discrepancias por discusión

2. **Medición de forks hostiles (1 semana):**
   - Para cada proyecto: contar forks que cumplan criterios de "hostil":
     - Fork público con comunicación crítica hacia el proyecto original
     - ≥10% de los contributors migran al fork en los primeros 6 meses
     - El fork tiene governance doc propio y roadmap diferenciado
   - Normalizar por tamaño (forks hostiles por cada 1000 contributors)

3. **Análisis (1 semana):**
   - Comparar tasa de forks hostiles por tipo de gobernanza
   - Test de Fisher o chi-cuadrado para significancia
   - Controlar por variables confusas: tamaño, edad, funding, dominio

## Setup

- **Datos:** GitHub API, governance docs, blog posts de anuncio de forks, comunicados oficiales
- **Proyectos candidatos:** PyTorch, TensorFlow, Hugging Face, LangChain, scikit-learn, Keras, JAX, ONNX, etc.
- **Clasificación:** Rúbrica estandarizada con ejemplos de cada tipo

## Algorithm

No aplica aún — si se confirma, el modelo de gobernanza tipo "órdenes" se documenta como Algorithm de diseño organizacional.

## Success Criteria

- Tasa normalizada de forks hostiles en tipo "órdenes" ≤50% de la tasa en tipo BDFL
- Diferencia estadísticamente significativa (p<0.05)
- La tasa de innovación (features/releases por año) en tipo "órdenes" no es inferior a tipo BDFL
- Resultados robustos a variaciones en la definición de "fork hostil"

## Data Collection

| Métrica | Fuente | Tipo |
|---------|--------|------|
| Tipo de gobernanza | Governance docs + clasificación manual | Categórica (BDFL/órdenes/descentralizado) |
| Forks hostiles | GitHub + búsqueda de comunicaciones | Conteo |
| Tamaño del proyecto | GitHub API (stars, contributors) | Numérico |
| Edad del proyecto | Fecha primer commit | Numérico (años) |
| Tasa de innovación | Releases + features por año | Numérico |
| Funding | Crunchbase, blog posts | Categórica (empresa/fundación/comunidad) |

## Results

(Pendiente de ejecución)

## Analysis

(Pendiente de ejecución)

## Next Steps

- Si positivo: diseñar una "guía de gobernanza tipo órdenes" para nuevos proyectos de IA como Algorithm
- Si positivo: probar la guía en un proyecto real (experimento prospectivo)
- Si negativo: investigar si el modelo de gobernanza importa menos que el factor "quién paga" (empresas vs comunidad)
- Datos de gobernanza como nuevo Source para alimentar el loop
