# ESP32_2-2562


![ScreenShot](https://github.com/worrajak/ESP32_2-2562/blob/master/images.jpeg?raw=true)

ESP32 pinout 

```
struct Button {
  const uint8_t PIN;
  uint32_t numberKeyPresses;
  bool pressed;
};

Button button1 = {14, 0, false};

void IRAM_ATTR isr() {
  button1.numberKeyPresses += 1;
  button1.pressed = true;
}

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(115200);
  pinMode(button1.PIN, INPUT_PULLUP);
  pinMode(13, OUTPUT);
  attachInterrupt(button1.PIN, isr, FALLING);
}

boolean toggle = false;

// the loop function runs over and over again forever
void loop() {
  if (button1.pressed) {
      Serial.printf("Button 1 has been pressed %u times\n", button1.numberKeyPresses);
      button1.pressed = false;
      toggle = !toggle;
      digitalWrite(13,toggle);
  }
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}

```
