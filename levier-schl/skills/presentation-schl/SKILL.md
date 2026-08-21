---
name: presentation-schl
description: Génère une présentation de dossier de financement SCHL (construction assurée ou long terme) au format PowerPoint, dans le style Levier, à partir des documents fournis pour un projet (rapport d'évaluation, plans, registre des loyers, informations financières, certificat de constitution, etc.). Utiliser quand l'utilisateur demande une "présentation SCHL", un "dossier SCHL", ou fournit un lot de documents sur un projet immobilier en construction/acquisition/refinancement et veut un support de présentation pour le prêteur ou la SCHL.
---

# Génération de présentation SCHL — style Levier

Construit une présentation PowerPoint de dossier de financement SCHL calquée sur le style et la structure des présentations Levier existantes.

## Étape 1 — Recherche avant construction

Avant d'écrire une seule diapositive, lis TOUS les documents fournis pour le projet (rapport d'évaluation, plans, registre des loyers, budget de construction, informations financières, certificat de constitution, dispense de cautionnement, attestation d'efficacité énergétique, etc.). Si le volume de documents est important, délègue l'extraction à un agent avec des instructions précises sur les champs à extraire (voir `references/champs-a-extraire.md`), plutôt que de tout lire toi-même.

**Ne jamais calculer ou inventer** : montant de prêt demandé, taux d'intérêt, taux plafond, prime SCHL, équité nette exacte à injecter. Marque ces champs "À COMPLÉTER PAR LE COURTIER" — c'est une décision du courtier Levier, pas de Claude.

## Étape 2 — Déterminer le type de dossier et le menu de diapositives

Le titre et les sections varient selon le type de financement. Consulte `references/menu-diapositives.md` pour le menu complet observé dans les présentations Levier réelles (constructions et financements long terme). Choisis les sections pertinentes selon :
- Le type de prêt (construction assurée vs long terme/acquisition/refinancement/take-out)
- Les documents disponibles (n'invente pas une section "Plans d'étage" si aucun plan n'a été fourni — indique plutôt qu'elle est à ajouter par l'utilisateur)
- La complexité du projet (espace commercial, phases multiples, plusieurs bâtiments, marque/bannière du promoteur, etc.)

Ne construis jamais un nombre fixe de diapositives — adapte le menu à ce que les documents du dossier permettent réellement de remplir.

**Trois diapositives sont obligatoires quel que soit le type de dossier ou le volume de documentation disponible** (consigne Levier — voir `references/menu-diapositives.md`, section « Diapositives obligatoires ») :
1. Organigramme de la structure de détention / structure juridique de l'emprunteur, confirmant qui détient réellement l'actif.
2. Présentation du gestionnaire de l'immeuble.
3. Présentation du constructeur / entrepreneur général — uniquement pour un financement de type construction (ou prêt à l'achèvement, si pertinent).

Si les documents fournis ne permettent pas de remplir une de ces diapositives, construis-la tout de même avec les champs disponibles et marque le reste « À COMPLÉTER PAR LE COURTIER » — ne l'omets jamais faute de documentation.

## Étape 3 — Construire le fichier

Lis le skill `pptx` (dans une autre plugin/skill du système) pour les mécaniques de création PowerPoint (pptxgenjs, gotchas, QA obligatoire). Utilise la palette de marque Levier (voir `references/style-levier.md`) plutôt qu'une palette générique.

Structure recommandée par diapositive : un fond blanc pour le contenu, fond foncé (vert forêt) pour la page titre et la diapositive de clôture/"prochaines étapes". Un accent or/taupe pour les chiffres clés et les kickers de section.

## Étape 4 — QA obligatoire

Suis la procédure de QA du skill `pptx` : validation de fichier (`validate.py`), conversion en images, et inspection visuelle de CHAQUE diapositive (débordement de texte, bullets vides causés par un "\n" combiné à `breakLine: true`, en-têtes de tableau invisibles si un rectangle est ajouté par-dessus après coup — préférer `fill` sur les cellules d'en-tête directement).

## Étape 5 — Livraison

Envoie le fichier .pptx avec SendUserFile. Rappelle explicitement à l'utilisateur les champs laissés à compléter (montant, taux, prime, équité) et, s'il travaille dans Google Slides, indique la marche à suivre (Fichier > Importer des diapositives).
