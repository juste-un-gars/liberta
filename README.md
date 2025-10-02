# Liberta

**Liberta** est un navigateur web open source, sécurisé, léger, compartimenté, et indépendant de Chromium. Il est conçu pour offrir à l'utilisateur un contrôle total sur sa vie numérique, sans dépendance à Google ni à des serveurs tiers.

---

## 🎯 Objectifs

- Navigateur **modulaire et souverain**
- **Compartimentation par site** façon Docker
- **Sécurité renforcée** et permissions explicites
- **Multilingue** (anglais, français, espagnol, allemand)
- **Synchronisation sans serveur**
- **Mise à jour automatique** via GitHub Releases

---

## 🧱 Architecture

- **Langage principal** : Rust
- **Moteur de rendu** : Servo ou Ladybird
- **Interface graphique** : Tauri, egui ou GTK
- **Stockage cloisonné** : chaque site a son propre espace (cookies, cache, localStorage)
- **Sandboxing** : chaque site fonctionne dans un conteneur isolé
- **Permissions** : micro, caméra, localisation, lecture vidéo, clipboard, etc.

---

## 🔐 Sécurité

- Isolation stricte entre domaines
- Aucun accès au système sans consentement
- Pas de télémétrie ni de dépendance à des services tiers
- Chiffrement local des données sensibles
- IA embarquée pour analyse comportementale des scripts

---

## 🎬 Fonctionnalités

- **Blocage automatique des vidéos** sur les pages web
- **Bouton d’autorisations** en haut à gauche de la barre d’adresse (remplace le logo Chrome)
- **Profils de navigation** :
  - Lecture seule
  - Authentifié
  - Créatif
  - Risqué

---

## 🌍 Multilingue

- Langues supportées : anglais, français, espagnol, allemand
- Traductions stockées dans des fichiers JSON :
