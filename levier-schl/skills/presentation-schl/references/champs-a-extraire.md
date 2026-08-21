# Champs à extraire des documents d'un dossier — checklist pour agent d'extraction

Quand tu délègues l'extraction à un agent (recommandé si plus de 3-4 documents), donne-lui cette liste de champs à repérer, organisée par section de présentation. Demande-lui d'indiquer explicitement "Non trouvé dans les documents fournis" plutôt que d'inventer une valeur.

## Identification générale
- Adresse complète, désignation cadastrale (lot), ville
- Société emprunteuse (nom, NEQ, date de constitution)
- Client du dossier (prêteur ou firme mandataire), numéro de dossier d'évaluation

## Résumé de la demande
- Type de prêt, produit SCHL (si mentionné)
- Nombre d'unités/bâtiments, nombre d'étages
- Dates clés : début travaux, mise en location, occupation, fin des travaux, stabilisation
- Terrain : JVM, prix payé, hypothèque existante

## Typologie et registre des loyers
- Table par unité : étage, type (pièces québécoises), superficie, loyer
- Composition (nombre par typologie)
- Stationnement (nombre de cases, tarif si applicable)
- Inclusions au loyer (par le registre SCHL)
- Espaces communs

## Implantation et détails techniques
- Firme et date du plan d'implantation, zone/zonage
- Superficies par étage et superficie brute totale
- Structure, fondations, murs extérieurs, toit, fenêtres, chauffage, plomberie

## Localisation
- Description du secteur, nuisances relevées
- Statistiques démographiques/marché locatif (population, taux d'inoccupation SCHL, évolution des loyers)
- Accès (autoroutes, transport en commun)

## Terrain
- Prix payé (acte notarié) et date
- Prix selon promesse d'achat, si différent
- JVM (rapport d'évaluation) — méthode du coût / du revenu / de comparaison / conclusion
- Hypothèque actuelle, zonage, historique de vente antérieure

## Revenus et dépenses d'exploitation
- RBP, réserve d'inoccupation, RBE, dépenses d'exploitation (détail par poste), RNE
- TGA appliqué (si mentionné)

## Efficacité énergétique
- Niveau/cote atteint, % de réduction vs référence CNB
- Prêteur agréé désigné sur l'attestation

## Promoteur / emprunteur
- Nom de la société, NEQ, date de constitution
- Actionnaire(s)/administrateur(s) et % de détention
- Historique et réalisations (nombre de logements construits, coût/budget cumulé, prêt cumulé — souvent dans le formulaire de dispense de cautionnement)

## Gestionnaire de l'immeuble (diapositive obligatoire — tous types de dossiers, voir menu-diapositives.md)
- Nom du gestionnaire (interne à l'emprunteur, ou firme de gestion tierce) et ses coordonnées
- Années d'expérience en gestion immobilière multirésidentielle, type/taille des immeubles gérés
- Immeubles sous gestion (adresse, nombre d'unités) — si mentionnés dans un CV ou une liste de références, pour démontrer la capacité de gestion
- Si aucune information sur le gestionnaire n'est fournie dans les documents : construire la diapositive quand même avec les champs marqués « À COMPLÉTER PAR LE COURTIER », ne jamais l'omettre

## Constructeur / entrepreneur général (diapositive obligatoire pour tout financement construction, voir menu-diapositives.md)
- Nom de l'entrepreneur général (ou du constructeur), licence RBQ si mentionnée
- Type de contrat envisagé (prix fixe / gestion de construction-directeur des travaux)
- Réalisations antérieures (nombre de projets, unités livrées, années d'expérience) — souvent dans le formulaire de dispense de cautionnement ou la liste des sous-traitants
- Si aucune information sur le constructeur n'est fournie : construire la diapositive quand même avec les champs marqués « À COMPLÉTER PAR LE COURTIER », ne jamais l'omettre

## Structure d'emprunt et force financière
- Organigramme des entités/cautions et % de participation
- Type de caution (corporative/personnelle) par entité
- Bilan de l'emprunteur (actif total, passif total, capitaux propres, bénéfice net)
- Parc immobilier des cautions (adresse, % de détention, revenu locatif, dépenses, RNE, valeur, dettes)

## Dépenses payées à ce jour
- Table budget vs payé à ce jour, par poste (construction, frais SCHL, terrain, frais municipaux, professionnels, autres)

## MLI Select — si le dossier vise une prime préférentielle
- Niveau visé/atteint par volet : accessibilité (1 ou 2), efficacité énergétique (1, 2 ou 3 — préciser si évalué selon la nouvelle méthodologie CNÉB/CNB 2020 "% au-dessus du palier 1" ou l'ancienne "% en dessous du code 2017"), résultats sociaux/abordabilité (RMML, % d'abordabilité)
- Prêteur agréé désigné inscrit sur les attestations
- Points cumulés (si mentionnés dans les documents) et palier de prime résultant — ne pas calculer si absent, indiquer "Non trouvé dans les documents fournis"

## Portefeuille et exposition du groupe
- Portefeuille immobilier déjà détenu par l'emprunteur/les cautions (propriétés, RPV/CCD par propriété, si fournis dans un registre ou une analyse sommaire de portefeuille)
- Exposition SCHL cumulée du groupe, si mentionnée — signaler si le dossier approche le seuil "grand emprunteur"
- Pour un projet québécois composé de plusieurs bâtiments 3-4plex jumelés sur un même terrain/lot : noter si un regroupement en un seul dossier multirésidentiel est mentionné par le prêteur

## Structure de financement anticipée (construction / prêt à l'achèvement)
- Type de contrat de construction envisagé (entrepreneur général à prix fixe, ou gestion de construction/directeur des travaux) et budget plafonné correspondant — ces éléments deviennent des clauses fermes de l'attestation d'assurance (COI), voir `dossier-schl/references/structure-attestation-assurance.md`
- Échéancier d'avances envisagé (dates de première/dernière avance) si déjà connu
- Pour un prêt à l'achèvement : le revenu brut réel (RBR) visé/atteint à la stabilisation — le COI imposera un seuil minimal avant le versement de l'avance unique
- Période d'abordabilité visée si APH Select (10 ou 20 ans selon les dossiers observés) — s'assurer que la présentation ne sous-entend pas une durée d'engagement plus courte que celle qui sera réellement inscrite au COI

## Champs à NE JAMAIS calculer
- Montant de prêt demandé, taux d'intérêt, taux plafond, prime SCHL, équité nette exacte à injecter — toujours "À COMPLÉTER PAR LE COURTIER".
- Ne jamais calculer une retenue pour réalisation du revenu locatif (RRRL) — signaler seulement le risque si RPV > 95% et CCD sous le seuil applicable (voir normes-schl.md), le calcul exact reste au courtier.
