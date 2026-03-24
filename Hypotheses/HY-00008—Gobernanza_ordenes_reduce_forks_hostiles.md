---
id: HY-00008
title: "Gobernanza tipo órdenes religiosas reduce forks hostiles en IA"
status: active
created: 2026-03-25
idea: ID-00008
tags: [gobernanza, forks, IA, órdenes, extensiones]
prediction: "Proyectos con core estricto + extensiones autónomas sufren menos forks hostiles que los con BDFL"
metric: "tasa_forks_hostiles"
success_criteria: "Proyectos tipo 'órdenes' tienen ≤50% de la tasa de forks hostiles comparados con proyectos tipo BDFL, en una muestra de ≥30 proyectos"
---

## Hypothesis

Si un proyecto open source de IA implementa un modelo de gobernanza tipo "órdenes religiosas" (core doctrinal estricto + extensiones/plugins con alta autonomía interna), entonces sufrirá significativamente menos forks hostiles que proyectos con gobernanza tipo BDFL (Benevolent Dictator For Life).

## Rationale

La Iglesia Católica ha mantenido unidad durante 2000 años a pesar de tensiones enormes, en parte gracias a las órdenes religiosas: franciscanos, jesuitas, dominicos tienen carismas y prácticas muy distintas, pero comparten un core doctrinal innegociable. Esta estructura absorbe la diversidad sin fork. Contraste: el protestantismo surgió cuando no había mecanismo para canalizar la disidencia de Lutero dentro del sistema. En software, los proyectos con arquitectura de plugins (WordPress, VSCode) absorben la diversidad mejor que los monolíticos con un líder único.

## Testing Plan

1. Clasificar ≥30 proyectos open source de IA según modelo de gobernanza:
   - **Tipo BDFL:** decisiones centralizadas en un líder (ej: proyectos pre-fork de Redis)
   - **Tipo órdenes:** core + extensiones autónomas (ej: Hugging Face con sus hubs)
   - **Tipo descentralizado:** sin autoridad clara (ej: algunos proyectos de la Linux Foundation)
2. Contar forks hostiles en los últimos 5 años por categoría
3. Normalizar por tamaño del proyecto (stars, contributors) para comparación justa

## Success Criteria

- Tasa de forks hostiles en proyectos tipo "órdenes" ≤50% de la tasa en tipo BDFL
- Diferencia estadísticamente significativa (p<0.05)
- El modelo tipo "órdenes" no muestra menor tasa de innovación (medida en features/año) como efecto secundario

## Risks

- La clasificación de gobernanza puede ser subjetiva y difícil de operacionalizar
- Pocos proyectos de IA tienen suficiente historia para evaluar forks hostiles
- Factores confusos: proyectos con más recursos (y por tanto con tipo "órdenes") podrían simplemente tener menos motivos de insatisfacción
- La analogía puede no transferir: las órdenes religiosas funcionan por vocación; los contributors de open source tienen motivaciones distintas
