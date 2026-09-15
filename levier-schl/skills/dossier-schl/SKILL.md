---
name: dossier-schl
description: Guide du processus de mise en place d'un financement assuré SCHL et des normes documentaires de Levier. Utiliser quand l'utilisateur pose une question sur les étapes d'un dossier SCHL (collecte de documentation, scénarios de financement, line-up, déboursement), sur les seuils et exigences de la SCHL (valeur nette de 25%, registre des loyers, proforma revenus et dépenses, espace commercial, APH Select, bilan personnel, cautionnement corporatif, parc immobilier, volet take-out, volet construction, budget de construction), ou pour valider qu'un dossier respecte les normes Levier/SCHL avant soumission.
---

# Guide du processus et des normes SCHL — Levier

Ce guide couvre la méthode Levier pour la mise en place d'un financement construction assurée ou long terme SCHL. Utilise ce contenu pour répondre aux questions du courtier sur le processus, les seuils, et pour auditer un dossier avant soumission à la SCHL.

## Quand l'utiliser

- Question sur une étape du processus ("où en est ce dossier", "que faut-il pour la soumission", "combien de temps ça prend")
- Question sur une norme ou un seuil SCHL (valeur nette, registre des loyers, proforma, bilan personnel, etc.)
- Demande de valider un dossier avant soumission ("est-ce que ce dossier est prêt", "manque-t-il quelque chose")

Charge `references/normes-schl.md` pour le détail complet des normes avant de répondre — ne réponds pas de mémoire sur les seuils précis.

## Les 16 étapes de la mise en place d'un financement (résumé)

1. Collecte de la documentation (liste transmise par Levier; l'analyse ne peut débuter qu'à 90% de la documentation requise)
2. Présentation des scénarios de financement par le courtier
3. Sélection du prêteur + émission d'une lettre d'intention
4. Soumission du dossier à la SCHL (1 à 4 semaines selon la qualité de l'information)
5. Paiement des droits de demande à la SCHL (dans les 72h suivant la facture)
6. Mise en line-up (2 à 12 semaines selon le volume de dossiers à la SCHL)
7. Prise en charge par un souscripteur SCHL, négociation, entente sur montant/conditions
8. Livraison du certificat d'assurance (COI)
9. Mise à jour de la documentation pour le prêteur (souvent les bilans personnels et preuves d'actifs/passifs)
10. Transmission du dossier au crédit (prêteur)
11. Émission d'une lettre d'engagement
12. Analyse des conditions préalables (CP) — les éléments inscrits à la lettre d'engagement à remplir avant déboursement
13. Transmission au consultant en assurance
14. Transmission au notaire
15. Révision juridique
16. Déboursement du prêt

## Utilisation avec les autres skills

- Avant même l'étape 1 (collecte de documentation), pour préparer le contrat que le client emprunteur doit signer avec Levier (l'offre de service / mandat de courtage), utilise la skill `offre-service-schl`.
- Pour construire une présentation de dossier à partir des documents d'un projet, utilise la skill `presentation-schl`.
- Pour remplir un gabarit de suivi (CP, bilan personnel, budget de construction, états des résultats, liste des intervenants), utilise la skill `gabarits-schl`.

## Checklist rapide avant soumission

Avant de dire qu'un dossier est prêt, vérifie (voir `references/normes-schl.md` pour le détail de chaque point) :

- [ ] Registre des loyers au format Excel officiel SCHL, avec colonnes Marché/Abordable renseignées et typologie SCHL respectée
- [ ] Proforma revenus et dépenses fourni (budget d'opération 3 ans si immeuble existant / projeté si construction ou take-out)
- [ ] Si espace commercial : revenus/dépenses distincts + détails de bail
- [ ] Si stratégie APH Select : attestation d'efficacité énergétique ou d'accessibilité signée par le professionnel, avec le nom du prêteur inscrit
- [ ] Valeur nette de tous les actionnaires derrière l'emprunteur ≥ 25% du montant de prêt demandé, liquidités démontrées (surtout en construction)
- [ ] Bilans personnels avec preuves d'actifs (relevés 3-6 mois) et passifs (dettes hypothécaires) pour chaque caution particulière
- [ ] Rapports d'impôts complets (fédéral + provincial, année courante) pour chaque caution particulière
- [ ] CV de chaque caution particulière (parcours en immobilier multirésidentiel; 5 ans d'expérience en gestion locative sinon gestionnaire tiers requis)
- [ ] 3 ans d'états financiers pour chaque entité corporative caution (ou années disponibles si moins)
- [ ] Parc immobilier rempli pour tout immeuble de 3 logements et plus détenu par une caution
- [ ] (Construction) Dispense de cautionnement d'exécution + liste des principaux sous-traitants, si applicable
- [ ] (Construction) Budget de construction incluant terrain, soft costs, hard costs, contingence, autocotisation, frais de développement, frais financiers — sans les frais/primes SCHL ni frais de démolition/décontamination
- [ ] (Take-out) Attestation de fin des travaux à 100% signée par un professionnel + confirmation du budget de construction par un CPA indépendant de l'organigramme

## Après l'émission du COI — deux checklists distinctes, volontairement séparées

Recevoir l'attestation d'assurance (COI) n'est pas la fin du dossier. Levier sépare volontairement le suivi post-COI en deux outils distincts plutôt qu'une seule grosse checklist (retour client : une liste unique trop longue est décourageante) :

**1. Les CP — conditions préalables au premier déboursé.** C'est la checklist opérationnelle que le courtier utilise concrètement entre la lettre d'engagement et le déboursement — voir la skill `gabarits-schl` et `gabarits-schl/references/structure-gabarits.md` pour le détail exact par type de dossier (acquisition, immeuble existant/refinancement, construction, take-out) : nouvelle étude environnementale, certificat de localisation, preuve de mise de fonds, assurance habitation, rapport du consultant en coûts, attestation de fin de travaux, mise à jour de documentation des cautions si le délai SCHL dépasse 90 jours, etc.

**2. Les obligations légales inscrites au COI lui-même.** Le COI impose en plus des obligations qui continuent pendant toute la durée du prêt, et parfois pendant 10 à 20 ans pour les dossiers APH Select (paiement de la prime dans les délais, échéancier des avances, attestations annuelles d'abordabilité/efficacité énergétique, etc.) — voir `references/structure-attestation-assurance.md` pour le détail complet par type de prêt avant de dire qu'un dossier est « clos ». Ces obligations recoupent souvent les CP dans la pratique (ex. la lettre de confirmation EES demandée en CP construction est aussi une clause du COI) mais certaines sont purement contractuelles et ne figurent pas dans les gabarits CP actuels (ex. le seuil de revenu brut réel pour un prêt à l'achèvement, ou la clause de réduction automatique si la dernière avance est manquée) — à surveiller même si elles ne sont pas encore sur une checklist Levier dédiée.
