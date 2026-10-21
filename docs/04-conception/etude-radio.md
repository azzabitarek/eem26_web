# Étude radio et dimensionnement de couverture

> **Processus PMBOK 6e — Conception (domaine PMBOK 7 *Delivery*) ; phase 5 du cycle en V**
> Périmètre : bloc d'instruction (2 étages, 7 bureaux, 5 salles de classe, 1 salle de réunion).

| | |
|---|---|
| **Référence** | RADIO-WIFI-2026-001 |
| **Version** | 1.0 |
| **Traçabilité** | Livrable WBS 5 ; exigences REQ-01, REQ-02, REQ-03, REQ-08, REQ-10 |

---

## 1. Objectifs de couverture et de capacité

| Zone | Type | Objectif signal | Densité cible | PA estimés |
|---|---|---|---|---|
| 5 salles de classe | Pédagogique (dense) | ≥ -65 dBm sur 95 % de la surface | ≤ 30 users/PA | 5–6 |
| 7 bureaux | Administratif | ≥ -67 dBm | ≤ 20 users/PA | 4–5 |
| 1 salle de réunion | Collaboratif/Visio | ≥ -65 dBm | ≤ 20 users/PA | 1–2 |
| Zones de circulation | Support | ≥ -70 dBm | Lié aux zones adjacentes | — |

**Total PA estimé : ~13** (1 par local, ajusté selon la modélisation).

## 2. Modélisation prédictive (simulation)

- Outil : type Ekahau / NetSpot / TamoGraph (ou équivalent) — [À préciser] ;
- Plans d'étage importés (échelle) + matériaux de paroi (béton, plâtre, vitrage) ;
- Puissance d'émission : 2,4 GHz ≈ 15–17 dBm, 5 GHz ≈ 17–20 dBm ;
- Objectifs de recouvrement (secondary coverage) pour l'itinérance.

### 2.1 Hypothèses de propagation

| Matériau | Atténuation approx. |
|---|---|
| Placoplâtre | 2–3 dB |
| Béton / mur porteur | 10–15 dB |
| Vitrage simple | 2–4 dB |
| Vitrage renforcé | 10–20 dB |

> Les murs épais (risque R03) sont traités par sur-dimensionnement local et positionnement adapté en couloir.

## 3. Relevé de site (site survey)

| Étape | Description |
|---|---|
| 1. Préparation | Plans RDC + 1er étage, identification des zones denses |
| 2. Relevé passif | Mesure de l'existant, bruit, interférences (2,4/5/6 GHz) |
| 3. Relevé prédictif | Simulation avant pose (positionnement virtuel des PA) |
| 4. Relevé actif (pilote) | Validation sur zone pilote (1 salle de classe RDC) |

## 4. Positionnement des points d'accès

| PA | Étage | Local / zone | Position recommandée | Canal 5 GHz |
|---|---|---|---|---|
| PA-01 | RDC | Salle de classe 1 | Plafond centre | 36 |
| PA-02 | RDC | Salle de classe 2 | Plafond centre | 40 |
| PA-03 | RDC | Salle de classe 3 | Plafond centre | 44 |
| PA-04 | RDC | Bureau 1 | Plafond / couloir | 48 |
| PA-05 | RDC | Bureaux 2-3 | Couloir (mutualisé) | 52 |
| PA-06 | RDC | Bureau 4 | Plafond | 56 |
| PA-07 | RDC | Circulation | Couloir | 60 |
| PA-08 | 1er | Salle de classe 4 | Plafond centre | 36 |
| PA-09 | 1er | Salle de classe 5 | Plafond centre | 40 |
| PA-10 | 1er | Salle de réunion | Plafond centre | 44 |
| PA-11 | 1er | Bureau 5 | Plafond / couloir | 48 |
| PA-12 | 1er | Bureaux 6-7 | Couloir (mutualisé) | 52 |
| PA-13 | 1er | Circulation | Couloir | 56 |

> Positionnement indicatif — à affiner selon la modélisation prédictive et le site survey.

## 5. Plan de canaux (5 GHz — réutilisation)

| Bande | Canaux utilisés | Largeur | Note |
|---|---|---|---|
| 5 GHz | 36, 40, 44, 48, 52, 56, 60 | 20 MHz (co-localisation) / 40–80 MHz si isolé | Éviter chevauchement entre PA voisins sur même étage |
| 2,4 GHz | 1, 6, 11 uniquement | 20 MHz | Non chevauchants, usage limité (IoT/legacy) |
| 6 GHz (si 6E) | Canaux dédiés | 80 MHz | Bande propre, sans interférence legacy |

**Règles de plan de canaux :**
- PA adjacents sur canaux non chevauchants (ex. étage 1 : 36/44/36 ; couloirs : 52/60) ;
- Éviter les canaux DFS partagés avec radar si environnement sensible ;
- Puissances réglées pour minimiser le recouvrement excessif (limiter l'itinérance trop fréquente).

## 6. Cartes de couverture (livrables)

| Carte | Contenu | Critère |
|---|---|---|
| Carte RDC | Signal 5 GHz | ≥ -65 dBm salles, ≥ -67 dBm bureaux |
| Carte 1er étage | Signal 5 GHz | idem + salle de réunion |
| Carte recouvrement | Secondary coverage | ≥ -75 dBm pour roaming |
| Carte interférences | Bruit / co-canal | Aucun canal critique saturé |

> Cartes thermiques à générer avec l'outil de simulation (captures à insérer ici une fois la simulation exécutée).

## 7. Validation radio (J5)

- Couverture conforme sur les 5 salles de classe et 7 bureaux ;
- Aucune zone morte en circulation ;
- Plan de canaux sans chevauchement critique ;
- Itinérance testée en zone pilote (REQ-08).
