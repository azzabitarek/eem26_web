# Plan de gestion des coûts

> **Processus PMBOK 6e — 7.1 Planifier la gestion des coûts, 7.2 Estimer les coûts, 7.3 Déterminer le budget**
> Estimation avec incertitude ≤ ±20 % (exigence REQ-12). Devise : [À compléter : EUR/DZD/MAD].

| | |
|---|---|
| **Référence** | COST-WIFI-2026-001 |
| **Version** | 1.0 |
| **Devise** | [À compléter] |
| **Méthode d'estimation** | Analogique + paramétrique + devis fournisseurs |

---

## 1. Coûts du projet d'étude (CE PROJET — bloc d'instruction)

Ce projet porte sur l'étude/conception/planification. Les coûts ci-dessous sont ceux du projet.

| Code WBS | Poste | Quantité | Coût unitaire | Total | Type |
|---|---|---|---|---|---|
| 1 | Pilotage / chef de projet | 13 sem | [À compléter] | [À compléter] | Main d'œuvre |
| 2 | Ingénieur réseau (audit) | 3 sem | [À compléter] | [À compléter] | Main d'œuvre |
| 4 | Architecte réseau | 2,5 sem | [À compléter] | [À compléter] | Main d'œuvre |
| 5 | Ingénieur radio (survey/simulation) | 2,5 sem | [À compléter] | [À compléter] | Main d'œuvre |
| 6 | Expert sécurité (RSSI) | 2 sem | [À compléter] | [À compléter] | Main d'œuvre |
| 9 | Ingénieur QA réseau | 2 sem | [À compléter] | [À compléter] | Main d'œuvre |
| 1 | Outils / licences simulation radio | 1 | [À compléter] | [À compléter] | Achat |
| — | **Total projet d'étude** | | | **[À compléter]** | |

## 2. Nomenclature du déploiement (CAPEX — indicatif, hors réalisation)

| Réf | Équipement | Qté | Prix unitaire | Total | Notes |
|---|---|---|---|---|---|
| EQ-01 | Points d'accès Wi-Fi 6/6E | ~13 | [À compléter] | [À compléter] | 1 par local, ajusté selon étude radio |
| EQ-02 | Contrôleur Wi-Fi / licence cloud | 1 | [À compléter] | [À compléter] | Selon choix technologique |
| EQ-03 | Switch PoE+ (48 ports) | 2 | [À compléter] | [À compléter] | Alimentation des PA |
| EQ-04 | Serveur RADIUS / appliance auth | 1 | [À compléter] | [À compléter] | 802.1X |
| EQ-05 | Câblage / gaines / supports | lot | [À compléter] | [À compléter] | Selon état du bâti |
| EQ-06 | Onduleurs / armoire | 1 | [À compléter] | [À compléter] | RDC + étage |
| EQ-07 | Mise en œuvre / configuration (prestation) | lot | [À compléter] | [À compléter] | Hors périmètre projet |
| | **Total CAPEX** | | | **[À compléter]** | |

## 3. Coûts d'exploitation (OPEX annuel — indicatif)

| Poste | Fréquence | Montant annuel |
|---|---|---|
| Maintenance constructeur / support | annuel | [À compléter] |
| Licences contrôleur / cloud | annuel | [À compléter] |
| Supervision (outil NMS) | annuel | [À compléter] |
| Consommation électrique (PoE) | annuel | [À compléter] |
| Formation / montée en compétence | ponctuel | [À compléter] |
| **Total OPEX annuel** | | **[À compléter]** |

## 4. Budget global (vue synthétique)

| Catégorie | Montant | Nature |
|---|---|---|
| Projet d'étude (ce projet) | [À compléter] | Coût du projet PMBOK |
| CAPEX déploiement (indicatif) | [À compléter] | Hors périmètre, informatif |
| OPEX annuel (indicatif) | [À compléter] | Hors périmètre, informatif |

## 5. Analyse coût/bénéfice et comparaison des solutions

| Scénario | Description | CAPEX | OPEX | Avantages | Inconvénients |
|---|---|---|---|---|---|
| S1 | Wi-Fi 6 on-premise (contrôleur) | [À compléter] | [À compléter] | Maîtrise totale, pas de dépendance cloud | Investissement initial |
| S2 | Wi-Fi 6/6E gestion cloud | [À compléter] | [À compléter] | Déploiement rapide, évolutif | Abonnement récurrent |
| S3 | Wi-Fi 5 (économie) | [À compléter] | [À compléter] | Coût faible | Obsolescence (R09) |

**Recommandation** : [À compléter après devis — favoriser Wi-Fi 6/6E pour l'évolutivité REQ-18].

## 6. Réserve de contingence

| Poste | Taux | Montant |
|---|---|---|
| Contingence (risques identifiés) | 10 % | [À compléter] |
| Marge de gestion (risques non identifiés) | 5 % | [À compléter] |

## 7. Contrôle des coûts

- Suivi mensuel de l'avancement vs budget (courbe en S — Earned Value) ;
- Indicateurs : CV (écart coût), CPI (indice performance coût) ;
- Toute dépense > [seuil] requiert l'approbation du sponsor (contrôle intégré des changements).
