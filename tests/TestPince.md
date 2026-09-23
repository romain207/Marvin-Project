```java
// Test pas encore bien opérationnel pour attraper un palet 

import lejos.hardware.motor.EV3MediumRegulatedMotor;
import lejos.hardware.port.MotorPort;

public class MouvPince extends java.lang.Object { 
	private EV3MediumRegulatedMotor pince;
	
	public MouvPince () {
		pince= new EV3MediumRegulatedMotor(MotorPort.A);
	}
	
	public void ouvrirPince() {
		pince.setSpeed(500);
		pince.rotate(1650); 
	}
	
	public void fermerPince() {
		pince.setSpeed(500);
		pince.rotate(-1650); 
	}
	
	public void stop() {
		pince.stop();       
		
	}
public static void main(String[] args) {
Mouvements mouvR = new Mouvements();
		MouvPince mouvP = new MouvPince();
		
		mouvR.avancer();
		Delay.msDelay(216); 
		//mouv.arret();// on fait une pause dans le programme pour que le robot puisse avancer
		//mouv.tournerAgauche();
		mouvP.ouvrirPince();
		mouvP.fermerPince();
		mouvP.stop();
}

}
```

