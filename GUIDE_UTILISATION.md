# Guide d'utilisation — Analyseur RSF / SLGP

Outil d'aide à la correction du reporting trimestriel RSF : il analyse votre fichier Excel,
repère toutes les incohérences, vous guide pour les corriger (à l'unité ou **en lot**),
et réexporte un fichier **corrigé et intact**, prêt à partager.

---

## 🔒 3 garanties à retenir

1. **Rien n'est installé** — l'outil est une simple page qui s'ouvre dans votre navigateur (Chrome, Edge…).
2. **Vos données restent chez vous** — le fichier est traité **localement** dans le navigateur, rien n'est envoyé sur un serveur.
3. **Votre fichier d'origine n'est jamais modifié** — l'outil exporte une **copie corrigée**. Et tout est annulable (Ctrl+Z).

---

## ⚡ Démarrage rapide (5 étapes)

1. **Ouvrez** le fichier de l'outil dans votre navigateur.
2. **Glissez-déposez** votre fichier Excel RSF (ou cliquez pour le sélectionner).
3. Cliquez sur **« Commencer la revue → »**.
4. Parcourez les onglets, **corrigez** les erreurs (à l'unité ou en lot), ajoutez des commentaires si besoin.
5. Cliquez sur **« 📥 Exporter »** → vous obtenez `…_corrige.xlsx`.

Le reste de ce guide détaille chaque étape.

---

## 1. Importer le fichier

- Zone **« Glissez votre fichier Excel RSF ici »** → glissez le `.xlsx`, ou cliquez pour le choisir.
- L'outil détecte automatiquement les feuilles : **Current QReport, MissingData, CompQoQ, Otherchecks, Compliance Checks**, ainsi que les trimestres historiques (ex. `4Q25`, `3Q25`…).
- L'analyse prend quelques secondes. Un badge ✓ s'affiche pour chaque feuille reconnue.
- Pour changer de fichier ensuite : bouton **« Changer de fichier »** en haut.

> ℹ️ L'outil lit les **colonnes telles qu'elles sont** dans votre fichier (il s'adapte à l'ajout/retrait/réordonnancement des colonnes). Si la structure n'est pas reconnue, signalez-le.

---

## 2. Le tableau de bord

Juste après l'analyse, une vue d'ensemble s'affiche :

- **Total / Conformes / Non-conformes** et le **ratio de non-conformité**.
- **Répartition par type** d'erreur (MissingData, CompQoQ, OtherChecks).
- **Comparaison** avec le trimestre précédent et le résumé **Compliance** (brèches éventuelles).

Cliquez **« Commencer la revue → »** pour passer au détail.

---

## 3. Les onglets

| Onglet | Contenu |
|---|---|
| **Current QReport** | Toutes les facilités, **éditables** cellule par cellule. |
| **MissingData** | Données manquantes détectées. |
| **CompQoQ** | Incohérences vs le **trimestre précédent**. |
| **OtherChecks** | Contrôles de cohérence internes. |
| **⏱️ Jours retard** | Nombre de jours d'impayé — **calculé automatiquement**. |
| **🛡️ Compliance** | Contrôles de conformité (brèches). |
| **📅 Historique trimestriel** | Trimestres passés, en **lecture seule** (comparaison visuelle). |

Le panneau de droite **« Problèmes & Commentaires »** liste, pour chaque ligne, les erreurs à traiter.

---

## 4. Corriger une erreur (le b.a.-ba)

Pour une erreur donnée, vous avez plusieurs possibilités :

- **Modifier la valeur directement** dans la cellule (onglet Current QReport). Une fenêtre vous propose ensuite d'ajouter un commentaire et/ou d'appliquer la même correction à d'autres lignes.
- **« ✓ Rétablir »** : remet la valeur du trimestre précédent (affichée dans la carte) en un clic.
- **Commentaire** : zone « Commentaire… » + **« 📋 Appliquer »** pour justifier la correction (et la propager à d'autres facilités si besoin).
- **« ⊘ Ignorer »** : marque l'alerte comme non pertinente (faux positif). **« ⊘ Ignorer tout »** fait de même sur toutes les facilités présentant la même alerte.

> Une erreur traitée (corrigée, commentée ou ignorée) **disparaît** de la liste, et la barre de progression avance.

---

## 5. Gagner du temps : les actions en lot et automatiques

C'est ici que l'outil fait la différence avec Excel.

- **Corriger en lot (OtherChecks)** — bouton **« ✏️ Corriger en lot (N) »** : sélectionnez d'un coup plusieurs facilités ayant la **même** erreur, choisissez une colonne + une valeur et/ou un commentaire, et appliquez **en une fois**.
- **Rétablir les similaires (CompQoQ)** — bouton **« ✓ Rétablir les N similaires »** : remet la valeur du trimestre précédent sur toutes les facilités concernées d'un coup.
- **Jours d'impayé (automatique)** — onglet **Jours retard** : l'outil calcule le nombre de jours entre la **date du 1er impayé** et la **date d'arrêté**, et détecte les jours manquants quand la facilité est toujours en arriéré. **« ✓ Corriger »** (une ligne) ou **« ✓ Corriger les N »** (toutes).
- **Appliquer un commentaire à plusieurs** — depuis n'importe quelle carte, **« 📋 Appliquer »** ouvre une liste pour cocher les facilités qui reçoivent le même commentaire.

---

## 6. Comparer avec un autre trimestre

Par défaut, les comparaisons se font avec le **trimestre précédent (N‑1)**. Vous pouvez choisir un autre trimestre de référence :

- **Globalement** : menu **« Comparer avec : »** en haut (visible sur Current QReport, MissingData, CompQoQ, OtherChecks, Historique).
- **Ligne par ligne** : dans une carte CompQoQ/MissingData, un petit menu **« Comparer avec : »** permet de changer le trimestre **juste pour cette facilité**, sans toucher au réglage global. Idéal pour une erreur qui remonte à plus de deux trimestres.

---

## 7. OtherChecks : « Voir / corriger la ligne »

Sur une alerte OtherChecks, le bouton **« 📋 Voir / corriger la ligne »** ouvre la **facilité complète du trimestre en cours**, modifiable directement. Dans cette fenêtre :

- chaque champ peut être corrigé ;
- la **valeur de chaque trimestre passé** est affichée à côté (cliquez dessus pour la réutiliser) ;
- le menu **« Trimestre de référence : »** change le trimestre comparé pour cette ligne ;
- un champ **commentaire** permet de justifier ;
- **« 💾 Enregistrer »** applique la correction et fait disparaître l'alerte.

---

## 8. Filtres, tri et pagination

- **Filtrer par colonne** : sous les onglets MissingData / CompQoQ / OtherChecks, pour se concentrer sur un seul contrôle. (Chaque onglet garde son propre filtre.)
- **Rang :** filtre multi-rangs (en haut à droite).
- **Pagination** : en bas du tableau (50 / 100 / 200 / tout afficher).
- **Navigateur de problèmes** : flèches **↑ Précédent / Suivant ↓** (ou **Alt+↑ / Alt+↓**) pour sauter de problème en problème.

---

## 9. Annuler / Refaire

- **Annuler** : bouton **↶** ou **Ctrl+Z**.
- **Refaire** : bouton **↷** ou **Ctrl+Y**.

Toutes les corrections (y compris les actions en lot) sont réversibles.

---

## 10. Sauvegarde automatique

- Votre travail est **sauvegardé automatiquement** dans le navigateur.
- Si vous fermez puis rouvrez le même fichier, une bannière **« Session précédente détectée »** propose **« Restaurer »** ou **« Ignorer »**.

> La session est liée à votre navigateur/poste. Pour transmettre votre travail, **exportez** le fichier.

---

## 11. Exporter le rapport

1. Cliquez **« 📥 Exporter »**.
2. Un **aperçu** récapitule : corrections, commentaires, ignorés, restants.
3. Confirmez → l'outil génère **`<nom_du_fichier>_corrige.xlsx`**.

Le fichier exporté contient :
- **Onglet « Current QReport »** : vos corrections appliquées, **formats et formules préservés** ;
- **Onglet « Commentaire »** : tous vos commentaires regroupés (corrections / OtherChecks) avec les lignes concernées.

> Le fichier ressort **intact** et peut être partagé directement avec les autres équipes IFC.

---

## 💡 Astuces

- Commencez par les **actions en lot** (Corriger en lot, Rétablir les similaires, Corriger les N) : vous liquidez le gros du volume en quelques clics.
- Utilisez **« Ignorer tout »** pour les faux positifs récurrents.
- Suivez la **barre de progression** (« X / Y problèmes traités ») pour savoir ce qu'il reste.
- En cas de doute, **Ctrl+Z** : rien n'est irréversible avant l'export.

---

## ❓ FAQ / dépannage

**Mes données sont-elles en sécurité ?**
Oui — tout est traité dans votre navigateur, rien n'est envoyé sur Internet.

**L'outil peut-il abîmer mon fichier ?**
Non — il n'écrit jamais dans l'original ; il exporte une copie corrigée.

**« Feuille Current QReport introuvable » ou colonnes mal lues ?**
La structure du fichier n'est probablement pas reconnue. Vérifiez le nom des feuilles, et signalez le format pour qu'il soit pris en charge.

**Une date saisie ne s'affiche pas correctement ?**
Saisissez les dates au format `jj/mm/aaaa` (ex. `31/03/2025`) — l'outil les convertit correctement à l'export.

**J'ai fermé l'onglet sans exporter — ai-je tout perdu ?**
Non : rouvrez le même fichier et cliquez **« Restaurer »** sur la bannière de session.
