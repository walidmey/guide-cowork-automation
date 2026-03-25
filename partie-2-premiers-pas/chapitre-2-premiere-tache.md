# Votre première tâche déléguée

La meilleure façon d'apprendre Cowork est de lui donner une vraie tâche — pas un exemple jouet, mais quelque chose que vous faites réellement et qui prend du temps.

Ce chapitre vous guide à travers une première tâche concrète, avec les patterns d'instruction qui fonctionnent.

---

## La structure d'une bonne instruction Cowork

Une instruction Cowork efficace a toujours quatre composants :

```
[CONTEXTE] Ce que Claude doit savoir sur la situation
[TÂCHE] Ce qu'il doit faire exactement
[SOURCES] Où il doit chercher les informations
[LIVRABLE] Ce qu'il doit produire en sortie
```

Plus l'instruction est précise sur ces quatre points, moins Claude aura besoin de vous poser des questions.

---

## Exemple 1 — Résumé d'emails de la semaine

```
CONTEXTE : Tu es dans mon projet Marketing. Je reviens d'une semaine de congés.

TÂCHE : Fais un résumé des emails importants que j'ai reçus cette semaine
et que je n'ai pas encore lus.

SOURCES : Gmail, boîte principale, période du [date de départ] à aujourd'hui.
Ignore les newsletters, notifications automatiques, et emails promotionnels.
Priorise : emails de clients, emails de collègues directs, emails avec mon
prénom dans l'objet.

LIVRABLE : Un document structuré avec :
1. Les 3-5 sujets les plus urgents à traiter (avec action recommandée)
2. Un résumé de 2-3 lignes par email important
3. Les emails qui peuvent attendre ou être archivés
Sauvegarde le document dans ./Outputs/retour-conges-[date].md
```

---

## Exemple 2 — Synthèse d'une veille thématique

```
CONTEXTE : Je fais une veille hebdomadaire sur l'IA en RH.

TÂCHE : Cherche les actualités importantes sur ce sujet des 7 derniers jours.

SOURCES :
- Recherches web sur "IA RH", "intelligence artificielle recrutement",
  "automatisation RH 2026"
- Lis les articles complets des 5 résultats les plus pertinents
- Inclus uniquement des sources crédibles (journaux, études, sites spécialisés)

LIVRABLE : Un rapport de 1 page avec :
- 3-5 faits marquants de la semaine
- Pour chaque fait : source, lien, impact potentiel pour mon activité
- Une phrase d'analyse : qu'est-ce que ça change pour les DRH ?
Sauvegarde dans ./Outputs/veille-ia-rh-semaine-[numéro semaine].md
```

---

## Exemple 3 — Préparation d'une réunion

```
CONTEXTE : J'ai une réunion de vente demain avec [Nom entreprise],
une PME de 200 personnes dans la logistique.

TÂCHE : Prépare un brief de 1 page pour cette réunion.

SOURCES :
- Recherche web sur [Nom entreprise] : actualités récentes, offres d'emploi
  publiées, communiqués de presse
- Lis leur site web, notamment les pages "À propos" et "Carrières"
- Notre CRM HubSpot : historique de contact avec cette entreprise si existant

LIVRABLE : Un brief avec :
- Contexte entreprise (secteur, taille, enjeux actuels identifiés)
- Points de connexion avec notre offre
- 3 questions pertinentes à poser en réunion
- Signaux d'achat potentiels identifiés
Sauvegarde dans ./Outputs/brief-reunion-[nom entreprise]-[date].md
```

---

## Ce qui rend une instruction efficace

**Soyez précis sur les sources.** "Cherche sur internet" est vague. "Cherche sur LinkedIn, Google News, et leur site officiel" est actionnable.

**Définissez le format de sortie.** Claude par défaut produit un texte long. Si vous voulez des bullet points, un tableau, un document Word — précisez-le.

**Donnez des contraintes de temps.** "Les 7 derniers jours", "cette semaine", "depuis le 1er janvier" — sans contrainte temporelle, Claude peut chercher trop loin.

**Indiquez où sauvegarder.** Si vous voulez un fichier dans votre dossier, précisez le chemin. Sans ça, le résultat reste dans la conversation.

---

## Après votre première tâche

Évaluez le résultat sur deux critères :

1. **Pertinence :** Le contenu est-il utile ? Si non, quelle partie de l'instruction était floue ?
2. **Format :** La mise en forme correspond-elle à votre usage ? Sinon, ajoutez les spécifications dans votre CLAUDE.md pour ne pas avoir à les répéter.

Chaque itération améliore la qualité. Après 3-4 tâches, vous saurez exactement comment formuler pour obtenir ce que vous voulez.
