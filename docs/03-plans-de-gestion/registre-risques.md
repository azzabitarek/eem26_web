# Registre et plan de gestion des risques

> **Processus PMBOK 6e — 11.1 Planifier la gestion des risques, 11.2 Identifier, 11.3 Analyse qualitative, 11.4 Analyse quantitative, 11.5 Planifier les réponses**
> Échelle probabilité/impact : 1 = Très faible, 2 = Faible, 3 = Moyen, 4 = Élevé, 5 = Très élevé. Criticité = P × I.

| | |
|---|---|
| **Référence** | RISK-WIFI-2026-001 |
| **Version** | 1.0 |
| **Criticité** | Faible (1–6), Moyenne (7–12), Élevée (13–19), Critique (20–25) |

---

## 1. Registre des risques

| ID | Risque | Catégorie | P | I | Criticité | Réponse | Stratégie |
|---|---|---|---|---|---|---|---|
| R01 | Sous-estimation de la densité d'utilisateurs | Besoins | 4 | 5 | **20 Critique** | Recensement terrain systématique (13 locaux), marge +30 % (REQ-02), comptage à l'heure de pointe | Atténuer |
| R02 | Interférences radio (voisinage, 2,4/5/6 GHz) | Technique | 3 | 4 | **12 Moyenne** | Modélisation prédictive, site survey, plan de canaux, choix 5/6 GHz | Atténuer |
| R03 | Contraintes du bâti (murs épais, gaines absentes) | Technique | 4 | 4 | **16 Élevée** | Audit bâti (A2), positionnement adapté, recours à solutions sans câblage si besoin | Atténuer |
| R04 | Indisponibilité du câblage/PoE | Technique | 3 | 4 | **12 Moyenne** | Audit PoE (A2), bilan de puissance, prévoir switchs PoE+ (EQ-03) | Atténuer |
| R05 | Dépassement budgétaire | Coût | 3 | 4 | **12 Moyenne** | Devis multiples, contingence 10 % + marge 5 %, comparaison S1/S2/S3 | Atténuer |
| R06 | Délais d'approvisionnement | Calendrier | 3 | 3 | **9 Moyenne** | Consultation anticipée (S9), fournisseurs référencés, plan d'appro | Transférer/Atténuer |
| R07 | Failles de sécurité non traitées | Sécurité | 2 | 5 | **10 Moyenne** | Validation RSSI (J6), 802.1X, tests de pénétration du pilote | Atténuer |
| R08 | Perturbation des enseignements | Parties prenantes | 3 | 3 | **9 Moyenne** | Phasage hors cours (A23), phase RDC puis étage, pilote | Atténuer |
| R09 | Obsolescence technologique rapide | Technique | 2 | 4 | **8 Moyenne** | Choix Wi-Fi 6/6E évolutif (REQ-18), veille technologique | Accepter/Atténuer |
| R10 | Disponibilité des parties prenantes (validations) | Organisation | 3 | 3 | **9 Moyenne** | Jalons planifiés, relances, suppléants désignés | Atténuer |
| R11 | Qualité des plans de bâtiment (obsolètes/incomplets) | Besoins | 3 | 3 | **9 Moyenne** | Relevé terrain contradictoire (site survey), vérification sur site | Atténuer |
| R12 | Dérive du périmètre (scope creep) | Périmètre | 3 | 3 | **9 Moyenne** | Contrôle intégré des changements, WBS de référence, validation sponsor | Atténuer |

## 2. Matrice probabilité × impact

| P\I | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| **5** | | | | | |
| **4** | | | | R03 | **R01** |
| **3** | | | R06,R08,R10,R11,R12 | R02,R04,R05 | |
| **2** | | | | R09 | R07 |
| **1** | | | | | |

## 3. Plan de réponses détaillé (risques majeurs)

### R01 — Sous-estimation de la densité (Critique)
- **Mitigation** : recensement exhaustif des 13 locaux (A3) à l'heure de pointe, croisement avec les effectifs pédagogiques et administratifs, marge de capacité +30 %.
- **Réserve** : prévoir la révision du dimensionnement (A13) si les relevés diffèrent de > 20 % des hypothèses.
- **Responsable** : Chef de projet / Ingénieur radio.

### R03 — Contraintes du bâti (Élevée)
- **Mitigation** : audit complet du bâti (A2 : murs, gaines, accès), site survey (A12), alternatives en cas de gaine absente.
- **Responsable** : Ingénieur radio / Service technique.

## 4. Processus de gestion des risques

| Étape | Action | Fréquence |
|---|---|---|
| Identification | Revue du registre | Chaque fin de phase |
| Analyse | Réévaluation P/I/criticité | Mensuel |
| Réponses | Mise à jour des plans | Sur déclenchement |
| Surveillance | Suivi des indicateurs de déclenchement | Hebdomadaire |

## 5. Indicateurs de déclenchement (triggers)

- R01 : écart > 20 % entre densité relevée et hypothèse initiale ;
- R02/R03 : impossibilité de positionner un PA dans une zone dense ;
- R05 : devis reçus > enveloppe + 15 % ;
- R06 : délai fournisseur annoncé > 6 semaines ;
- R08 : chevauchement du phasage avec une période d'examens.
