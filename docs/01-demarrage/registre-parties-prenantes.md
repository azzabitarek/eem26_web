# Registre des parties prenantes

> **Processus PMBOK 6e — 6.2 Identifier les parties prenantes**
> Identification continue tout au long du projet. Mis à jour lors des revues de phases (cycle en V).

| | |
|---|---|
| **Référence** | PPP-WIFI-2026-001 |
| **Version** | 1.0 |
| **Date** | [À compléter] |
| **Responsable** | Chef de projet |
| **Légende pouvoir/intérêt** | H = Fort, M = Moyen, B = Faible |

---

## 1. Registre détaillé

### ID — PPP-01 : Direction générale / Présidence
- **Catégorie** : Interne
- **Rôle** : Commanditaire / Sponsor du projet
- **Pouvoir** : H — **Intérêt** : H
- **Attentes** : modernisation des outils pédagogiques, maîtrise budgétaire, image de l'établissement
- **Influence** : valide la charte, le budget, les jalons majeurs ; peut arbitrer les changements de périmètre
- **Stratégie d'engagement** : *Gérer de près* — sponsorship actif, revues aux jalons, reporting bimensuel
- **Communication** : comité de pilotage (J1, J4, J7, J10), note de synthèse

### ID — PPP-02 : Direction des Systèmes d'Information (DSI)
- **Catégorie** : Interne
- **Rôle** : Maître d'ouvrage fonctionnel ; responsable de l'exploitation future
- **Pouvoir** : H — **Intérêt** : H
- **Attentes** : architecture intégrable au réseau existant, sécurité conforme, exploitation supervisée, coût maîtrisé
- **Influence** : valide l'architecture, le plan d'adressage, la politique de sécurité
- **Stratégie d'engagement** : *Gérer de près* — implication dans toutes les revues de conception
- **Communication** : comité de pilotage, revues techniques, ateliers hebdomadaires

### ID — PPP-03 : Chef de projet
- **Catégorie** : Interne
- **Rôle** : Pilotage, planification, coordination, livraison des livrables PMBOK
- **Pouvoir** : M — **Intérêt** : H
- **Attentes** : moyens humains et accès aux informations (plans, relevés)
- **Influence** : planifie, anime, escalade les risques et demandes de changement
- **Stratégie d'engagement** : *Gérer de près* — pilotage quotidien
- **Communication** : rapports d'avancement, registre des risques, journal des changements

### ID — PPP-04 : RSSI / Responsable de la sécurité des SI
- **Catégorie** : Interne
- **Rôle** : Garant de la politique de sécurité
- **Pouvoir** : H — **Intérêt** : M
- **Attentes** : 802.1X, segmentation, filtrage, journalisation conforme RGPD
- **Influence** : droit de veto sur la politique de sécurité et le plan de segmentation
- **Stratégie d'engagement** : *Gérer de près* — validation formelle de la politique de sécurité (J6)
- **Communication** : ateliers sécurité, revue de conception, compte rendu de validation

### ID — PPP-05 : Responsable réseau / Administrateur infrastructure
- **Catégorie** : Interne
- **Rôle** : Expert technique du réseau filaire existant ; futur administrateur Wi-Fi
- **Pouvoir** : M — **Intérêt** : H
- **Attentes** : solution opérable, supervision intégrée, formation adaptée
- **Influence** : alimente l'audit (switchs, VLAN, PoE, débits), participe à l'étude radio et à la recette
- **Stratégie d'engagement** : *Gérer de près* — acteur clé de l'audit, de la conception et du pilote
- **Communication** : ateliers techniques hebdomadaires, site survey terrain

### ID — PPP-06 : Service technique / Bâtiment
- **Catégorie** : Interne
- **Rôle** : Contraintes physiques : gaines, accès toiture/comble, alimentation, travaux
- **Pouvoir** : M — **Intérêt** : M
- **Attentes** : minimisation des travaux, planning compatible avec l'exploitation du campus
- **Influence** : conditionne la faisabilité du positionnement des points d'accès
- **Stratégie d'engagement** : *Tenir informé* + consultation sur le phasage
- **Communication** : réunions de phasage par bâtiment, plans d'exécution

### ID — PPP-07 : Enseignants et corps professoral
- **Catégorie** : Interne
- **Rôle** : Utilisateurs principaux des usages pédagogiques
- **Pouvoir** : B — **Intérêt** : M
- **Attentes** : couverture fiable en salle de cours, visioconférence sans coupure, pas de perturbation pendant les cours
- **Influence** : validateurs des besoins par zone, prescripteurs des exigences de débit
- **Stratégie d'engagement** : *Tenir informé* — questionnaire de besoins, restitution des résultats
- **Communication** : questionnaire de recueil des besoins, note de synthèse, affichage

