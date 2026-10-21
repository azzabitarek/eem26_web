# Charte du projet

> **Processus PMBOK 6e — 6.1 Élaborer la charte du projet**
> Document d'autorisation officielle du projet. Le sponsor le signe, le chef de projet reçoit son autorité.

| | |
|---|---|
| **Référence** | CHART-WIFI-2026-001 |
| **Version** | 1.1 |
| **Date d'autorisation** | [À compléter] |
| **Chef de projet** | [À compléter] |
| **Sponsor / Commanditaire** | [À compléter : ex. Direction des Systèmes d'Information] |
| **Périmètre physique** | Bloc d'instruction — bâtiment de 2 étages : 7 bureaux, 5 salles de classe, 1 salle de réunion (13 locaux) |
| **Durée du projet** | 3 mois (13 semaines) |
| **Cycle de vie projet** | Cycle en V (étude, conception, planification) |
| **Approche de livraison** | Prédictive (PMBOK 7 — domaine *Development approach & life cycle*) |

---

## 1. Justification (raison stratégique)

L'établissement [À compléter : nom de l'université/établissement] doit doter son **bloc d'instruction** (bâtiment de deux étages comprenant 7 bureaux, 5 salles de classe et 1 salle de réunion) d'une connectivité sans fil moderne répondant à :

- des **usages pédagogiques** croissants (LMS, visioconférences, travail collaboratif, BYOD étudiant) dans les 5 salles de classe ;
- des **besoins administratifs** (mobilité des services, accès aux applications internes) dans les 7 bureaux et la salle de réunion ;
- à l'insuffisance probable de la couverture et de la capacité du réseau existant face à la densité actuelle des utilisateurs.

Le présent projet porte sur l'**étude, la conception et la planification** du déploiement sur ce bâtiment, pour une **durée de 3 mois**. Il vise à produire un dossier de référence permettant au commanditaire de décider et de lancer sereinement le déploiement physique.

## 2. Objectifs mesurables (SMART)

| # | Objectif | Indicateur de mesure |
|---|---|---|
| O1 | Recenser les besoins par zone et catégorie d'utilisateurs | 100 % des zones et catégories couvertes par une fiche de besoins (nombre d'utilisateurs, densité, usages, débit souhaité) |
| O2 | Concevoir l'architecture du réseau | Dossier d'architecture complet (topologie logique et physique, segmentation VLAN, PoE, plan d'adressage, intégration au filaire et à l'Internet) validé en revue |
| O3 | Dimensionner couverture et capacité | Couverture prédictive ≥ -65 dBm dans 95 % des zones pédagogiques ; capacité dimensionnée pour la densité relevée + 30 % de marge |
| O4 | Définir la politique de sécurité | Authentification centralisée 802.1X, accès invités, filtrage et journalisation documentés et validés par le RSSI/RSSI-adjoint |
| O5 | Chiffrer le projet | Budget d'investissement et d'exploitation estimé avec une incertitude ≤ ±20 % |
| O6 | Planifier le déploiement sans perturber les enseignements | Gantt phasé par bâtiment hors périodes de cours, chemin critique identifié |
| O7 | Définir la recette et l'exploitation | Plan de recette avec critères mesurables (couverture, débit, itinérance, charge) ; guide d'exploitation et de supervision remis |

## 3. Description sommaire du projet

Conception et planification du déploiement d'un réseau Wi-Fi couvrant les besoins pédagogiques et administratifs du **bloc d'instruction** : dimensionnement de la couverture et de la capacité, sécurité, budget, calendrier et plan de recette. **Durée : 3 mois.**

### 3.0 Périmètre physique (bloc d'instruction)

| Étage | Locaux | Quantité | Usage dominant |
|---|---|---|---|
| RDC | Salles de classe | 3 | Pédagogique (densité forte) |
| RDC | Bureaux | 4 | Administratif |
| 1er étage | Salles de classe | 2 | Pédagogique (densité forte) |
| 1er étage | Bureaux | 3 | Administratif |
| 1er étage | Salle de réunion | 1 | Collaboratif / visioconférence |
| **Total** | | **13 locaux** | 5 salles de classe, 7 bureaux, 1 salle de réunion |

### 3.1 Inclus au périmètre (Study/Conception/Planning)
- Cadrage et recueil des besoins ;
- Audit de l'existant (plans, réseau filaire, trafic, usages, densité) ;
- Rédaction du cahier des charges technique ;
- Architecture (topologie, choix technologiques, adressage, segmentation) ;
- Étude radio (modélisation prédictive, site survey, positionnement PA, plan de canaux) ;
- Politique de sécurité et d'authentification ;
- Estimation budgétaire (investissement et exploitation) et plan d'approvisionnement ;
- WBS, calendrier, phasage par bâtiment, plan de gestion des risques ;
- Plan de tests et de recette (validation sur zone pilote ou simulation) ;
- Guide d'exploitation/supervision, formation des administrateurs, restitution.

