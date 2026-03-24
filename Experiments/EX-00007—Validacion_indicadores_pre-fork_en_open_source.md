---
id: EX-00007
title: "Validación de indicadores pre-fork contra forks históricos de open source"
status: draft
created: 2026-03-25
hypothesis: HY-00007
algorithm: ""
tags: [forks, predicción, open-source, validación-histórica]
methodology: "Estudio retrospectivo con clasificador binario"
duration: "4 semanas"
success_criteria: "Precisión ≥70% y recall ≥60% en predicción de forks"
---

## Objective

Validar si los 5 indicadores pre-fork derivados de cismas religiosos pueden predecir forks hostiles en proyectos open source con precisión suficiente para ser útiles como sistema de alerta temprana.

## Methodology

1. **Construcción del dataset (1 semana):**
   - **Casos positivos (forkearon):** ≥12 forks hostiles bien documentados:
     - Node.js → io.js (2014)
     - OpenOffice → LibreOffice (2010)
     - MySQL → MariaDB (2009)
     - Redis → Valkey (2024)
     - Jenkins → Hudson (2011)
     - ownCloud → Nextcloud (2016)
     - Mambo → Joomla (2005)
     - XFree86 → X.Org (2004)
     - FFmpeg → Libav (2011)
     - OpenSSL → LibreSSL (2014)
     - Terraform → OpenTofu (2023)
     - Elasticsearch → OpenSearch (2021)
   - **Casos negativos (no forkearon):** ≥12 proyectos de tamaño similar sin forks hostiles
   - Criterio de matching: tamaño comparable (stars, contributors) en periodo comparable

2. **Medición de indicadores (2 semanas):**
   - Para cada proyecto, medir los 5 indicadores en los 12 meses previos al fork (o periodo equivalente):
   - **I1 — Concentración:** % de merges por top 3 maintainers (GitHub API)
   - **I2 — Rechazo:** ratio issues cerradas como "wontfix"/"not planned" vs total (GitHub API)
   - **I3 — Profetas alternativos:** conteo de blog posts/talks críticos por contributors top-50 (búsqueda manual)
   - **I4 — Divergencia visión/uso:** diferencia entre el roadmap oficial y los PRs más demandados (análisis manual)
   - **I5 — Lenguaje nosotros/ellos:** análisis de sentimiento en issues/discussions con keywords adversariales (NLP)

3. **Modelado (1 semana):**
   - Regresión logística con los 5 indicadores como features
   - Leave-one-out cross-validation (dataset pequeño)
   - Análisis de importancia de features
   - Curva ROC y AUC

## Setup

- **Datos:** GitHub API (GraphQL), Wayback Machine, Google Scholar, blog archives
- **NLP:** Análisis de sentimiento con LLM (Claude Haiku para coste) sobre corpus de issues
- **Análisis:** Python (scikit-learn) o TypeScript
- **Tiempo manual:** ~2 horas por proyecto para I3 e I4 (evaluación cualitativa)

## Algorithm

No aplica aún — si el modelo funciona, los indicadores + umbrales se documentan como Algorithm de predicción.

## Success Criteria

- Precisión ≥70% (de los predichos como fork, ≥70% realmente forkearon)
- Recall ≥60% (de los que forkearon, detecta ≥60%)
- AUC ≥0.75
- Al menos 3 de 5 indicadores con coeficiente significativo (p<0.05)
- El modelo generaliza a ≥2 forks recientes (2023-2024) no usados en entrenamiento

## Data Collection

| Indicador | Fuente | Tipo |
|-----------|--------|------|
| I1 - Concentración | GitHub API: merge authors | Cuantitativo (%) |
| I2 - Rechazo | GitHub API: issue labels/close reasons | Cuantitativo (ratio) |
| I3 - Profetas | Búsqueda manual: blogs, talks, Twitter | Cuantitativo (conteo) + cualitativo |
| I4 - Divergencia | Roadmap vs PRs populares | Cualitativo (escala 1-5) |
| I5 - Lenguaje | NLP sobre issues/discussions | Cuantitativo (score sentimiento) |

## Results

(Pendiente de ejecución)

## Analysis

(Pendiente de ejecución)

## Next Steps

- Si positivo: construir un dashboard de "salud de gobernanza" como herramienta open source
- Si positivo: probar el modelo en tiempo real sobre 5 proyectos grandes y monitorizar durante 6 meses
- Si negativo: investigar qué indicadores faltan (¿dinámicas privadas? ¿factores económicos?)
- Los forks más difíciles de predecir son un Source interesante: ¿qué los hace diferentes?
