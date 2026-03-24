---
id: EX-00009
title: "Intervención de frecuencia de ceremonias en equipos de desarrollo"
status: draft
created: 2026-03-25
hypothesis: HY-00009
algorithm: ""
tags: [ceremonias, frecuencia, equipos, intervención, satisfacción]
methodology: "Estudio pre/post con intervención controlada"
duration: "12 semanas (4 baseline + 8 intervención)"
success_criteria: "≥20% mejora en satisfacción y ≥15% reducción en overhead percibido"
---

## Objective

Validar si ajustar la frecuencia de ceremonias de un equipo al patrón calibrado por milenios de práctica religiosa (diario=individual, semanal=grupal, mensual=equipo extendido, trimestral=sistémico) mejora la satisfacción y reduce el overhead percibido.

## Methodology

1. **Reclutamiento (1 semana):**
   - ≥4 equipos de desarrollo, ≥6 personas cada uno
   - Requisito: ceremonias establecidas con al menos 6 meses de antigüedad
   - Diversidad: incluir equipos con exceso de reuniones Y con pocas reuniones

2. **Diagnóstico (1 semana):**
   - Inventariar ceremonias actuales de cada equipo
   - Clasificar cada ceremonia por scope:
     - **Individual:** stand-up, daily check-in, journaling
     - **Grupal:** planning, sync, design review
     - **Equipo extendido:** retro, demo, all-hands
     - **Sistémico:** planificación trimestral, OKRs, strategy
   - Identificar desalineamientos: ceremonias grupales con frecuencia diaria, ceremonias individuales con frecuencia mensual, etc.

3. **Baseline (4 semanas):**
   - Encuesta semanal (2 min):
     - "¿Cuánto valoras las reuniones de esta semana?" (1-7)
     - "¿Cuánto tiempo sientes que pierdes en reuniones?" (% estimado)
     - "¿Hubo alguna reunión que no debería haber existido?" (sí/no + cuál)
   - Métricas de delivery: velocity, cycle time, PRs mergeados

4. **Intervención (8 semanas):**
   - Realinear ceremonias al patrón:
     - **Diario (individual):** Check-in asíncrono en Slack/chat, ≤5 min, cada uno a su ritmo. Pregunta: "¿Qué voy a hacer hoy? ¿Tengo algún bloqueo?"
     - **Semanal (grupal):** Una reunión síncrona ≤30 min. Agenda: dependencias, decisiones pendientes, demo rápida
     - **Mensual (equipo extendido):** Retrospectiva + ajustes de proceso. ≤60 min
     - **Trimestral (sistémico):** Planificación, alineamiento con objetivos organizacionales. ≤2 horas
   - Eliminar ceremonias que no encajan en ninguna categoría
   - Misma encuesta semanal que en baseline

5. **Análisis (1 semana):**
   - Comparar pre/post: satisfacción, overhead percibido, métricas de delivery
   - Entrevistas cualitativas con ≥2 personas por equipo

## Setup

- **Equipos:** ≥4, preferiblemente de organizaciones distintas
- **Encuesta:** Google Forms o Typeform, 2 min máximo
- **Métricas:** Jira/Linear para velocity y cycle time
- **Facilitación:** Un facilitador que guíe la transición sin ser intrusivo
- **Coste:** Tiempo de coordinación únicamente

## Algorithm

El patrón de frecuencia (diario-individual/semanal-grupal/mensual-extendido/trimestral-sistémico) es el candidato a Algorithm si se valida.

## Success Criteria

- Satisfacción con ceremonias ≥20% superior (media escala Likert 1-7)
- Overhead percibido ≥15% menor
- Velocity y cycle time sin degradación (≤5% de variación)
- ≥75% del equipo prefiere el nuevo modelo
- Efecto se mantiene en las semanas 6-8 (no es solo novedad)

## Data Collection

| Métrica | Fuente | Frecuencia |
|---------|--------|------------|
| Satisfacción con ceremonias | Encuesta Likert 1-7 | Semanal |
| Overhead percibido | Encuesta (% tiempo) | Semanal |
| Reuniones innecesarias | Encuesta (sí/no + cuál) | Semanal |
| Velocity | Jira/Linear | Por sprint |
| Cycle time | Jira/Linear | Por sprint |
| PRs mergeados | GitHub | Semanal |
| Feedback cualitativo | Entrevistas | Semanas 4 y 8 |

## Results

(Pendiente de ejecución)

## Analysis

(Pendiente de ejecución)

## Next Steps

- Si positivo: documentar el "Protocolo de Frecuencia de Ceremonias" como Algorithm
- Si positivo: probar variantes (¿quincenal en lugar de mensual? ¿bi-diario para equipos críticos?)
- Si negativo: investigar si la frecuencia importa menos que el formato o la facilitación
- Si mixto: segmentar por tipo de equipo — ¿funciona mejor en remoto que en presencial?
- Publicar hallazgos como Source y como artículo (loop + divulgación)