### 3.2 Exclus du périmètre (hors projet)
- Travaux physiques : pose de câbles, de bornes, d'armoires, travaux de bâtiment ;
- Commande et réception du matériel (objet d'une phase ultérieure) ;
- Déploiement réel et mise en production ;
- Maintenance et exploitation opérationnelle après recette.

## 4. Exigences sommaires

- **Technologie Wi-Fi** : génération retenue selon l'état de l'art et le budget (ex. Wi-Fi 6/6E) ;
- **Contrôleur / architecture** : mode contrôlé ou cloud, dimensionnement ;
- **Segmentation** : VLAN séparant usages (pédagogique, administratif, invités, IoT) ;
- **Alimentation** : PoE/PoE+ adapté au standard retenu ;
- **Intégration** : interconnexion au réseau filaire existant et à l'accès Internet (débit de sortie, QoS) ;
- **Sécurité** : 802.1X (RADIUS), accès invités, filtrage, journalisation ;
- **Qualité de service** : priorisation des usages temps réel (visioconférence) ;
- **Conformité** : [À compléter : référentiel(s) de l'établissement, RGPD pour les journalisations].

## 5. Livrables sommaires

1. Charte du projet et registre des parties prenantes *(livré à l'étape 1)* ;
2. Rapport d'audit de l'existant et cahier des charges technique ;
3. Dossier d'architecture : schémas logique et physique, plan d'adressage et de segmentation ;
4. Plan de couverture (cartes thermiques), positionnement des points d'accès et plan de canaux ;
5. Politique de sécurité et d'authentification ;
6. Budget détaillé (nomenclature, devis estimatif, coût d'exploitation) ;
7. WBS, diagramme de Gantt et chemin critique ; registre des risques ;
8. Plan de tests et de recette, avec rapport de validation du pilote ou de la simulation ;
9. Guide d'exploitation et de supervision.

## 6. Contraintes

- **Méthodologie** : cycle en V ; démarche PMBOK pour la gestion de projet ;
- **Périmètre** : limité à l'étude/conception/planification (pas d'exécution physique) ;
- **Perturbations** : le phasage planifié ne doit pas perturber les enseignements ;
- **Budget** : enveloppe d'étude fixée par le commanditaire — [À compléter] ;
- **Accès** : disponibilité des plans de bâtiments, du réseau filaire et des relevés de site ;
- **Ressources** : équipe projet et compétences radio/sécurité disponibles — [À compléter].

## 7. Hypothèses

- Les plans d'étage et l'inventaire réseau existant sont accessibles et à jour ;
- Les responsables de bâtiments sont disponibles pour le site survey ;
- Le parc filaire (switchs, gaines, PoE) est auditables avant la conception ;
- Le budget d'étude est validé à la signature de la charte ;
- Les fournisseurs répondent aux consultations (devis) dans les délais planifiés.

## 8. Risques sommaires (registre préliminaire — détaillé à l'étape 6)

| ID | Risque | Catégorie |
|---|---|---|
| R01 | Sous-estimation de la densité d'utilisateurs | Besoins/Conception |
| R02 | Interférences radio (voisinage, 2,4/5/6 GHz) | Technique |
| R03 | Contraintes du bâti (murs épais, gaines absentes) | Technique/Environnement |
| R04 | Indisponibilité du câblage ou de l'alimentation PoE | Technique |
| R05 | Dépassement budgétaire | Coûts |
| R06 | Délais d'approvisionnement des équipements | Calendrier/Fournisseurs |
| R07 | Failles de sécurité identifiées ou non traitées | Sécurité |
| R08 | Perturbation des enseignements pendant l'installation | Parties prenantes |
| R09 | Obsolescence technologique rapide du matériel choisi | Technique |

## 9. Calendrier sommaire (jalons)

Durée totale : **3 mois (13 semaines)**. Date de démarrage : [À compléter : ex. S1 = 01/03].

| Jalon | Description | Semaine cible | Mois |
|---|---|---|---|
| J1 | Charte signée, parties prenantes identifiées | S1 | M1 |
| J2 | Audit de l'existant et besoins validés (13 locaux) | S3 | M1 |
| J3 | Cahier des charges technique approuvé | S4 | M1 |
| J4 | Dossier d'architecture validé (revue de conception) | S6 | M2 |
| J5 | Étude radio livrée (cartes de couverture, plan de canaux) | S8 | M2 |
| J6 | Politique de sécurité validée | S9 | M3 |
| J7 | Budget et plan d'approvisionnement approuvés | S10 | M3 |
| J8 | WBS, Gantt, risques et phasage approuvés | S10 | M3 |
| J9 | Plan de recette validé (pilote/simulation) | S12 | M3 |
| J10 | Dossier restitué et projet clos | S13 | M3 |

## 10. Budget sommaire

| Poste | Montant estimé |
|---|---|
| Enveloppe d'étude (ce projet) | [À compléter] |
| Estimation CAPEX déploiement (hors réalisation, indicative) | [À compléter : fourchette] |
| Estimation OPEX annuel (exploitation, supervision, licences) | [À compléter : fourchette] |

## 11. Parties prenantes clés

Direction générale, DSI, enseignants, étudiants, service technique/bâtiment, gestionnaire réseau, RSSI, fournisseurs/éditeurs — détail et stratégie d'engagement dans `registre-parties-prenantes.md`.

## 12. Critères d'achèvement (définition de « terminé »)

- Tous les livrables §5 remis au sponsor ;
- Revue finale du dossier passée avec les parties prenantes clés ;
- Plan de recette validé et guide d'exploitation remis ;
- Leçons apprises documentées.

## 13. Approbations

| Rôle | Nom | Signature | Date |
|---|---|---|---|
| Sponsor / Commanditaire | [À compléter] | | |
| Chef de projet | [À compléter] | | |
| Représentant RSSI | [À compléter] | | |
