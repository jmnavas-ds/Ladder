---
id: EX-00006
title: "Auditoría de procesos zombie en equipos de desarrollo"
status: draft
created: 2026-03-25
hypothesis: HY-00006
algorithm: ""
tags: [procesos-zombie, auditoría, equipos, desperdicio]
methodology: "Auditoría + intervención con grupo de control temporal"
duration: "12 semanas (4 baseline + 8 intervención)"
success_criteria: "≥15% de horas-persona liberadas sin impacto negativo"
---

## Objective

Determinar qué porcentaje de los recursos de un equipo de desarrollo se dedican a procesos "zombie" (que se ejecutan por inercia sin valor claro) y validar que pueden eliminarse sin impacto negativo.

## Methodology

1. **Reclutamiento (1 semana):**
   - Contactar ≥5 equipos de desarrollo (≥10 personas cada uno)
   - Requisito: equipo con al menos 1 año de antigüedad y ceremonias establecidas
   - Compromiso: participar 12 semanas y reportar métricas

2. **Inventario de procesos (1 semana):**
   - Cada equipo lista todos sus procesos recurrentes:
     - Reuniones (stand-ups, retros, planning, 1:1s, all-hands)
     - Reportes (status updates, dashboards, weekly emails)
     - Revisiones (code review, design review, security review)
     - Aprobaciones (deploy approval, access requests, purchase orders)
     - Documentación (ADRs, changelogs, meeting notes)
   - Para cada proceso: frecuencia, duración, participantes, antigüedad

3. **Clasificación (1 semana):**
   - Clasificar cada proceso según el ciclo de vida de ID-00006:
   - **Running:** se ejecuta y cumple su función original
   - **Patched:** se ha modificado para adaptarse pero sigue siendo útil
   - **Deprecated:** reconocido como poco útil pero nadie lo ha eliminado
   - **Zombie:** se ejecuta por inercia, nadie sabe bien para qué sirve
   - Clasificación por consenso del equipo (votación anónima)

4. **Baseline (4 semanas):**
   - Medir: velocity, cycle time, incidentes, satisfacción del equipo (encuesta semanal)
   - Registrar horas-persona dedicadas a cada proceso

5. **Intervención (8 semanas):**
   - Eliminar todos los procesos clasificados como "zombie"
   - Mantener los "deprecated" como grupo de control (no eliminar aún)
   - Medir las mismas métricas que en baseline
   - Check-in quincenal: ¿alguien echa de menos algún proceso eliminado?

## Setup

- **Equipos:** ≥5, diversos (startup, enterprise, open source)
- **Herramientas de medición:** Jira/Linear para velocity, encuesta Typeform/Google Forms para satisfacción
- **Coordinación:** Un facilitador por equipo que gestiona el inventario y la clasificación
- **Coste:** Principalmente tiempo de coordinación, sin coste de herramientas

## Algorithm

Usar el framework de ciclo de vida ritual→proceso de ID-00006 como método de clasificación.

## Success Criteria

- ≥15% de horas-persona dedicadas a procesos zombie (confirmando la hipótesis)
- Al eliminarlos: cero degradación en velocity, cycle time e incidentes durante 8 semanas
- ≥80% del equipo no echa de menos los procesos eliminados
- Satisfacción del equipo se mantiene o mejora

## Data Collection

| Métrica | Fuente | Frecuencia |
|---------|--------|------------|
| Horas en procesos recurrentes | Auto-reporte + calendarios | Semanal |
| Velocity | Jira/Linear | Por sprint |
| Cycle time | Jira/Linear | Por sprint |
| Incidentes | Sistema de monitorización | Semanal |
| Satisfacción | Encuesta 1-7 Likert | Semanal |
| "¿Echas de menos algún proceso?" | Check-in anónimo | Quincenal |

## Results

(Pendiente de ejecución)

## Analysis

(Pendiente de ejecución)

## Next Steps

- Si positivo: crear un "Protocolo de Auditoría Zombie" como Algorithm, aplicable a cualquier equipo
- Si positivo: repetir con procesos "deprecated" (la siguiente capa)
- Si negativo: investigar qué función oculta cumplen los procesos zombie (cohesión social, seguridad psicológica, etc.)
- Publicar hallazgos como Source para alimentar el loop