### ID — PPP-08 : Étudiants
- **Catégorie** : Interne (utilisateurs finaux)
- **Rôle** : Utilisateurs majoritaires (BYOD, plateformes pédagogiques)
- **Pouvoir** : B — **Intérêt** : H
- **Attentes** : Wi-Fi haut débit partout, accès invités simple, stabilité
- **Influence** : mesuré via les statistiques de densité et les enquêtes de satisfaction
- **Stratégie d'engagement** : *Tenir informé* — mesure de densité, communication sur le projet
- **Communication** : sondages, affichage, revue des besoins

### ID — PPP-09 : Responsable administratif / Comptabilité
- **Catégorie** : Interne
- **Rôle** : Suivi budgétaire et procédures d'approvisionnement
- **Pouvoir** : M — **Intérêt** : M
- **Attentes** : chiffrage fiable, respect des procédures de commande
- **Influence** : valide le budget et le plan d'approvisionnement
- **Stratégie d'engagement** : *Tenir informé* — implication dès la phase de chiffrage
- **Communication** : revue budgétaire (J7), devis justifiés

### ID — PPP-10 : Fournisseurs / Éditeurs Wi-Fi (externes)
- **Catégorie** : Externe
- **Rôle** : Consultation technique, devis, documentation produit
- **Pouvoir** : M — **Intérêt** : M
- **Attêtes** : cahier des charges clair, délais de réponse raisonnables
- **Influence** : proposent les technologies et conditionnent les délais d'approvisionnement (R06)
- **Stratégie d'engagement** : *Surveiller* — consultation formelle, comparaison des offres
- **Communication** : consultation au cahier des charges, réponses formalisées

### ID — PPP-11 : Prestataire d'études / Site survey (externe, si recours)
- **Catégorie** : Externe
- **Rôle** : Modélisation radio prédictive et relevé terrain
- **Pouvoir** : M — **Intérêt** : M
- **Attentes** : périmètre et critères de couverture précis
- **Influence** : qualité des cartes de couverture et du positionnement des PA
- **Stratégie d'engagement** : *Surveiller* — cadrage contractuel des livrables radio
- **Communication** : brief technique, validation des livrables (J5)

### ID — PPP-12 : Hébergeur / Opérateur d'accès Internet
- **Catégorie** : Externe
- **Rôle** : Capacité de l'accès sortant (débit, redondance)
- **Pouvoir** : M — **Intérêt** : B
- **Attentes** : anticipation des besoins de débit
- **Influence** : conditionne le dimensionnement de l'accès Internet
- **Stratégie d'engagement** : *Tenir informé* — consultation sur le dimensionnement
- **Communication** : demande d'offre si évolution du contrat

## 2. Matrice pouvoir/intérêt (analyse de salience)

| | Intérêt élevé | Intérêt faible |
|---|---|---|
| **Pouvoir élevé** | **Gérer de près** : PPP-01 Direction, PPP-02 DSI, PPP-04 RSSI, PPP-05 Réseau | **Satisfaire** : PPP-09 Compta |
| **Pouvoir faible** | **Tenir informé** : PPP-07 Enseignants, PPP-08 Étudiants, PPP-06 Technique, PPP-10 Fournisseurs, PPP-11 Prestataire | **Surveiller** : PPP-12 Opérateur |

## 3. Plan d'engagement par phase (cycle en V)

| Phase | Parties prenantes mobilisées | Engagement |
|---|---|---|
| 1. Cadrage | PPP-01, PPP-02, PPP-03 | Validation charte, constitution équipe |
| 2. Audit & besoins | PPP-05, PPP-06, PPP-07, PPP-08 | Questionnaires, relevés, site survey |
| 3. Spécification | PPP-02, PPP-04, PPP-05 | Cahier des charges technique |
| 4. Architecture | PPP-02, PPP-05, PPP-10 | Revue de conception |
| 5. Étude radio | PPP-05, PPP-06, PPP-11 | Positionnement et cartes de couverture |
| 6. Sécurité | PPP-04, PPP-02 | Validation politique sécurité |
| 7. Chiffrage | PPP-01, PPP-09, PPP-10, PPP-12 | Devis, budget, approvisionnement |
| 8. Planification | PPP-01, PPP-03, PPP-06 | Gantt, phasage, risques |
| 9. Recette | PPP-04, PPP-05, PPP-07 | Validation pilote/simulation |
| 10. Clôture | Toutes les PPP | Restitution, leçons apprises |

## 4. Éléments à compléter

- Noms et coordonnées des personnes par rôle (colonne contact) ;
- Référent de chaque partie prenante dans l'organigramme réel de l'établissement ;
- Dates des comités de pilotage.
