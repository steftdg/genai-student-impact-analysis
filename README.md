# L'IA générative améliore-t-elle vraiment les performances académiques ?

Une analyse de 50 000 profils étudiants  et une leçon sur le p-hacking.

## Contexte

Avec l'adoption massive d'outils comme ChatGPT, Copilot ou Gemini dans la vie étudiante, les établissements scolaires se forgent des avis tranchés — interdire, encadrer, encourager  souvent sans données solides pour appuyer ces décisions.

Ce projet part d'une question simple : **est-ce que l'usage de l'IA générative améliore réellement la performance académique des étudiants ?**

## Démarche

L'analyse suit une approche de test d'hypothèse classique :

- **H0** : l'usage de l'IA générative n'a pas d'effet significatif sur la performance académique
- **H1** : l'usage de l'IA générative améliore la performance académique

**Variable indépendante** : `Weekly_GenAI_Hours`
**Variable dépendante** : `GPA_Change` (Post_Semester_GPA − Pre_Semester_GPA)

Ce notebook documente aussi, honnêtement, une dérive méthodologique rencontrée en cours d'analyse (p-hacking / data dredging)  testée et expliquée plutôt que cachée.

## Résultat principal

Le test ne permet pas de rejeter H0 : malgré une p-value très faible (p < 0.0001) due à la taille de l'échantillon, l'écart réel de progression du GPA entre gros et petits utilisateurs d'IA n'est que de 0.013 point  sans portée pratique.

## Dataset

`ai_student_impact_dataset.csv`  50 000 profils étudiants (usage de l'IA générative, GPA avant/après semestre, anxiété, burnout, dépendance perçue, politique institutionnelle).

## Installation

```bash
pip install -r requirements.txt
jupyter notebook ai_genai_impact_analysis.ipynb
```

## Auteure

Steffi TADOGBE
