# Créer et configurer une tâche récurrente

Les tâches planifiées dans Cowork fonctionnent comme des instructions permanentes avec un déclencheur temporel. Vous écrivez l'instruction une fois — Cowork l'exécute selon le calendrier défini.

---

## Créer une tâche planifiée

{% stepper %}
{% step %}
### Accéder au panneau de tâches planifiées

Dans Cowork, ouvrez votre projet et cliquez sur **"Programmé"** dans le menu latéral (icône horloge). Vous verrez la liste de vos tâches planifiées existantes et un bouton **"Nouvelle tâche"**.
{% endstep %}
{% step %}
### Nommer et décrire la tâche

Donnez un nom explicite à votre tâche. Exemples : "Brief matinal quotidien", "Rapport veille lundi", "Digest emails vendredi 17h".

Rédigez ensuite l'instruction complète de la tâche dans le champ de description. Utilisez la structure CONTEXTE / TÂCHE / SOURCES / LIVRABLE présentée dans la partie précédente.
{% endstep %}
{% step %}
### Définir le calendrier

Choisissez parmi les options disponibles :

- **Quotidien** — à une heure précise, tous les jours ou jours de semaine seulement
- **Hebdomadaire** — un ou plusieurs jours de la semaine, à une heure précise
- **Mensuel** — le Xème jour du mois ou le premier lundi du mois, etc.
- **Toutes les X heures** — pour des suivis fréquents (ex : toutes les 2h entre 9h et 18h)
- **À la demande** — pas de calendrier automatique, vous déclenchez manuellement
{% endstep %}
{% step %}
### Activer et tester

Activez la tâche. Pour vérifier qu'elle fonctionne, utilisez le bouton **"Exécuter maintenant"** — Cowork lancera la tâche immédiatement, indépendamment du calendrier.

Vérifiez le résultat dans votre dossier Outputs et ajustez l'instruction si nécessaire.
{% endstep %}
{% endstepper %}

---

## Contraintes importantes à connaître

**L'ordinateur doit être allumé et l'app ouverte.** Les tâches planifiées ne s'exécutent que si votre ordinateur est en marche et que l'application Claude Desktop est ouverte. Si votre ordinateur est en veille à l'heure prévue, Cowork exécutera la tâche dès que vous rouvrez l'app.

**La tâche s'exécute dans le contexte du projet.** Tout ce qui est dans votre CLAUDE.md est disponible. Inutile de répéter votre profil ou vos préférences dans chaque tâche planifiée.

**Les connecteurs doivent être actifs.** Si votre tâche utilise Gmail, le connecteur Gmail doit être connecté et authentifié. Les tokens OAuth expirent parfois — vérifiez que vos connecteurs sont actifs si une tâche échoue.

---

## Gérer les résultats

**Par défaut,** les résultats d'une tâche planifiée apparaissent dans l'historique de conversation du projet.

**Pour sauvegarder automatiquement,** incluez dans votre instruction : *"Sauvegarde le résultat dans ./Outputs/[nom-fichier]-[date].md"* — Cowork créera le fichier dans votre dossier.

**Pour recevoir une notification,** incluez : *"À la fin, envoie un message dans Slack #[canal] avec un résumé de 2 lignes et un lien vers le fichier créé."*

---

## Exemple d'instruction complète pour une tâche planifiée

```
[Tâche planifiée — Chaque lundi à 8h30]

CONTEXTE : Début de semaine, je veux savoir ce qui s'est passé dans mon secteur
(IA appliquée au RH) pendant le week-end et les priorités de la semaine.

TÂCHE :
1. Recherche les actualités "IA RH" et "HR tech" des 3 derniers jours
2. Lis mon calendrier Google de la semaine (connecteur Google Calendar)
3. Vérifie mes emails non lus du week-end (connecteur Gmail)

LIVRABLE :
Crée un brief matinal "Semaine du [date]" avec :
- Section 1 : 3-4 actus clés de la semaine dans mon secteur
- Section 2 : Mes 3 réunions les plus importantes cette semaine avec contexte
- Section 3 : Les emails du week-end qui nécessitent une action (avec
  action recommandée)
- Section 4 : Ma recommandation pour la priorité #1 de la semaine

Sauvegarde dans ./Outputs/brief-semaine-[date lundi].md
Envoie un message dans Slack #todo : "Brief semaine du [date] prêt ✓"
```

---

## Débugger une tâche qui ne fonctionne pas

Si une tâche planifiée produit un résultat inattendu ou échoue :

1. Vérifiez que les connecteurs utilisés sont actifs (ré-authentifiez si nécessaire)
2. Testez l'instruction manuellement en mode conversation pour identifier la partie problématique
3. Affinez l'instruction — souvent, une ambiguïté dans la formulation suffit à causer des résultats hors cible
4. Vérifiez que le dossier de destination pour les fichiers existe bien
