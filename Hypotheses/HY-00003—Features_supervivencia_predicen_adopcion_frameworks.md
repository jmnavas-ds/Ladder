---
id: HY-00003
title: "Las features de supervivencia religiosa predicen adopción de frameworks de software"
status: active
created: 2026-03-25
idea: ID-00003
tags: [adopción, supervivencia, frameworks, predicción]
prediction: "Frameworks con bajo acoplamiento, mecanismo de reset, narrativa de propósito y escalabilidad de uso tienen mayor adopción a largo plazo"
metric: "adopcion_a_10_anos"
success_criteria: "Correlación ≥0.6 entre número de features de supervivencia (0-4) y adopción sostenida a 10 años, validado contra 20+ frameworks"
---

## Hypothesis

Si un framework de software implementa al menos 3 de las 4 features de supervivencia identificadas en religiones longevas (bajo acoplamiento cultural, mecanismo de reset/perdón, narrativa de propósito trascendente, escalabilidad de uso individual-colectivo), entonces tendrá mayor adopción sostenida a 10 años que los que implementan 2 o menos.

## Rationale

Las religiones que han sobrevivido milenios comparten features estructurales que las religiones extintas no tenían. Si estas features son principios universales de sistemas que necesitan adopción masiva y persistencia, deberían predecir también el éxito de frameworks de software:

- **Bajo acoplamiento:** React se adapta a web, mobile, desktop (como el Islam de Marruecos a Indonesia)
- **Reset:** Git permite revertir cualquier error (como la confesión restaura estado limpio)
- **Narrativa:** "Learn once, write anywhere" (como "Ama al prójimo como a ti mismo")
- **Escalabilidad:** Puedes usar React solo o en equipo de 1000 (como rezar solo o en catedral)

## Testing Plan

1. Seleccionar 30 frameworks lanzados entre 2005-2015 (suficiente historia para medir 10 años)
2. Puntuar cada uno en las 4 features (0 o 1 por feature, total 0-4)
3. Medir adopción sostenida: descargas, stars, contribuidores activos a 10 años del lanzamiento
4. Calcular correlación entre puntuación de features y adopción sostenida

## Success Criteria

- Correlación (Spearman) ≥0.6 entre puntuación de features y adopción a 10 años
- Los 5 frameworks más longevos tienen puntuación ≥3
- Los 5 frameworks más abandonados tienen puntuación ≤2

## Risks

- El scoring de features puede ser subjetivo — dos evaluadores podrían puntuar distinto
- La adopción depende de muchos factores (timing, marketing, ecosistema) que esta hipótesis no controla
- Sesgo de supervivencia: solo analizamos frameworks conocidos, no los miles que murieron en silencio
