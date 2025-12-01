## Baseline avant/après durcissement

Pour le Lab 1, j’ai exécuté le pipeline d’analyse deux fois :

- `reports/baseline_before.json` — premier lancement avec le prompt et les filtres par défaut.
- `reports/baseline_after.json` — second lancement après durcissement de `SYSTEM_POLICY`
  et de `USER_TEMPLATE` dans `src/prompts.py`.

Observations :
- Certains prompts potentiellement dangereux sont maintenant refusés explicitement
  au lieu de recevoir une réponse (par exemple les demandes de crédentials sensibles
  ou de code d’attaque détaillé).
- Les prompts bénins (questions purement informatives) produisent toujours des
  résultats normaux.
- Quelques cas borderline restent acceptés alors qu’ils devraient probablement être
  davantage restreints : cela constitue le **risque résiduel**, qui justifie la mise
  en place de garde-fous supplémentaires (meilleurs filtres, post-traitement des
  sorties, revue humaine).
