---
name: gabarits-schl
description: Aide à remplir les gabarits de suivi Levier pour un dossier de financement SCHL — conditions préalables (CP) au déboursé, bilan personnel, budget de construction, états des résultats sur 3 ans, liste des intervenants pour la dispense de cautionnement, registre des loyers et parc immobilier. Utiliser quand l'utilisateur fournit un gabarit Levier vide (ou partiellement rempli) avec des documents source, et demande de le remplir, le compléter ou le mettre à jour.
---

# Remplissage des gabarits de suivi Levier

Remplit les gabarits Excel standards de Levier à partir des documents sources d'un dossier (rapports d'évaluation, informations financières, factures, contrats, etc.). Consulte `references/structure-gabarits.md` pour la structure exacte (feuilles, colonnes) de chaque gabarit avant de le modifier — ne devine pas la structure.

## Principes

- Lis d'abord le skill `xlsx` pour les mécaniques d'édition de fichiers Excel (préserver le formatage, formules, validations de données existantes).
- Ne jamais supprimer ou renommer les feuilles, en-têtes ou validations de données existantes dans un gabarit Levier — ce sont des fichiers normés SCHL/Levier.
- Chaque valeur ajoutée dans un bilan personnel ou un parc immobilier doit être traçable à une pièce justificative fournie — si aucune pièce n'appuie une valeur, laisse la cellule vide plutôt que d'inventer un chiffre, et signale-le à l'utilisateur.
- Ne jamais remplir le montant de prêt, le taux, la prime SCHL ou l'équité nette finale — ce sont des décisions du courtier.

## Identifier le bon gabarit

| Situation | Gabarit |
|---|---|
| Suivi des conditions à remplir avant déboursement (acquisition) | `Conditions préalables_acquisition.xlsx` |
| Suivi des conditions à remplir avant déboursement (immeuble existant / refinancement) | `Conditions préalables_Immeuble existant.xlsx` |
| Suivi de dossier de construction (grille de gestion + conditions préalables) | `Levier_CP_CONSTRUCTION.xlsx` |
| Suivi de dossier take-out | `Levier_CP_TAKEOUT.xlsx` |
| Liste des documents requis (acquisition / construction / refinancement / take-out) | `Levier_Acquisition.xlsx`, `Levier_Construction.xlsx`, `Levier_Refinancement.xlsx`, `Levier_Takeout.xlsx` |
| Bilan personnel d'une caution particulière | `Levier_Bilan personnel_V2026.xlsx` |
| Budget de construction d'un projet | `Levier_Budget de construction.xlsx` |
| Historique financier d'un immeuble existant (3 ans) | `Levier_États des résultats_3 ans.xlsx` |
| Historique et sous-traitants pour dispense de cautionnement d'exécution | `Levier_Liste des intervenants_cautionnement.xlsx` |

Si l'utilisateur ne précise pas lequel utiliser, demande-lui de préciser le type de dossier (acquisition, construction, refinancement, take-out) et ce qu'il souhaite documenter (documents requis, conditions préalables, force financière, budget, historique financier, sous-traitants).

## Après remplissage

Vérifie systématiquement (voir aussi la skill `dossier-schl` pour les normes complètes) :
- Bilan personnel : chaque ligne d'actif/passif a-t-elle une pièce justificative numérotée?
- Budget de construction : les frais et primes SCHL sont-ils exclus des soft costs? Les frais de démolition/décontamination sont-ils exclus des hard costs?
- Parc immobilier : le % de détention est-il inscrit pour chaque propriété?
- États des résultats : les 3 années sont-elles remplies (ou les années disponibles, si moins de 3 ans)?

Livre le fichier avec SendUserFile et signale explicitement toute case laissée vide par manque de documentation source.
