---
id: HY-00007
title: "5 indicadores pre-fork predicen bifurcaciones en proyectos open source con 70% de precisión"
status: active
created: 2026-03-25
idea: ID-00007
tags: [forks, predicción, open-source, indicadores, gobernanza]
prediction: "Los 5 indicadores pre-fork identificados en cismas religiosos predicen forks hostiles en software con ≥70% de precisión"
metric: "precision_prediccion_forks"
success_criteria: "Precisión ≥70% y recall ≥60% validado contra ≥10 forks históricos documentados y ≥10 proyectos que no forkearon"
---

## Hypothesis

Si se monitorizan 5 indicadores pre-fork derivados de cismas religiosos (concentración de decisiones, quejas rechazadas, profetas alternativos, divergencia visión/uso, lenguaje nosotros-vs-ellos), entonces se pueden predecir forks hostiles en proyectos open source con al menos un 70% de precisión.

## Rationale

ID-00007 argumenta que los cismas religiosos y los forks de software siguen mecánicas idénticas. Si los síntomas previos son los mismos, un modelo basado en indicadores de cismas debería funcionar para software. Casos de validación disponibles:
- Node.js → io.js (2014): concentración en Joyent, issues rechazadas, emergencia de líderes alternativos
- OpenOffice → LibreOffice (2010): Oracle centralizando, comunidad alienada
- MySQL → MariaDB (2009): misma dinámica post-adquisición Oracle
- Redis → Valkey (2024): cambio de licencia, divergencia visión/comunidad

## Testing Plan

1. Recopilar datos históricos de ≥10 forks hostiles documentados y ≥10 proyectos de tamaño similar que NO forkearon (grupo control)
2. Para cada proyecto, medir los 5 indicadores en los 12 meses previos al fork (o periodo equivalente para el control):
   - Concentración: % de commits/merges por top 3 maintainers
   - Rechazo: ratio issues cerradas sin resolver / issues totales
   - Profetas: aparición de blogs/talks críticos por contributors significativos
   - Divergencia: diferencia entre el roadmap oficial y los PRs de la comunidad
   - Lenguaje: análisis de sentimiento en issues/discussions (nosotros vs. ellos)
3. Entrenar un clasificador simple (regresión logística) y evaluar con cross-validation

## Success Criteria

- Precisión ≥70% (de los que predice como fork, ≥70% realmente forkearon)
- Recall ≥60% (de los que realmente forkearon, detecta ≥60%)
- Al menos 3 de los 5 indicadores son estadísticamente significativos (p<0.05)

## Risks

- Muestra pequeña: puede que no haya suficientes forks hostiles bien documentados para entrenar un modelo robusto
- Los indicadores pueden ser correlación, no causación — proyectos en crisis muestran estos síntomas pero la causa puede ser otra
- Sesgo retrospectivo: sabiendo qué proyectos forkearon, es fácil "ver" los indicadores en los datos históricos
- Los datos públicos (issues, commits) pueden no capturar la dinámica real (que a menudo ocurre en canales privados)
