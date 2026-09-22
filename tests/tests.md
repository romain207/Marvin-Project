```java
Test pour faire tourner PIX sur lui-même

import lejos.hardware.motor.EV3LargeRegulatedMotor;
import lejos.hardware.port.MotorPort;

public class Tourner {

// déclaration attributs représentant les deux roues
	private EV3LargeRegulatedMotor roueG;
	private EV3LargeRegulatedMotor roueD;

	// initialisation des attributs dans le constructeur
	public Mouvements() {
		roueG= new EV3LargeRegulatedMotor(MotorPort.B);
		roueD= new EV3LargeRegulatedMotor(MotorPort.C); 
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
}

public static void main(String[] args) {

Mouvements mouv = new Mouvements();
mouv.tournerAgauche();
}
}
```
