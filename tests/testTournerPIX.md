```java
// Test pour faire tourner PIX sur lui-même

import lejos.hardware.motor.EV3LargeRegulatedMotor;
import lejos.hardware.port.MotorPort;

public class Tourner {

// déclaration attributs représentant les deux roues
	private EV3LargeRegulatedMotor roueG;
	private EV3LargeRegulatedMotor roueD;

	// initialisation des attributs dans le constructeur
	public Tourner() {
		roueG= new EV3LargeRegulatedMotor(MotorPort.B);
		roueD= new EV3LargeRegulatedMotor(MotorPort.C); 
	}

// methode pour avancer
public void avancer() {
		roueG.setSpeed(200); // vitesse du moteur
		roueD.setSpeed(200);
		roueG.forward(); // je dis à mes roues d'avancer
		roueD.forward(); 
	}

// methode pour reculer
public void reculer() {
		roueG.setSpeed(200);
		roueD.setSpeed(200);
		roueG.backward(); 
		roueD.backward();
	}

public void arret() {
		roueG.stop();
		roueD.stop();
	}

// méthode pour tourner à droite
public void tournerAdroite() {
		roueG.rotate(840, true); 
		roueD.rotate(-840);
	}

// méthode pour tourner à gauche
public void tournerAgauche() {
		roueG.rotate(-840, true); 
		roueD.rotate(840);
	}

public static void main(String[] args) {

Tourner mouv = new Tourner();
mouv.tournerAgauche();
	}
}
```
