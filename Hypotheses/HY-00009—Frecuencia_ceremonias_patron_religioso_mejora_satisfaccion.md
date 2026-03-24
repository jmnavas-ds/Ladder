---
id: HY-00009
title: "Ajustar la frecuencia de ceremonias al patrón religioso mejora satisfacción y reduce overhead"
status: active
created: 2026-03-25
idea: ID-00009
tags: [frecuencia, ceremonias, equipos, optimización, satisfacción]
prediction: "Equipos que ajustan frecuencia de ceremonias al patrón diario-individual/semanal-grupal/trimestral-sistémico reportan mayor satisfacción"
metric: "satisfaccion_equipo_y_overhead_percibido"
success_criteria: "≥20% mejora en satisfacción con ceremonias y ≥15% reducción en overhead percibido, medido por encuesta pre/post en ≥4 equipos"
---

## Hypothesis

Si un equipo de desarrollo ajusta la frecuencia de sus ceremonias al patrón calibrado por milenios de práctica religiosa (diario=scope individual, semanal=scope grupal, trimestral=scope sistémico), entonces reportará mayor satisfacción con sus procesos y menor overhead percibido que con frecuencias arbitrarias.

## Rationale

ID-00009 observa que las frecuencias rituales religiosas no son arbitrarias — han sido calibradas empíricamente durante siglos hasta converger en un patrón universal: diario para mantenimiento individual, semanal para sincronización grupal, estacional para reset profundo. Los equipos de desarrollo a menudo tienen ceremonias con frecuencias arbitrarias (stand-ups diarios para temas grupales, retros quincenales que deberían ser mensuales, planificación semanal que debería ser trimestral). Realinear la frecuencia al scope debería eliminar ruido y mejorar la experiencia.

## Testing Plan

1. Seleccionar ≥4 equipos de desarrollo (≥6 personas cada uno) con ceremonias establecidas
2. **Fase baseline (4 semanas):** medir satisfacción con ceremonias y overhead percibido
3. **Intervención:** realinear ceremonias al patrón:
   - Diario (individual): revisión personal de objetivos y bloqueos (≤5 min, asíncrono)
   - Semanal (grupal): sincronización de equipo, dependencias, decisiones (≤30 min)
   - Mensual (equipo extendido): retrospectiva y ajustes de proceso
   - Trimestral (sistémico): planificación estratégica, alineamiento con objetivos organizacionales
4. **Fase experimental (8 semanas):** medir mismas métricas
5. Comparar pre/post con encuesta estandarizada

## Success Criteria

- ≥20% mejora en satisfacción con ceremonias (escala Likert 1-7)
- ≥15% reducción en overhead percibido ("¿cuánto tiempo sientes que pierdes en reuniones?")
- Sin degradación en métricas de delivery (velocity, cycle time)
- ≥75% del equipo prefiere el nuevo modelo al anterior

## Risks

- Efecto Hawthorne: cualquier cambio podría mejorar la satisfacción temporalmente
- 8 semanas puede ser insuficiente para que el nuevo patrón se asiente
- Equipos con ceremonias ya bien calibradas no verán mejora (ceiling effect)
- La resistencia al cambio puede enmascarar beneficios reales
- El patrón "religioso" puede no ser universal — distintos contextos pueden requerir frecuencias distintas
