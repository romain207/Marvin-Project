```java
import lejos.hardware.lcd.LCD;
import lejos.hardware.port.SensorPort;
import lejos.hardware.sensor.EV3UltrasonicSensor;
import lejos.robotics.SampleProvider;

public class Perception {
	private EV3UltrasonicSensor detection; 
	private float [] tab;
	SampleProvider detec;
	// les ultarasons peuvent detecter d'autres ultrasons aux alentours
	// capteurs 4 c'est les couleurs
	// capteurs 1 c'est ultrasons
	// capteurs 2 c'est le tactile des qu'il tape sur le bouton rouge
	// capteurs ultrasons exemple objet à 34,5 cm

	public Perception() { 
		detection= new EV3UltrasonicSensor(SensorPort.S1);
		detec= detection.getDistanceMode(); // recupere la valeur
		tab = new float[detec.sampleSize()]; // le met dan sun tableau en fonction du nombre d'element a mettre (sampleSize)
	}
	
	public void allumer() {
		detection.enable();
	}
	
	public void mesurer() {
		detec.fetchSample(tab, 0); // mesure à un moment précis
		LCD.drawString(String.valueOf(tab[0]), 0, 4);
	}

public static void main(String[] args) {
Perception percept = new Perception();
		percept.allumer();
		percept.mesurer();
		Delay.msDelay(5000);

  		LCD.clear();
		LCD.drawString("Fin du test", 0, 4);
		Delay.msDelay(1000);
	}
}

```
