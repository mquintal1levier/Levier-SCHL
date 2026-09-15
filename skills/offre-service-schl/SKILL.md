---
name: offre-service-schl
description: Génère l'offre de service (mandat de courtage) que Levier fait signer à un client emprunteur avant de monter un dossier de financement SCHL, au format PowerPoint dans le style Levier. Utiliser quand l'utilisateur demande une "offre de service", un "mandat de courtage", un "mandat de financement" ou une "entente de service" pour un nouveau client, ou fournit les informations d'un client/projet pour préparer le contrat à faire signer avant de démarrer le dossier SCHL.
---

# Génération d'une offre de service (mandat de courtage) — style Levier

Produit le contrat "Offre de service — Levier" que le client emprunteur signe avec l'Agence Immobilière Levier avant le début du dossier de financement. C'est le tout premier document du processus — il précède la collecte de documentation (étape 1 du guide `dossier-schl`) et n'a rien à voir avec la skill `presentation-schl`, qui produit plus tard le support de présentation pour convaincre un prêteur ou la SCHL.

## Quand l'utiliser

- "Prépare une offre de service pour [client]"
- "J'ai besoin d'un mandat de courtage pour ce dossier"
- Le courtier fournit un nom de client, un projet, et veut le contrat prêt à signer

## Étape 1 — Recueillir les informations nécessaires

Ne jamais inventer les éléments suivants. Si l'un d'eux manque, construis le document quand même mais laisse le champ vide ou marqué à confirmer, et signale-le explicitement à l'utilisateur dans ta réponse (jamais silencieusement) :

- **Client** : raison sociale exacte, adresse complète, nom du représentant autorisé signataire. Si l'entité définitive n'est pas encore constituée, reprendre la mention "(ou toute autre entité à être créée)" sous le nom du client (observée dans tous les exemples Levier).
- **Projet(s)** : adresse, nombre d'unités, ville — un ou plusieurs projets par mandat (voir Étape 2 pour la gestion de mandats à projets multiples).
- **Type(s) de financement visé(s) par phase** — voir Étape 2 pour les combinaisons observées et déterminer la formulation du "Mandat" et de la "Mention générale".
- **Honoraires (%) par volet et modalités de paiement (rétribution)** — **toujours une décision du courtier, jamais une valeur à déduire ou copier d'un dossier précédent.** Les pourcentages observés dans les dossiers Levier varient énormément (de 0,20 % à 0,95 % selon le volet et le rapport de force du dossier) : il n'existe pas de barème par défaut. Demande cette information si elle n'a pas été fournie; si le courtier ne la donne pas, laisse le champ "___ %" dans le document et indique clairement dans ta réponse que la rétribution reste à compléter.
- **Signataire Levier** : par défaut Tommy Archambault, Président-Fondateur, tarchambault@levier.ca, 514.814.8771 (voir tous les exemples). Confirme si un autre courtier Levier doit signer le mandat.

## Étape 2 — Déterminer la structure du mandat

Consulte `references/champs-variables.md` pour :
- Les combinaisons de phases de financement observées (construction → long terme SCHL; conventionnel/bridge → long terme SCHL; conventionnel seul) et la formulation correspondante du "Mandat" (page titre) et de la "Mention générale".
- La gestion d'un mandat à **projets multiples** (ex. repositionnement + acquisition dans une même offre de service) : chaque projet reçoit sa propre diapositive "Objectifs visés" et sa propre diapositive "Rétribution", clairement libellées par le nom du projet, alors que la page titre, la "Définition du mandat" et les "Signatures" restent uniques pour l'ensemble du mandat.
- Le texte fixe exact à réutiliser verbatim (13 points de la "Définition du mandat", les deux variantes de la "Mention générale", le gabarit de "Signatures") : `references/gabarit-texte-fixe.md`. Ce texte est standardisé chez Levier et ne doit **pas** être reformulé ou résumé.

## Étape 3 — Construire le fichier

Lis le skill `pptx` (autre plugin/skill du système) pour les mécaniques de création PowerPoint (pptxgenjs, gotchas, QA obligatoire). Utilise la palette et la mise en page propres à l'offre de service (voir `references/style-levier-mandat.md`) — distincte de la palette utilisée par `presentation-schl` pour les présentations de dossier destinées au prêteur/SCHL.

Structure des diapositives, dans cet ordre :
1. Page titre (fond bicolore : bandeau gauche foncé avec le titre du document et les coordonnées du client; bandeau droit clair avec l'entente de service, le mandat et le/les projet(s))
2. Définition du mandat (texte fixe, 13 points — voir `references/gabarit-texte-fixe.md`)
3. Objectifs visés (une diapositive par projet si mandat à projets multiples)
4. Mention générale (texte fixe avec variante selon le type de financement de la phase 1 — voir `references/gabarit-texte-fixe.md`)
5. Rétribution (une diapositive par projet si mandat à projets multiples)
6. Signatures (gabarit fixe — voir `references/gabarit-texte-fixe.md`)

Ne construis jamais un mandat à projets multiples en fusionnant les "Objectifs visés" ou les "Rétribution" de deux projets sur une même diapositive — les exemples Levier les séparent toujours.

## Étape 4 — QA obligatoire

Suis la procédure de QA du skill `pptx` : validation de fichier (`validate.py`), conversion en images, et inspection visuelle de CHAQUE diapositive. Vérifie en particulier :
- Que la "Définition du mandat" et le gabarit de "Signatures" correspondent mot pour mot au texte fixe de `references/gabarit-texte-fixe.md`.
- Qu'aucun pourcentage d'honoraires n'a été inventé ou copié d'un exemple — soit une valeur fournie par le courtier, soit un champ clairement laissé à compléter.
- Que la "Mention générale" utilise la bonne variante selon le type de financement de la phase 1 (construction vs conventionnel/bridge).

## Étape 5 — Livraison

Envoie le fichier .pptx avec SendUserFile. Si un ou plusieurs champs ont été laissés à compléter (rétribution, dates, représentant du client, etc.), rappelle-les explicitement dans ta réponse plutôt que de laisser l'utilisateur les découvrir en ouvrant le fichier.
