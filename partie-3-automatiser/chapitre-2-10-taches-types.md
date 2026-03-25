# 10 tâches prêtes à l'emploi

Ces instructions sont prêtes à copier-coller dans Cowork. Adaptez les éléments entre crochets à votre contexte.

---

## 1. Brief matinal quotidien

**Fréquence recommandée :** Tous les jours de semaine à 7h30

```
CONTEXTE : Début de journée. Je veux une vue d'ensemble rapide pour
prioriser ma journée.

TÂCHE :
1. Lis mon calendrier Google des prochaines 24h (connecteur Google Calendar)
2. Vérifie mes emails non lus depuis hier soir 18h (connecteur Gmail)
3. Lis les 5 derniers messages dans Slack #todo et #priorités (connecteur Slack)

LIVRABLE :
Un brief de 1 page maximum :
- Mes 3 engagements du jour (réunions, deadlines)
- Les 3 emails/messages qui demandent une réponse ou action aujourd'hui
- Ma recommandation : quelle est la priorité #1 de la journée ?

Sauvegarde dans ./Outputs/brief-[date].md
```

---

## 2. Rapport de veille hebdomadaire

**Fréquence recommandée :** Tous les lundis à 8h

```
CONTEXTE : Veille hebdomadaire sur [votre secteur ou thématique].

TÂCHE :
1. Cherche les actualités "[mot-clé 1]" et "[mot-clé 2]" des 7 derniers jours
2. Lis les 5-7 articles les plus pertinents
3. Identifie les tendances émergentes et les signaux faibles

LIVRABLE :
Un rapport de veille "Semaine du [date]" avec :
- 5 actualités clés (titre, source, lien, résumé 2 lignes)
- 2-3 tendances à surveiller
- 1 recommandation d'action pour votre activité

Sauvegarde dans ./Outputs/veille-[date-lundi].md
```

---

## 3. Mise à jour CRM automatique

**Fréquence recommandée :** Tous les jours à 18h

```
CONTEXTE : Fin de journée, je veux que mon CRM reflète ce qui s'est
passé aujourd'hui avec mes contacts et prospects.

TÂCHE :
1. Lis mes emails du jour (connecteur Gmail) — filtre : emails envoyés
   ou reçus de domaines professionnels (pas de newsletters)
2. Identifie les échanges avec des prospects ou clients
3. Pour chaque échange identifié, détermine : contact concerné,
   nature de l'échange, action de suivi éventuelle

LIVRABLE :
Un fichier de mise à jour CRM avec pour chaque contact :
- Nom / entreprise
- Résumé de l'échange du jour (2 lignes)
- Action de suivi suggérée avec date

Sauvegarde dans ./Outputs/crm-update-[date].md
```

---

## 4. Analyse concurrentielle mensuelle

**Fréquence recommandée :** Le 1er de chaque mois à 9h

```
CONTEXTE : Suivi mensuel de mes principaux concurrents dans [secteur].

TÂCHE :
1. Pour chaque concurrent dans la liste ci-dessous, cherche :
   - Nouvelles publications LinkedIn du mois écoulé
   - Nouveaux contenus sur leur site (blog, ressources)
   - Mentions presse ou articles à leur sujet
   - Offres d'emploi publiées (signaux de croissance ou changement)

CONCURRENTS : [concurrent 1], [concurrent 2], [concurrent 3]

LIVRABLE :
Un rapport "Veille concurrentielle — [mois]" avec :
- Tableau récapitulatif : concurrent / mouvement notable / signal
- Top 3 mouvements à surveiller
- Implication pour notre stratégie (1 paragraphe)

Sauvegarde dans ./Outputs/veille-concurrents-[mois].md
```

---

## 5. Calendrier de contenu

**Fréquence recommandée :** Chaque lundi à 9h

```
CONTEXTE : Je publie du contenu sur [LinkedIn / blog / newsletter].
Je veux un plan de contenu pour la semaine qui s'appuie sur l'actualité.

TÂCHE :
1. Lis le rapport de veille de la semaine dans ./Outputs/ (cherche le
   fichier veille-[date-lundi].md le plus récent)
2. Identifie 3 angles de contenu exploitables cette semaine
3. Pour chaque angle : formule un titre accrocheur, un hook d'ouverture,
   les 3 idées principales

LIVRABLE :
Un planning contenu semaine avec :
- 3 sujets × (titre + hook + plan en 3 points)
- Pour chaque sujet : format recommandé (post, thread, article)
- Calendrier de publication suggéré (quel jour pour quel contenu)

Sauvegarde dans ./Outputs/planning-contenu-semaine-[date].md
```

---

## 6. Préparation de réunion

**Fréquence recommandée :** À la demande, ou automatique chaque soir

