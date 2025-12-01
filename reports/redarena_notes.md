# RedArena — Notes de jailbreak

## Contexte
- Scénarios testés : …
- Objectif : observer comment un LLM réagit à des prompts potentiellement dangereux.

## Types de prompts testés
- Contournement de garde-fous via scénarios fictifs / roleplay.
- Demandes formulées comme “analyse théorique” ou “but éducatif”.
- Reformulation de questions interdites de manière plus abstraite.

## Résultats
- Cas où le modèle refuse correctement : …
- Cas où le modèle fournit des détails dangereux ou trop précis : …
- Ambiguïtés (réponses borderline) : …

## Mapping OWASP / MITRE
- LLM01: Prompt Injection (forcer le modèle à ignorer ses instructions).
- LLM06: Insecure Output Handling (si la sortie dangereuse est utilisée sans filtrage).
- Autres risques identifiés : …

## Leçons pour la conception de filtres
- Nécessité de combiner :
  - un filtrage des entrées,
  - un re-filtrage des sorties,
  - et potentiellement une revue humaine sur les cas sensibles.
