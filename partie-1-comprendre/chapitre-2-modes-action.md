# Les quatre modes d'action de Cowork

Quand Cowork exécute une tâche, il utilise différents modes d'action selon ce que la tâche requiert. Comprendre ces modes vous aide à formuler vos instructions de façon plus efficace — et à savoir ce qui est possible.

---

## Mode 1 — Génération de contenu

**Ce que c'est :** Claude rédige, résume, structure, traduit, reformule. Tout ce que le chat fait déjà, mais avec le contexte permanent du projet.

**Exemples :**
- Rédiger un rapport basé sur des données que vous lui fournissez
- Résumer un document PDF uploadé dans le projet
- Générer 10 variantes d'un objet d'email

**Quand l'utiliser :** Toujours — c'est le mode de base. Les autres modes viennent en complément.

---

## Mode 2 — Connecteurs MCP

**Ce que c'est :** Claude utilise des connexions directes à vos services (Slack, Google Drive, Notion, HubSpot, etc.) pour lire des données ou déclencher des actions.

**Exemples :**
- Lire les 20 derniers emails non lus dans Gmail
- Créer une entrée dans votre base de données Airtable
- Rechercher tous les documents Notion avec le tag "À traiter"
- Envoyer un message dans un canal Slack

**Connecteurs disponibles (2026) :** Slack, Notion, Google Drive, Gmail, Google Calendar, HubSpot, Salesforce, Airtable, Jira, Asana, Linear, GitHub, Figma, Snowflake, et 20+ autres.

**Comment les activer :** Dans le panneau latéral de Cowork, section "Connecteurs". Authentification OAuth pour la plupart.

{% hint style="info" %}
Les connecteurs MCP sont la façon la plus fiable d'interagir avec des services externes. Ils sont plus rapides et plus précis que le contrôle bureau. Si un connecteur existe pour votre outil, utilisez-le.
{% endhint %}

---

## Mode 3 — Contrôle bureau (Computer Use)

**Ce que c'est :** Quand aucun connecteur MCP n'existe pour un outil, Cowork prend le contrôle de votre bureau. Il voit l'écran via captures successives, clique, tape, navigue comme un humain.

**Exemples :**
- Remplir un formulaire dans un logiciel propriétaire sans API
- Naviguer dans une interface web non supportée par les connecteurs
- Extraire des données d'un outil legacy sans accès développeur

**Important :** Le contrôle bureau nécessite que votre ordinateur soit allumé et l'écran actif (non verrouillé). C'est plus lent que les connecteurs et plus susceptible d'erreurs si l'interface change.

**Limite de sécurité :** Cowork n'entre pas vos mots de passe, ne valide pas des transactions financières, et n'envoie pas d'emails sans votre confirmation. Ces actions sont réservées à l'humain.

---

## Mode 4 — Accès fichiers locaux

**Ce que c'est :** Cowork lit et écrit directement dans votre dossier de travail sélectionné. Pas besoin d'uploader, pas de copier-coller.

**Exemples :**
- Analyser tous les fichiers CSV dans votre dossier "Rapports/"
- Créer un document Word formaté et le sauvegarder directement
- Lire votre fichier de configuration de projet et en extraire des informations
- Classer des documents dans des sous-dossiers selon des règles définies

**Configuration :** Lors du premier lancement de Cowork, vous sélectionnez un dossier de travail. Tous les fichiers dans ce dossier (et sous-dossiers) sont accessibles à Claude.

---

## Comment les modes se combinent

La puissance de Cowork vient de la combinaison de ces modes dans une seule tâche.

**Exemple — Rapport de veille hebdomadaire :**

1. Connecteur Gmail → lecture des emails marqués "veille" de la semaine (Mode 2)
2. Connecteur Slack → récupération des mentions importantes dans #veille (Mode 2)
3. Accès fichiers → lecture du template de rapport dans votre dossier (Mode 4)
4. Génération → rédaction du rapport structuré avec les informations collectées (Mode 1)
5. Accès fichiers → sauvegarde du rapport dans Google Drive via connecteur (Mode 2)

Cinq actions, zéro intervention humaine, résultat en quelques minutes.
