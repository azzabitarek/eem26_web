# Matrice des exigences (Requirements Traceability Matrix)

> **Processus PMBOK 6e — 5.2 Collecter les exigences**
> Traçabilité : de la source (partie prenante) au besoin, à l'exigence, au livrable du WBS, aux critères d'acceptation et au test de recette.
> Périmètre : bloc d'instruction — 2 étages, 7 bureaux, 5 salles de classe, 1 salle de réunion. Durée 3 mois.

| | |
|---|---|
| **Référence** | RTM-WIFI-2026-001 |
| **Version** | 1.0 |
| **Priorité** | M = Must (obligatoire), S = Should (important), C = Could (souhaitable) |

---

## 1. Matrice de traçabilité

| ID | Source (PPP) | Besoin | Exigence | Type | Priorité | Livrable WBS | Critère d'acceptation | Test recette |
|---|---|---|---|---|---|---|---|---|
| REQ-01 | PPP-07/08 Enseignants, Étudiants | Couverture fiable dans les 5 salles de classe | Signal ≥ -65 dBm sur ≥ 95 % de la surface des salles de classe | Couverture | M | 5 (Étude radio) | Cartes thermiques conformes sur les 5 salles | T-C1 mesure de couverture |
| REQ-02 | PPP-02 DSI | Capacité suffisante en zone dense | 1 PA pour ≤ 30 utilisateurs simultanés ; débit ≥ 10 Mbit/s/utilisateur | Capacité | M | 3.2 + 5 (Dimensionnement) | Simulation de charge validée | T-C2 test de charge |
| REQ-03 | PPP-01 Direction | Couverture des zones administratives | Couverture ≥ -67 dBm dans les 7 bureaux et la salle de réunion | Couverture | M | 5 (Étude radio) | Cartes thermiques conformes | T-C1 |
| REQ-04 | PPP-02 DSI | Intégration au réseau existant | Interconnexion au réseau filaire et à l'accès Internet, QoS configurée | Intégration | M | 4.5 | Revue d'architecture validée | Revue J4 |
| REQ-05 | PPP-04 RSSI | Authentification centralisée | 802.1X avec serveur RADIUS pour les utilisateurs internes | Sécurité | M | 6.1 | Politique validée par le RSSI | Revue J6 |
| REQ-06 | PPP-04 RSSI | Accès invités maîtrisé | Portail captif isolé, débit limité, traçabilité des connexions | Sécurité | M | 6.2 | Portail fonctionnel en pilote | T-S1 test invités |
| REQ-07 | PPP-04 RSSI | Isolation des flux | Segmentation VLAN : pédagogique, administratif, invités, IoT | Sécurité | M | 4.4 | Plan de segmentation validé | Revue J4 |
| REQ-08 | PPP-08 Étudiants | Couverture mobile continue | Itinérance (roaming) sans coupure perceptible entre zones | QoS | S | 5.4 | Coupure < 50 ms lors du roaming | T-Q1 test itinérance |
| REQ-09 | PPP-07 Enseignants | Qualité pour la visioconférence | Priorisation QoS du temps réel en salle de classe et réunion | QoS | S | 3.3 | Classification QoS active | T-Q2 |
| REQ-10 | PPP-06 Bâtiment | Contraintes du bâti | Positionnement des PA compatible avec murs épais et gaines existantes | Technique | M | 2.4 + 5.3 | Plan de positionnement validé sur site | Site survey J5 |
| REQ-11 | PPP-05 Réseau | Alimentation des équipements | Alimentation PoE/PoE+ conforme au standard retenu | Technique | M | 4.1 + 4.2 | Bilan de puissance PoE validé | Revue J4 |
| REQ-12 | PPP-09 Comptabilité | Maîtrise budgétaire | Budget avec incertitude ≤ ±20 % ; CAPEX + OPEX chiffrés | Coût | M | 7.2 + 7.3 | Budget approuvé | Revue J7 |
| REQ-13 | PPP-01 Direction | Respect du planning | Livraison du dossier dans un délai de 3 mois | Calendrier | M | 8.2 | Tous les jalons J1→J10 tenus | Revue jalons |
| REQ-14 | PPP-07 Enseignants | Non-perturbation | Phasage du déploiement hors périodes de cours | Contrainte | M | 8.3 | Phasage validé par les parties prenantes | Revue J8 |
| REQ-15 | PPP-02 DSI | Exploitabilité | Supervision et guide d'exploitation remis | Exploitation | S | 10.1 | Guide et supervision documentés | Revue J10 |
| REQ-16 | PPP-04 RSSI | Conformité des journaux | Journalisation conforme RGPD (durée, accès, anonymisation) | Conformité | M | 6.3 | Analyse de conformité validée | Revue J6 |
| REQ-17 | PPP-03 Chef de projet | Traçabilité projet | Registre des risques, Gantt et chemin critique produits | Gestion | M | 8.5 + 8.2 | Livrables approuvés | Revue J8 |
| REQ-18 | PPP-01/02 | Évolutivité | Architecture extensible (déploiement futur à d'autres bâtiments) | Technique | C | 4.1 | Revue d'architecture — marge justifiée | Revue J4 |

## 2. Synthèse par type d'exigence

| Type | Nombre | ID |
|---|---|---|
| Couverture | 3 | REQ-01, REQ-03, REQ-10 |
| Capacité / Débit | 1 | REQ-02 |
| Intégration | 1 | REQ-04 |
| Sécurité / Conformité | 5 | REQ-05, REQ-06, REQ-07, REQ-16, REQ-18 |
| QoS / Itinérance | 2 | REQ-08, REQ-09 |
| Technique / PoE | 1 | REQ-11 |
| Coût / Calendrier / Gestion | 3 | REQ-12, REQ-13, REQ-17 |
| Exploitation | 1 | REQ-15 |

## 3. Exigences par zone (densité)

| Zone | Local | Catégorie | Priorité couverture | Exigences liées |
|---|---|---|---|---|
| RDC | Salle de classe 1–3 | Pédagogique (dense) | M | REQ-01, REQ-02, REQ-09 |
| RDC | Bureaux 1–4 | Administratif | M | REQ-03, REQ-05 |
| 1er étage | Salle de classe 4–5 | Pédagogique (dense) | M | REQ-01, REQ-02, REQ-09 |
| 1er étage | Bureaux 5–7 | Administratif | M | REQ-03, REQ-05 |
| 1er étage | Salle de réunion | Collaboratif / Visio | M | REQ-03, REQ-08, REQ-09 |

## 4. Note

Toutes les exigences **M (Must)** sont traçables à un livrable du WBS et à un test ou une revue de validation. Les exigences S/C font l'objet d'un arbitrage si une contrainte (budget, délai 3 mois) l'impose, via le contrôle intégré des changements.
