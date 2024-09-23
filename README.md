
Ejercicio 1
// Definir los pines a los que están conectados los LEDs
const int ledPins[] = {2, 3, 4, 5, 6}; // Pines digitales 2 a 6

void setup() {
  // Configurar los pines de los LEDs como salidas
  for (int i = 0; i < 5; i++) {
    pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {
  // Encender todos los LEDs
  for (int i = 0; i < 5; i++) {
    digitalWrite(ledPins[i], HIGH);  // Encender el LED
  }
  delay(1000);  // Mantener los LEDs encendidos por 1 segundo

  // Apagar todos los LEDs
  for (int i = 0; i < 5; i++) {
    digitalWrite(ledPins[i], LOW);   // Apagar el LED
  }
  delay(1000);  // Mantener los LEDs apagados por 1 segundo
}





Ejercicio 2

// Definir los pines a los que están conectados los LEDs
const int ledPins[] = {5, 6, 7, 8}; // Pines digitales 5 a 8

void setup() {
  // Configurar los pines de los LEDs como salidas
  for (int i = 0; i < 4; i++) {
    pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {
  // Encender los LEDs secuencialmente
  for (int i = 0; i < 4; i++) {
    digitalWrite(ledPins[i], HIGH);  // Encender el LED
    delay(200);                      // Esperar 200 milisegundos
  }

  // Apagar los LEDs secuencialmente
  for (int i = 0; i < 4; i++) {
    digitalWrite(ledPins[i], LOW);   // Apagar el LED
    delay(200);                      // Esperar 200 milisegundos
  }

  // Encender y apagar los LEDs en los pines 5 y 8 simultáneamente
  digitalWrite(ledPins[0], HIGH);  // Encender LED en pin 5
  digitalWrite(ledPins[3], HIGH);  // Encender LED en pin 8
  delay(200);                      // Mantener encendidos por 200 milisegundos

  digitalWrite(ledPins[0], LOW);   // Apagar LED en pin 5
  digitalWrite(ledPins[3], LOW);   // Apagar LED en pin 8
  delay(200);                      // Mantener apagados por 200 milisegundos
}


Ejercicio 3 


// Pines para los LEDs del semáforo
int ledRojo = 2;
int ledAmarillo = 3;
int ledVerde = 4;

void setup() {
    // Configurar los pines del semáforo como salida
    pinMode(ledRojo, OUTPUT);
    pinMode(ledAmarillo, OUTPUT);
    pinMode(ledVerde, OUTPUT);
}

void loop() {
    // Fase 1: Rojo encendido, Amarillo apagado, Verde encendido
    digitalWrite(ledRojo, HIGH);      // Encender LED rojo
    digitalWrite(ledAmarillo, LOW);   // Apagar LED amarillo
    digitalWrite(ledVerde, HIGH);     // Encender LED verde
    delay(1000);  // Esperar 1 segundo

    // Fase 2: Rojo apagado, Amarillo encendido, Verde apagado
    digitalWrite(ledRojo, LOW);       // Apagar LED rojo
    digitalWrite(ledAmarillo, HIGH);  // Encender LED amarillo
    digitalWrite(ledVerde, LOW);      // Apagar LED verde
    delay(1000);  // Esperar 1 segundo

    // Repetir la secuencia
}
