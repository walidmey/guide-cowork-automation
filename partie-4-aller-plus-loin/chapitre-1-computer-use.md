# Computer Use — Cowork contrôle votre ordinateur

La plupart des outils que vous utilisez au quotidien n'ont pas d'API. Votre logiciel de facturation, les portails fournisseurs, les back-offices métier, les sites d'offres d'emploi — pour interagir avec eux automatiquement, il faut contrôler un navigateur comme un humain le ferait.

C'est ce que fait Computer Use dans Cowork.

---

## Ce que Computer Use permet

Cowork peut ouvrir un navigateur Chrome, naviguer vers n'importe quelle URL, cliquer sur des boutons, remplir des formulaires, attendre que des pages chargent, prendre des captures d'écran, et lire le contenu visible à l'écran.

**Concrètement, cela signifie :**

Extraire des données de sites sans API — prix d'un concurrent, offres d'emploi d'un secteur, résultats d'une recherche Google, données sur un portail public.

Interagir avec des interfaces web — soumettre un formulaire, changer un statut dans un outil, télécharger un fichier généré à la demande.

Surveiller des changements — vérifier si un prix a changé, si une page a été mise à jour, si un résultat est apparu.

---

## La différence avec les connecteurs MCP

Les connecteurs MCP sont plus efficaces et plus fiables que Computer Use — quand ils existent. Gmail MCP lit vos emails directement via l'API Google. C'est rapide, structuré, authentifié.

Computer Use est la solution de repli quand il n't y a pas de connecteur. Ou quand l'interface web est la seule façon d'accéder à quelque chose.

| Situation | Utiliser |
|-----------|----------|
| Le service a un connecteur Cowork | Connecteur MCP |
| Pas de connecteur, mais il y a une API publique | Appel API direct |
| Pas d'API, interface web uniquement | Computer Use |
| Authentification complexe (2FA, CAPTCHA) | Vous faites vous-même |

---

## Comment activer Computer Use

Dans les paramètres de votre projet Cowork, activez **"Computer Use"**. Cowork ouvrira alors Chrome dans un environnement contrôlé quand une tâche le nécessite.

{% hint style="warning" %}
**Sécurité :** Ne donnez pas à Cowork l'accès à des sessions authentifiées contenant des données sensibles (banque, admin critique). Pour ces usages, restez sur des connecteurs dédiés ou gérez vous-même.
{% endhint %}

---

## Exemple — Extraire des offres d'emploi concurrentes

```
CONTEXTE : Je surveille les recrutements de mes concurrents pour
comprendre leur stratégie et détecter leurs axes de croissance.

TÂCHE :
1. Pour chaque entreprise de la liste, recherche leurs offres d'emploi
   actuelles sur LinkedIn Jobs et leur site carrières :
   - [Entreprise 1]
   - [Entreprise 2]
   - [Entreprise 3]
2. Pour chaque offre trouvée : note le titre, département, localisation,
   et date de publication
3. Identifie les signaux : recrutent-ils en engineering ? En commercial ?
   Dans une nouvelle géographie ?

LIVRABLE :
Un tableau de bord concurrentiel :
- Tableau : entreprise / rôle / département / localisation / date
- Analyse : quels sont les 3 signaux de croissance les plus significatifs ?
- Implication pour notre stratégie

Sauvegarde dans ./Outputs/recrutements-concurrents-[date].md
```

---

## Exemple — Surveiller un tableau de bord public

```
CONTEXTE : Je surveille chaque semaine un indicateur sur un portail
public (ex : appels d'offres, publications officielles, etc.)

TÂCHE :
1. Navigue vers [URL du portail]
2. Recherche les nouvelles entrées de la semaine avec les critères :
   [vos critères de filtre]
3. Capture les résultats pertinents

LIVRABLE :
- Liste des nouvelles entrées correspondant à mes critères
- Pour chaque entrée : titre, date, lien, résumé
- Alerte si 0 résultats (possible erreur de navigation)

Sauvegarde dans ./Outputs/surveillance-portail-[date].md
```

---

## Ce que Computer Use ne fait pas

**Il ne contourne pas les CAPTCHA.** Si un site présente un test anti-robot, Cowork s'arrête et vous en informe. C'est intentionnel.

**Il ne se connecte pas à vos comptes.** Cowork n'entre pas de mots de passe. Pour les sites qui requièrent une authentification, vous devrez soit utiliser un connecteur dédié, soit pré-authentifier la session vous-même.

**Il n'est pas infaillible sur les sites complexes.** Les interfaces très dynamiques (SPA lourdes, pop-ups multiples, structures non-standard) peuvent poser des problèmes. Dans ces cas, testez l'instruction manuellement avant de planifier la tâche.

---

## Bonnes pratiques

**Testez toujours manuellement d'abord.** Avant de planifier une tâche Computer Use, exécutez-la en mode conversation pour voir comment Cowork navigue et ajustez si nécessaire.

**Soyez précis sur ce que vous cherchez.** "Scrape ce site" est vague. "Navigue vers [URL], clique sur l'onglet 'Offres', liste tous les éléments de la page avec leur titre et leur prix" est actionnable.

**Prévoyez les états d'erreur.** Ajoutez dans votre instruction : "Si la page ne charge pas ou si tu ne trouves pas les éléments attendus, note l'erreur dans le livrable et n'écris pas de données vides."
