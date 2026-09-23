```java
// Test incomplet pour attraper un palet 

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

}
```

