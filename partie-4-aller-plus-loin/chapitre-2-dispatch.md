# Dispatch — Plusieurs agents en parallèle

Un agent Cowork travaille en séquence : il fait A, puis B, puis C. C'est suffisant pour la plupart des tâches.

Mais certaines tâches sont parallélisables par nature. Analyser 30 entreprises, traiter 50 emails, générer 15 variantes d'un même contenu. Les faire en séquence prend du temps. Les faire en parallèle — avec plusieurs agents travaillant simultanément — prend une fraction du temps.

C'est ce que fait Dispatch.

---

## Le principe

Dispatch divise une tâche en sous-tâches identiques et les distribue à plusieurs agents qui tournent en même temps. Chaque agent prend en charge une unité de travail, produit son résultat, et Cowork consolide ensuite l'ensemble.

```
Dispatch reçoit : "Analyse ces 30 entreprises"
         ↓
Agent 1 → Analyse entreprises 1-10
Agent 2 → Analyse entreprises 11-20
Agent 3 → Analyse entreprises 21-30
         ↓
Cowork consolide → 1 rapport avec 30 analyses
```

Au lieu de 3h de traitement séquentiel, vous obtenez un résultat en 1h.

---

## Quand utiliser Dispatch

**Traitement de volume.** Vous avez une liste d'éléments à traiter de façon identique — chaque élément reçoit le même traitement, mais ils sont indépendants les uns des autres.

**Génération de variantes.** Vous voulez plusieurs versions d'un même contenu : 10 accroches différentes pour un post, 5 angles de présentation pour une offre, 3 niveaux de détail d'un même résumé.

**Recherche multi-sources.** Chercher la même information dans 20 sources différentes simultanément plutôt qu'en séquence.

---

## Comment activer Dispatch

Dans votre instruction, ajoutez la directive Dispatch avec votre liste d'éléments et le nombre d'agents à utiliser :

```
[DISPATCH — 5 agents]
LISTE :
- Entreprise A
- Entreprise B
- Entreprise C
[...]

Pour chaque élément de la liste, exécute la tâche suivante :
[votre instruction de tâche]

CONSOLIDATION :
À la fin, fusionne tous les résultats dans un seul document structuré.
```

Cowork déterminera automatiquement comment répartir le travail entre les agents selon le nombre disponible.

---

## Exemple — Analyse de prospects en masse

```
[DISPATCH — 5 agents]
LISTE :
- Acme Corp (acmecorp.com)
- Beta Solutions (betasolutions.ch)
- Gamma Tech (gammatech.com)
- Delta Services (deltaservices.fr)
- Epsilon Group (epsilongroup.com)
[...continuez la liste...]

Pour chaque entreprise :
1. Cherche leur site web, leur page LinkedIn, leurs actualités récentes
2. Identifie : taille, secteur, enjeux actuels, décideurs visibles
3. Évalue : notre offre est-elle pertinente ? Pourquoi ?
4. Rédige un brief de 10 lignes : contexte + angle d'approche recommandé

CONSOLIDATION :
Crée un fichier ./Outputs/analyse-prospects-[date].md avec :
- Un brief par entreprise (titre = nom entreprise)
- À la fin : tableau récapitulatif (entreprise / pertinence / action recommandée)
Trie par ordre de pertinence décroissante.
```

---

## Exemple — Génération de variantes de contenu

```
[DISPATCH — 3 agents]

Génère 3 versions différentes de la même annonce pour [votre produit/service].

Agent 1 : Version "problème" — commence par la douleur du lecteur,
solution en deuxième temps. Ton : direct, empathique.

Agent 2 : Version "résultat" — commence par le résultat obtenu par
un client type, explique comment. Ton : factuel, rassurant.

Agent 3 : Version "différenciation" — commence par ce qui rend notre
approche unique vs les alternatives. Ton : confiant, sans arrogance.

Chaque version : 150-200 mots, terminée par un CTA.

CONSOLIDATION :
Regroupe les 3 versions dans ./Outputs/variantes-annonce-[date].md
avec un titre clair pour chaque version et un commentaire éditorial
d'une ligne sur le meilleur usage de chaque variante.
```

---

## Limites de Dispatch

**Il ne convient pas aux tâches séquentielles.** Si la sous-tâche B dépend du résultat de A, Dispatch n't est pas adapté. C'est un outil pour les tâches parallélisables uniquement.

**La consolidation demande de la précision.** Indiquez toujours dans votre instruction comment vous voulez que les résultats soient fusionnés. Un Dispatch sans instructions de consolidation claire peut produire un résultat difficile à utiliser.

**Chaque agent consomme du contexte.** Dispatch multiplie les ressources utilisées. Pour des listes de 100+ éléments, découpez en plusieurs passes plutôt qu'une seule instruction massive.

---

## Dispatch vs Tâche planifiée

Ces deux fonctionnalités se complètent :

| | Tâche planifiée | Dispatch |
|---|---|---|
| **Usage** | Récurrence dans le temps | Volume en un seul run |
| **Exemple** | Brief matinal chaque jour | Analyser 50 prospects en une fois |
| **Parallélisme** | Non (1 agent) | Oui (N agents) |
| **Déclencheur** | Calendrier ou manuel | Manuel ou dans une tâche |

Vous pouvez combiner les deux : une tâche planifiée qui, chaque lundi, lance un Dispatch sur la liste d'entreprises ajoutées pendant la semaine.
