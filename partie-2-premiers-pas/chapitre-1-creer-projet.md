# Créer un projet et définir le contexte

Un projet Cowork est un espace de travail persistant avec sa propre mémoire, ses propres fichiers accessibles, et ses propres instructions. C'est l'équivalent d'un brief permanent que Claude lit avant chaque tâche dans ce projet.

---

## Créer votre premier projet

{% stepper %}
{% step %}
### Ouvrir Cowork et créer un nouveau projet

Dans la barre latérale gauche, cliquez sur l'icône **+** à côté de "Projets". Donnez un nom explicite à votre projet. Exemples : "Marketing", "Recherche client", "Admin quotidien".

Un projet peut couvrir plusieurs types de tâches liées à un même domaine de votre vie professionnelle.
{% endstep %}
{% step %}
### Sélectionner un dossier de travail

Cowork vous demande de sélectionner un dossier sur votre ordinateur. Ce dossier sera l'espace de fichiers accessible à Claude pour ce projet.

**Recommandations :**
- Créez un dossier dédié (ex : `Claude/[Nom du projet]/`)
- Ne sélectionnez pas votre dossier Documents entier — trop de bruit
- Organisez avec des sous-dossiers : `Inputs/`, `Outputs/`, `Templates/`, `Archive/`
{% endstep %}
{% step %}
### Rédiger le fichier CLAUDE.md

C'est l'étape la plus importante. Le fichier `CLAUDE.md` dans votre dossier de projet est le brief permanent que Claude lit avant chaque tâche. Il contient tout ce dont il a besoin pour travailler efficacement sans vous poser de questions basiques.

Créez un fichier `CLAUDE.md` dans votre dossier de travail et remplissez-le avec le template ci-dessous.
{% endstep %}
{% endstepper %}

---

## Template CLAUDE.md — À adapter à votre contexte

```markdown
# Contexte du projet : [Nom]

## Qui je suis
[Votre nom], [votre rôle] chez [votre entreprise/secteur].
[2-3 phrases sur votre contexte professionnel pertinent pour ce projet]

## Objectifs de ce projet
[Ce que vous voulez accomplir avec Cowork dans ce projet]

## Règles de travail
- Langue : [Français / Anglais / etc.]
- Ton des livrables : [professionnel / décontracté / technique]
- Format préféré des documents : [.md / .docx / .pdf]
- Longueur des résumés : [court (1 page max) / détaillé]

## Outils et services utilisés
- [Liste vos outils : CRM, suite office, communications]
- Dossier des outputs : ./Outputs/
- Dossier des templates : ./Templates/

## Informations sensibles — Ne jamais utiliser
- [Ce que Claude ne doit jamais inclure dans ses livrables]

## Règles absolues
- [Contraintes non-négociables sur ce projet]
```

---

## Exemple concret — CLAUDE.md pour un projet "Marketing"

```markdown
# Contexte du projet : Marketing

## Qui je suis
Directeur Marketing d'une PME B2B en France, 15 personnes, secteur RH tech.
Notre cible : DRH et responsables recrutement de moyennes entreprises (50-500 salariés).

## Objectifs de ce projet
Automatiser la production de contenu, les rapports de performance, et la veille concurrentielle.

## Règles de travail
- Langue : Français uniquement
- Ton : professionnel mais direct, pas de jargon
- Format documents : .docx pour livrables finaux, .md pour drafts
- Résumés : 1 page max, bullet points pour les actions

## Outils et services utilisés
- CRM : HubSpot
- Communication : Slack (#marketing, #veille)
- Documents : Google Drive (dossier "Marketing/")
- Dossier des outputs : ./Outputs/
- Dossier des templates : ./Templates/

## Règles absolues
- Ne jamais envoyer d'email directement — toujours présenter pour validation
- Ne jamais mentionner de données clients nominatives dans les livrables
- Toujours sourcer les informations de veille
```

---

## Activer les connecteurs MCP

Dans le panneau latéral de Cowork, section **"Connecteurs"**, activez les services dont vous avez besoin pour ce projet. Chaque connecteur nécessite une authentification OAuth — vous autorisez Cowork à accéder à votre compte une seule fois.

Commencez par les 3-4 plus utilisés. Vous en ajouterez d'autres au fur et à mesure.

{% hint style="info" %}
**Ordre de priorité pour un usage généraliste :** Gmail ou Outlook → Google Drive ou OneDrive → Slack → Notion ou Airtable
{% endhint %}