```
CONTEXTE : Je prépare les réunions du lendemain.

TÂCHE :
1. Lis mon Google Calendar de demain (connecteur Google Calendar)
2. Pour chaque réunion externe (avec des personnes hors de mon entreprise) :
   - Cherche les informations publiques sur les participants (LinkedIn)
   - Cherche les actualités récentes de leur entreprise
   - Lis l'historique d'échanges dans Gmail si disponible

LIVRABLE :
Un brief par réunion externe :
- Contexte : qui est là, de quelle entreprise, leur rôle
- Actualité de leur entreprise (2-3 faits récents)
- Objectif de la réunion (d'après l'invitation)
- 2-3 questions pertinentes à poser
- Points de vigilance ou opportunités

Sauvegarde dans ./Outputs/prep-reunions-[date-demain].md
```

---

## 7. Organisation des fichiers téléchargés

**Fréquence recommandée :** Chaque vendredi à 17h

```
CONTEXTE : Mon dossier Téléchargements s'accumule. Je veux trier
automatiquement les fichiers de la semaine.

TÂCHE :
1. Liste les fichiers dans ./Inputs/A-trier/ créés cette semaine
2. Pour chaque fichier, détermine la catégorie selon le nom et le type :
   - Factures / Documents comptables
   - Contrats / Documents légaux
   - Ressources métier (études, rapports)
   - Présentations reçues
   - Autre

LIVRABLE :
Un rapport de tri avec :
- Liste des fichiers par catégorie
- Pour chaque fichier : action recommandée (archiver, traiter, supprimer)
- Fichiers qui nécessitent une attention immédiate (factures à payer, etc.)

Note : Ne pas déplacer les fichiers — uniquement lister et recommander.
Sauvegarde dans ./Outputs/tri-fichiers-[date].md
```

---

## 8. Digest email hebdomadaire

**Fréquence recommandée :** Chaque vendredi à 16h

```
CONTEXTE : Synthèse hebdomadaire de mes emails pour garder le
fil sans tout lire.

TÂCHE :
1. Lis tous mes emails de la semaine (lundi–vendredi) (connecteur Gmail)
2. Exclure : newsletters, notifications automatiques, confirmations de
   commande, emails marketing
3. Classer les emails restants par importance et urgence

LIVRABLE :
Un digest email "Semaine du [date]" :
- Section 1 : Emails en attente de réponse (avec résumé + action)
- Section 2 : Échanges importants conclus cette semaine
- Section 3 : Emails de fond à lire quand j'ai le temps
- Statistiques rapides : X emails reçus, Y traités, Z en attente

Sauvegarde dans ./Outputs/digest-email-semaine-[date].md
```

---

## 9. Rapport d'activité hebdomadaire

**Fréquence recommandée :** Chaque vendredi à 17h30

```
CONTEXTE : Je dois produire un rapport d'activité hebdomadaire pour
mon manager / mes associés.

TÂCHE :
1. Lis mes fichiers créés ou modifiés cette semaine dans ./Outputs/
2. Lis mon calendrier de la semaine (connecteur Google Calendar)
3. Identifie les accomplissements, les décisions prises, les blocages

LIVRABLE :
Un rapport d'activité "Semaine du [date]" :
- Réalisations : ce qui a été accompli cette semaine
- En cours : projets avancés mais pas terminés
- Blocages : ce qui n'a pas avancé et pourquoi
- Semaine prochaine : les 3 priorités

Format : professionnel, concis (1 page max)
Sauvegarde dans ./Outputs/rapport-activite-semaine-[date].md
```

---

## 10. Analyse de performance mensuelle

**Fréquence recommandée :** Le dernier vendredi du mois à 17h

```
CONTEXTE : Bilan mensuel de mes activités et performances.

TÂCHE :
1. Lis tous les rapports hebdomadaires du mois dans ./Outputs/
   (fichiers rapport-activite-semaine-*.md)
2. Lis tous les briefs matinaux du mois (fichiers brief-*.md)
3. Identifie les patterns : qu'est-ce qui avance bien ? Où sont
   les frictions récurrentes ?

LIVRABLE :
Un bilan mensuel "[mois]" :
- Top 3 accomplissements du mois
- Top 3 frictions ou points d'amélioration
- Analyse : où j'ai passé mon temps vs où je devrais le passer
- 3 décisions à prendre pour le mois prochain
- KPIs personnels : réunions, livrables produits, temps de réponse email

Sauvegarde dans ./Outputs/bilan-mensuel-[mois].md
```

---

## Adapter ces templates à votre contexte

Ces 10 tâches couvrent les cas d'usage les plus courants. Pour les adapter :

**Ajoutez vos connecteurs.** Remplacez les sources génériques par vos outils réels : Notion, Airtable, HubSpot, Slack, Linear, etc. Plus les sources sont précises, plus les résultats sont exploitables.

**Précisez vos critères de filtrage.** "Emails importants" est vague. "Emails de [domaine-client.com] et [domaine-partenaire.com]" est actionnable.

**Définissez vos seuils.** "Articles récents" → "Articles des 7 derniers jours". "Fichiers à trier" → "Fichiers de plus de 500 Ko". Les seuils évitent les résultats hors cible.

**Combinez des tâches.** La tâche 2 (veille) peut alimenter la tâche 5 (contenu). Référencez les fichiers Outputs d'une tâche comme source d'une autre — Cowork lira les fichiers dans votre dossier de travail.
