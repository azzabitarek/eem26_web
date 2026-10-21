# Politique de sécurité et d'authentification

> **Processus PMBOK 6e — Conception (domaine PMBOK 7 *Delivery*) ; phase 6 du cycle en V**
> Périmètre : bloc d'instruction. Validation : RSSI (jalon J6).

| | |
|---|---|
| **Référence** | SEC-WIFI-2026-001 |
| **Version** | 1.0 |
| **Traçabilité** | Livrable WBS 6 ; exigences REQ-05, REQ-06, REQ-07, REQ-16 |

---

## 1. Principes directeurs

- **Zéro confiance implicite** : tout accès authentifié et segmenté ;
- **Moindre privilège** : chaque profil d'utilisateur accède au strict nécessaire ;
- **Traçabilité** : journalisation conforme RGPD (REQ-16) ;
- **Isolation** : aucun flux inter-VLAN non explicitement autorisé.

## 2. Authentification centralisée (802.1X)

| Élément | Choix | Détail |
|---|---|---|
| Protocole | WPA2-Enterprise / WPA3-Enterprise | 802.1X |
| Serveur | RADIUS (type FreeRADIUS / NPS / ClearPass) | Authentification centralisée |
| Méthode EAP | EAP-TLS (certificats) recommandé ; PEAP-MSCHAPv2 en secours | TLS=fort, PEAP=compatibilité |
| Annuaire | LDAP / Active Directory | Comptes utilisateurs |
| Attribution VLAN | Dynamic VLAN via RADIUS | Pédagogique/Administratif selon profil |

**Flux d'authentification :**
```
Client → (EAP) → PA → (RADIUS) → Serveur RADIUS → (LDAP) → Annuaire
                                     ↓
                          Attribution VLAN + ACL
```

## 3. Profils d'accès

| Profil | Population | Authentification | VLAN | Accès |
|---|---|---|---|---|
| Étudiants | Étudiants | 802.1X (EAP) | Pédagogique | Internet + ressources pédagogiques |
| Personnel | Enseignants/admin | 802.1X (EAP) | Administratif | Applications internes + Internet |
| Invités | Visiteurs | Portail captif | Invités | Internet uniquement, débit limité |
| IoT/Gestion | PA, contrôleur | PSK fort / certificat | IoT | Administration uniquement |

## 4. Accès invités (REQ-06)

- **Portail captif** avec acceptation des conditions d'usage ;
- Comptes temporaires (durée limitée : 1 jour / 1 semaine) ;
- Bande passante limitée par client (ex. 5 Mbit/s) ;
- **Isolation client** (pas de communication invité↔invité, ni vers réseaux internes) ;
- Journalisation des connexions invités.

## 5. Filtrage et segmentation (REQ-07)

| Règle | Source | Destination | Action |
|---|---|---|---|
| SG-01 | Pédagogique | Internet | Autoriser (proxy filtré) |
| SG-02 | Pédagogique | Administratif | Refuser |
| SG-03 | Administratif | Internet + interne | Autoriser |
| SG-04 | Invités | Internet | Autoriser (limité) |
| SG-05 | Invités | Tout réseau interne | Refuser |
| SG-06 | IoT | Réseaux utilisateurs | Refuser |
| SG-07 | MGMT | Équipements | Autoriser (SSH/HTTPS admin) |

## 6. Journalisation et conformité RGPD (REQ-16)

| Donnée journalisée | Durée de conservation | Base légale |
|---|---|---|
| Authentifications (succès/échec) | 6 mois | Sécurité SI |
| Association MAC/IP (sessions) | 30 jours | Sécurité SI |
| Connexions invités (identité portail) | Durée nécessaire | Consentement |
| Logs équipements (syslog) | 3 mois | Sécurité SI |

- **Minimisation** : collecter uniquement le nécessaire ;
- **Droit d'accès / effacement** : procédure définie avec le DPO [À compléter] ;
- **Accès aux journaux** : restreint aux administrateurs habilités.

## 7. Durcissement des équipements

- Mots de passe/PSK forts, rotation régulière ;
- Désactivation des services inutiles (Telnet, HTTP non chiffré) ;
- Mise à jour firmware planifiée ;
- Administration via VLAN MGMT isolé ;
- Désactivation du SSID beacon si non requis (mode furtif pour IoT).

## 8. Gestion des risques de sécurité

| Risque | Contre-mesure |
|---|---|
| Point d'accès pirate (rogue AP) | Détection WIPS, surveillance radio |
| Attaque par dictionnaire (PSK) | WPA3-Enterprise, certificats |
| Interception (evil twin) | Certificats serveur, validation mutuelle |
| Fuite de données (invités) | Isolation client + filtrage |

## 9. Validation (J6)

- Politique validée et signée par le RSSI ;
- Analyse de conformité RGPD validée ;
- Scénarios de test de sécurité intégrés au plan de recette (T-S1).
