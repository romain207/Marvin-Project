## 📋 Nos Tâches Principales

### Mouvements de base
- [X] Faire avancer, reculer et tourner le robot de manière précise.
- [ ] Programmer le suivi de la ligne au sol.

### Interaction avec les palets
- [ ] Détecter la présence d'un palet devant le robot.
- [ ] Ouvrir et fermer la pince pour attraper le palet.
- [ ] Sécuriser le palet pour le transporter.
- [ ] Déposer proprement le palet dans la zone d'arrivée.

### Communication et Repérage
- [ ] Recevoir la distance des palets envoyées par la caméra.
- [ ] Calculer le chemin pour se rendre jusqu'au palet ciblé.

## 🧠 Stratégie et Gestion des Imprévus

### Stratégie Générale:
- [ ] **Priorité de ramassage :** Quelle est notre stratégie principale ?
  > **Décision :** viser les palets les plus proches
- [ ] **Fin de mission :** Comment le robot sait-il qu'il a terminé sa mission ou que le temps est écoulé ?
  > **Décision :** fonction pour qu'il tourne le programme pendant 5 minutes

### Gestion des Adversaires et des Obstacles
- [ ] **Face-à-face :** Que doit faire le robot s'il se trouve bloqué juste devant un autre robot ?
  > **Décision :** 
- [ ] **Esquive :** Comment doit-il réagir de manière générale s'il détecte un autre robot sur son chemin (le contourner, attendre, reculer) ?
  > **Décision :** 
- [ ] **Palet volé :** Que faire s'il arrive à l'emplacement d'un palet, mais qu'un robot adverse vient de le prendre juste avant lui ?
  > **Décision :**

### Gestion des Erreurs de Manipulation
- [ ] **Capture ratée :** Que faire si la pince se ferme mais que le robot a raté le palet ?
  > **Décision :**
- [ ] **Perte en route :** Que doit faire le robot s'il fait tomber le palet pendant le trajet vers la zone de dépôt (l'abandonner, essayer de le reprendre) ?
  > **Décision :**
- [ ] **Perte de trajectoire :** Que se passe-t-il si le robot perd la ligne au sol pendant son déplacement ?
  > **Décision :**
