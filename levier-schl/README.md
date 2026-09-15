# Levier SCHL

Méthode Levier pour monter des dossiers de financement assuré SCHL (construction et long terme).

## Skills incluses

- **offre-service-schl** — Génère l'offre de service (mandat de courtage) que le client emprunteur signe avec Levier avant le début du dossier de financement, au format PowerPoint dans le style Levier. Couvre la page titre, la "Définition du mandat" (texte fixe), les "Objectifs visés", la "Mention générale" (deux variantes selon le type de financement de la phase 1) et la "Rétribution" (toujours à confirmer avec le courtier, jamais de pourcentage par défaut), y compris les mandats à projets multiples.
- **dossier-schl** — Guide du processus de mise en place (16 étapes) et des normes documentaires SCHL/Levier (registre des loyers, proforma, valeur nette 25%, bilan personnel, cautionnement, budget de construction, etc.), y compris les obligations de suivi après l'émission de l'attestation d'assurance (COI) par type de prêt — construction, prêt à l'achèvement, acquisition, refinancement. Répond aux questions sur le processus et permet de valider un dossier avant soumission ou après réception du COI.
- **presentation-schl** — Génère une présentation PowerPoint de dossier SCHL dans le style Levier, à partir des documents d'un projet (rapport d'évaluation, plans, registre des loyers, informations financières, etc.). Le menu de diapositives s'adapte au type de dossier et aux documents disponibles.
- **gabarits-schl** — Aide à remplir les gabarits de suivi Levier (conditions préalables, bilan personnel, budget de construction, états des résultats 3 ans, liste des intervenants pour la dispense de cautionnement).

## Principes communs

- Ne jamais estimer ou inventer le montant de prêt demandé, le taux d'intérêt, la prime SCHL ou l'équité nette à injecter — ce sont des décisions du courtier, toujours marquées "à compléter".
- Chaque valeur financière ajoutée à un bilan ou un gabarit doit être traçable à une pièce justificative fournie par l'utilisateur.

## Origine

Construite à partir du Guide de normes SCHL de Levier (décembre 2024), des gabarits de suivi Levier, et de 9 présentations de dossiers SCHL réels (construction et financement long terme, 8 à 210 unités).

## Mise à jour — structure de l'attestation d'assurance (COI), par type de prêt

`skills/dossier-schl/references/structure-attestation-assurance.md` documente, à partir de 20 COI réels (5 construction, 5 prêt à l'achèvement, 5 acquisition, 5 refinancement), la structure commune du COI et ce qui distingue chaque type de prêt, ainsi que la longue liste d'obligations qui commencent seulement à l'émission du COI (paiement de la prime dans les 30 jours, échéancier des avances, formulaire d'avance échelonnée pour la construction, seuil de revenu brut réel pour le prêt à l'achèvement, attestations annuelles d'abordabilité et d'efficacité énergétique pour les dossiers APH Select, etc.). `dossier-schl/SKILL.md` inclut désormais une checklist de suivi post-COI, et `presentation-schl/references/champs-a-extraire.md` anticipe les éléments qui deviendront des clauses fermes du COI (type de contrat de construction, échéancier d'avances, période d'abordabilité).

## Mise à jour — diapositives obligatoires dans toute présentation SCHL

Consigne Mél (courtier Levier) : quel que soit le type de dossier, chaque présentation SCHL doit toujours inclure une diapositive d'organigramme confirmant la structure juridique / la détention de l'actif de l'emprunteur, ainsi qu'une diapositive de présentation du gestionnaire de l'immeuble. Pour un financement de type construction, une diapositive de présentation du constructeur/entrepreneur général est également obligatoire. `presentation-schl/references/menu-diapositives.md` et `presentation-schl/SKILL.md` marquent désormais ces trois diapositives comme non-optionnelles : si la documentation ne permet pas de les remplir, elles doivent être construites quand même avec les champs manquants marqués « À COMPLÉTER PAR LE COURTIER » plutôt qu'omises. `champs-a-extraire.md` inclut deux nouvelles sections (Gestionnaire de l'immeuble; Constructeur / entrepreneur général) pour guider l'extraction correspondante.

## Mise à jour — offre de service / mandat de courtage (nouvelle skill)

`offre-service-schl` a été construite à partir de l'analyse de 6 offres de service Levier réellement signées (MA2D Construction, Construction Morin, Groupe Marcillaud, Groupe Mathieu, Mellem Candiac, OTA Immobilier). Elle documente le texte fixe verbatim de la "Définition du mandat" (13 points identiques dans les 6 exemples) et du gabarit de "Signatures", les deux variantes de "Mention générale" selon le type de financement de la phase 1 (construction vs conventionnel/bridge), la gestion des mandats à projets multiples (ex. OTA : repositionnement + acquisition dans une même offre), et une palette/mise en page distincte de celle de `presentation-schl`. Les pourcentages d'honoraires ("Rétribution") ne sont jamais générés par défaut — ce sont des décisions du courtier, propres à chaque dossier.

## Mise à jour — normes gouvernementales officielles (2025-2026)

`skills/dossier-schl/references/normes-schl.md` a été enrichi avec le contenu du Manuel des prêteurs agréés par la SCHL (novembre 2025), des avis officiels SCHL/CMHC (dont les avis 241, 248, 250, 264, 268, 274, 275), des formulaires d'attestation MLI Select (accessibilité, efficacité énergétique, résultats sociaux), du barème des benchmarks nationaux, de la Liste de contrôle de la documentation requise (janvier 2026), des nouveaux gabarits du portail CMHC en ligne (« Multi-Unit Insurance Connect », 2026), et du registre des loyers SCHL 2026. Ce contenu gouvernemental prime sur le guide interne Levier de 2024 partout où il y a divergence — notamment : le tableau RPV maximal par type de prêt, la retenue pour réalisation du revenu locatif (RRRL), la distinction financement à la construction / à l'achèvement, la nouvelle méthodologie d'efficacité énergétique MLI Select (CNÉB/CNB 2020, % au-dessus du palier 1), et la structure de documentation par type de transaction/emprunteur. `skills/presentation-schl/references/champs-a-extraire.md` et `skills/gabarits-schl/references/structure-gabarits.md` ont aussi été mis à jour en conséquence (nouveaux champs MLI Select, portefeuille immobilier, gabarits portail 2026).
