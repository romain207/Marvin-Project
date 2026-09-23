⁶## Semaine 1
Présentation de Pix et première configuration

## Semaine 2
Configuration terminée, lancement de petits programmes pour tester

**Observations :**
- Pix a peut etre une vitesse max: autour de 700 ou moins
- Une seule roue fonctionne lors de la rotation ??
- Soucis pour fermer la pince au max: résolu la vitesse du petit moteur a une plus grosse limite que celle du grand moteur

## Semaine 3
Centralisation des documents internes présents sur les autres branches dans le main :
branches "cahier-des-charges" et "cahier-de-bord" (supprimées suite au regroupement).
- Observations du jour: angle de rotation de PIX: tour complet: angle 840° (en degrès de PIX )
- découverte de nouvelles stratégies pour récupérer au plus vite les premiers palets, particulièrement le premier (mise en place d'un circuit prédéfini pour les premiers palets)
- capteurs ultrasons: fonctionne et renvoie une série de valeur
- capteur lumière: reconnait les couleurs du terrain (rouge, jaune, vert, blanc, noir, bleu)
- les pinces: problème de fermeture (pour l'instant)
- modification de Github (réorganisation des dossiers)
- on estime que PIX parcours 55.5 cm en 1 seconde (mesure imprécise, la vitesse de PIX est mesuré en (°/s)il faudra effectuer de nouvelle mesure et convertir pour obtenir des (cm/s)(La formule de conversion est :Vitesse(cm/s)=Vitesse angulaire(°/s)*(pi/180)*Rayon(cm))).
- 1ère réussite de saisie de palet de PIX , on observe cependant des complications(vélocité mal géré et interprété , décalage par rapport à un axe donné du aux frottements des roues) lorsque l'on essaye à plus grande vitesse aussi bien pour les pinces que pour les roues.
