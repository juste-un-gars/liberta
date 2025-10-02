🌐 Liberta – Navigateur web open source et souverain

Liberta est un navigateur web open source, sécurisé, léger, et indépendant de Chromium.
Son but est de redonner le contrôle total à l’utilisateur sur sa navigation : pas de Google, pas de télémétrie, pas de dépendance à des serveurs tiers.

🎯 Objectifs

Navigateur modulaire et souverain

Isolation par site (chaque domaine fonctionne dans un conteneur/processus séparé)

Sécurité renforcée et permissions explicites

Multilingue (anglais, français, espagnol, allemand)

Synchronisation sans serveur (export/import chiffré, pair-à-pair à terme)

Mises à jour fiables (GitHub Releases + miroirs)

🧱 Architecture

Langage principal : Rust

Moteur de rendu HTML/CSS : Servo ou Ladybird (plan B : WebKitGTK)

Moteur JavaScript : QuickJS (léger) ou SpiderMonkey (compatible)

UI : Tauri ou egui (léger et multiplateforme)

Réseau : Hyper + support HTTP/3 et QUIC

Sandboxing : isolation par process, namespaces Linux, seccomp

Stockage cloisonné : cookies, cache et localStorage isolés par site

🔐 Sécurité

Isolation stricte entre domaines

Pas de télémétrie ni dépendances externes

Chiffrement local des données sensibles

Permissions explicites pour micro, caméra, clipboard, fichiers, etc.

🎬 Fonctionnalités

Blocage automatique des vidéos autoplay

Bouton autorisations en barre d’adresse (remplace le cadenas Chrome/Firefox)

Profils de navigation :

Lecture seule (pas de JS ni cookies persistants)

Authentifié (sessions normales)

Créatif (accès clipboard, médias, stockage local étendu)

Risqué (tout activé, sites non fiables)

🌍 Multilingue

Anglais, français, espagnol, allemand

Traductions dans des fichiers JSON (extensible par la communauté)

🚀 Roadmap MVP

Prototype minimal : rendu HTML/CSS + moteur JS basique + UI simple

Cloisonnement : processus isolés + stockage séparé

Sécurité : gestion des permissions explicites

Confort utilisateur : profils, blocage vidéos, multilingue

Fonctionnalités avancées : synchro sans serveur, mises à jour décentralisées
