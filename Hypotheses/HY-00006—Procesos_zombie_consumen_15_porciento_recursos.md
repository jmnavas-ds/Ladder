---
id: HY-00006
title: "Los procesos zombie consumen más del 15% de los recursos de un equipo"
status: active
created: 2026-03-25
idea: ID-00006
tags: [procesos-zombie, desperdicio, organizaciones, mantenimiento]
prediction: "Los procesos organizacionales en fase zombie (se ejecutan por inercia sin valor claro) consumen más del 15% de los recursos del equipo"
metric: "porcentaje_recursos_en_procesos_zombie"
success_criteria: "≥15% de horas-persona dedicadas a procesos que, al eliminarlos, no generan impacto negativo medible en 8 semanas"
---

## Hypothesis

Si se auditan los procesos recurrentes de un equipo de desarrollo usando el framework de ciclo de vida ritual→proceso (init, running, deprecated, zombie, killed), entonces se descubrirá que más del 15% de los recursos del equipo están dedicados a procesos en fase "zombie" — que se ejecutan por inercia pero que pueden eliminarse sin impacto negativo.

## Rationale

ID-00006 establece que los procesos organizacionales siguen el mismo ciclo de vida que los rituales religiosos. La Navidad celebrada por ateos es un ejemplo de ritual zombie — se ejecuta sin su función original. Las organizaciones acumulan equivalentes: reuniones que ya no sirven, reportes que nadie lee, aprobaciones que siempre se conceden, documentación que nunca se consulta. Como nadie los "mata" explícitamente, consumen recursos indefinidamente.

## Testing Plan

1. Seleccionar 5 equipos de desarrollo de diferentes organizaciones (≥10 personas cada uno)
2. Inventariar todos los procesos recurrentes (reuniones, reportes, revisiones, ceremonias)
3. Clasificar cada proceso según el ciclo de vida: init, running, forked, deprecated, patched, zombie, killed
4. Para los clasificados como zombie: eliminarlos durante 8 semanas
5. Medir impacto: productividad, satisfacción, incidentes, calidad de entregables

## Success Criteria

- ≥15% de horas-persona liberadas al eliminar procesos zombie
- Cero impacto negativo medible en productividad, calidad o incidentes durante las 8 semanas sin ellos
- ≥80% del equipo confirma que no nota su ausencia

## Risks

- Algunos procesos "zombie" pueden tener funciones latentes no evidentes (seguridad psicológica, cohesión social)
- 8 semanas puede ser insuficiente para detectar impactos de largo plazo (como dejar de hacer backups y no notarlo hasta el desastre)
- Sesgo de confirmación: equipos pueden no reportar problemas para validar la eliminación
- La clasificación zombie vs. deprecated puede ser subjetiva
