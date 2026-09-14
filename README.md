
# 🤖 Project PIX — Robot Autonome LEGO EV3

> **Module :** Introduction à l'Intelligence Artificielle et Robotique (6 ECTS)  
> **Établissement :** UFR de Mathématiques et Informatique — Université Grenoble Alpes  
> **Cadre :** Challenge PERSYCUP — Fablab  
> **Encadrant :** Damien Pellier  

---

## 📌 Présentation du Projet

**PIX** est un robot mobile autonome conçu à partir du kit **LEGO Mindstorms EV3** et programmé en **Java (leJOS)**. 

Son objectif principal est d'évoluer sur un terrain de $3\text{ m} \times 2\text{ m}$, de localiser des palets à l'aide d'un système de vision zénithale infrarouge, de les capturer grâce à une pince motorisée et de les rapporter dans la zone de dépôt en un minimum de temps.

---

## 🚀 Fonctionnalités Principales

* **📡 Communication Réseau UDP :** Écoute du flux broadcast (`192.168.1.255:8888`) pour recevoir en temps réel les coordonnées $(X, Y)$ des palets envoyées par la caméra IR zénithale.
* **🛣️ Suivi de Ligne (PID) :** Suivi fluide du réseau de lignes colorées au sol via un capteur de couleur/luminosité.
* **🧭 Navigation & Odométrie :** Recalage et déplacement du robot vers des positions cibles à partir des encodeurs de roues (moteurs tachymétriques).
* **🎯 Détection & Capture :** Détection fine d'obstacle/palet à moins de 8 cm via capteur à ultrasons et verrouillage automatique de la pince.
* **🤖 Machine à États (FSM) :** Contrôle autonome de la stratégie globale (Recherche → Déplacement → Approche → Capture → Dépôt).

---

