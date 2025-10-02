🌐 Liberta – Navigateur web open source et souverain

Liberta est un navigateur open source, sécurisé, léger, et indépendant de Chromium.
Son objectif est de redonner le contrôle total à l’utilisateur sur sa vie numérique : pas de Google, pas de télémétrie cachée, pas de dépendance à des serveurs tiers.

🎯 Objectifs

Navigateur modulaire et souverain → architecture ouverte, choix transparents, pas d’API opaque.

Compartimentation par site (style Docker) → chaque site fonctionne dans un processus isolé, avec stockage dédié (cookies, cache, localStorage).

Sécurité renforcée et permissions explicites → aucun accès au micro, caméra, clipboard ou fichiers sans consentement explicite.

Multilingue → anglais, français, espagnol, allemand dès la v1.

Synchronisation sans serveur → export/import chiffré, support futur du pair-à-pair (ex : CRDT, Syncthing).

Mises à jour fiables → d’abord via GitHub Releases, puis prévoir un miroir auto-hébergé.

👉 À faire :
Commence simple (rendu, JS, sandbox minimal) puis ajoute ces objectifs au fur et à mesure.

🧱 Architecture

Langage principal : Rust (sécurité mémoire, async performant).

Moteur de rendu HTML/CSS : Servo (expérimental mais Rust natif) ou Ladybird (projet jeune mais actif).

Plan B recommandé : WebKitGTK, plus mature.

Moteur JavaScript : SpiderMonkey (Firefox) ou QuickJS (léger mais moins compatible).

UI : Tauri ou egui (léger, multiplateforme). GTK comme solution plus stable.

Réseau : Hyper + QUIC/HTTP3 (Rust natif).

Sandboxing : isolation par process, namespaces Linux, seccomp (pas besoin de Docker).

Stockage cloisonné : chaque site = son propre répertoire chiffré.

👉 À faire :
Choisir un moteur de rendu + un moteur JS pour le MVP. Le reste peut venir après.

🔐 Sécurité

Isolation stricte entre domaines (un site ne peut pas lire les cookies d’un autre).

Permissions explicites via une interface claire (caméra, micro, clipboard, etc.).

Pas de télémétrie ni de services tiers.

Chiffrement local pour mots de passe et cookies sensibles.

Analyse de scripts via heuristiques (type NoScript intelligent).

L’IA peut venir plus tard : commence par un moteur de règles simples.

👉 À faire :
Implémenter d’abord une UI permissions claire (genre cadenas en barre d’adresse), puis un blocage par défaut du JS non sûr.

🎬 Fonctionnalités

Blocage automatique des vidéos autoplay.

Bouton d’autorisations en haut à gauche de la barre d’adresse.

Profils de navigation :

Lecture seule → pas de JS ni cookies persistants

Authentifié → cookies/session normaux

Créatif → accès médias et clipboard autorisés

Risqué → tout activé, pour sites non fiables

👉 À faire :
Les profils peuvent être un mode de navigation simple au début (Lecture seule vs Authentifié). Ajoute les autres ensuite.

🌍 Multilingue

Langues supportées : anglais, français, espagnol, allemand.

Traductions stockées dans des fichiers JSON pour permettre la contribution communautaire.

👉 À faire :
Préparer la structure i18n dès le départ (fichiers JSON séparés).

📌 Roadmap MVP réaliste

Phase 1 – Prototype minimal

Rendu HTML + CSS (Servo/Ladybird/WebKitGTK)

Moteur JS basique (QuickJS pour commencer)

Ouverture d’une page web statique

UI simple (adresse + bouton reload)

Phase 2 – Cloisonnement et sécurité

Processus isolés par domaine

Stockage séparé par site

Permissions explicites (caméra, micro, clipboard)

Phase 3 – UX et confort

Profils de navigation

Blocage vidéos autoplay

Interface multilingue

Phase 4 – Avancé

Synchronisation sans serveur

Analyse de scripts

Mises à jour décentralisées
