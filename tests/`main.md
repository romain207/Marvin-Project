``` java

import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;
import lejos.hardware.lcd.LCD;
import lejos.utility.Delay;

public class Pixou {


	public static void main(String[] args) throws IOException {
		// Affiche un texte sur l'écran
		//LCD.drawString("Je suis Pix!", 0, 4);

		// Allume la LED en vert et fait un bip
		//Button.LEDPattern(1); 
		//Sound.beep();
		
		Mouvements mouvR = new Mouvements();
		Perception percept = new Perception();
		BufferedWriter f= new BufferedWriter (new FileWriter("Relevés.txt",true));
 
		//Perception percept1 = new Perception();
		//percept1.mesureContinu(mouvR,percept);
		//percept.allumer();
		//percept.mesurer();
		//Delay.msDelay(5000);
		percept.allumer();
		int i=0;
		mouvR.tournerCompletD();
		while (mouvR.estEnMouvement()) {
			float distance =percept.mesurer();
			f.write(String.valueOf(distance));
			f.newLine();
			i++;
			Delay.msDelay(50);
		}
		f.close();
		
		mouvR.arret();
	
	
		
		
		
		// Pause de 5 secondes pour lire l'écran
		//Delay.msDelay(5000);

		//Port left_port = MotorPort.B;
		//Port right_port= MotorPort.C;
		//testProf mouvR = new testProf(left_port, right_port);
		//mouvR.forward();
		//Delay.msDelay(216); 
		//mouvR.rotateClockwise();
		
		//Mouvements mouvR = new Mouvements();
		//MouvPince mouvP = new MouvPince();
		
		//mouvR.tournerAgauche();
		//Delay.msDelay(1000); 
		//mouvR.arret(); // on fait une pause dans le programme pour que le robot puisse avancer
		//mouv.tournerAgauche();
		//mouvP.ouvrirPince();
		//mouvP.fermerPince();
		//mouvR.avancer();
		//mouvP.stop();
		/*
		 * mouv.reculer(); Delay.msDelay(5000); mouv.tournerAdroite(); mouv.avancer();
		 * Delay.msDelay(5000); mouv.arret();
		 */

		// Nettoie l'écran avant de quitter
		LCD.clear();
		//LCD.drawString("Fin du test", 0, 4);
		Delay.msDelay(1000);
	}
	
}

```

