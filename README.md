# TP_commande : Quentin ROLLAND et Cheyenne PEREZ 

**1ère séance** : GIT + tp jusqu'à "Console UART"

**2ème séance** : 6.1 et 6.2 fait + changement de alpha avec le shell, début de la commande start avec GPIO

**3ème séance** : 6.3 commande start fait avec le shell et le blue button (les 2 fonctionnent)
	6.4 Premiers tests avec le moteur : rapport cylique à 50 à chaque lancement. PB : pic de courant lorsque 
	l'on change le rapport cyclique (s'il y a un trop gros écart)
	6.5 Définition de la vitesse : fait avec l'UART (ajout de la condition si alpha est supérieur à 100)
	7.1 Commande de l'ADC entamée : initialisation de l'ADC, DMA et Timer 2, création de la commande dans 
	le shell. Pour l'instant le retour de la mesure retourne 0. Il faudra vérifier la cohérence de la valeur
	récupérée dans le buffer par le DMA et vérifier que le shell envoie bien la bonne valeur.

**4ème séance** : 7.1 terminé, nous avons réussi à avoir une bonne valeur du courant en sortie du moteur (vérifiée 
	à l'oscillo) 

**5ème séance** : début encodeur (activation du timer4 et ecriture des fonctions pour calculer la vitesse).
	La valeur de vitesse qui nous est renvoyée est de 0tr/min. Le pb est que l'on ne rentre pas dans la fonction
	callback qui appelle le timer3 donc ne modifie pas la variable vitesse puisque le compteur n'est pas lancé.
	
**6ème séance** : Correction du code de l'encodeur. Il fallait mettre les sorties de l'encodeur, A et B, dans le bon
	sens. Il est maintenant opérationnel. Nous avons également réalisé le code pour l'asservissement 
	en courant.

