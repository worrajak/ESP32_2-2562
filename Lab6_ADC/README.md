Other Useful Functions
There are other more advanced functions to use with the ADC pins that can be useful in other projects.

- analogReadResolution(resolution): set the sample bits and resolution. It can be a value between 9 (0 – 511) and 12 bits (0 – 4095). Default is 12-bit resolution.
- analogSetWidth(width): set the sample bits and resolution. It can be a value between 9 (0 – 511) and 12 bits (0 – 4095). Default is 12-bit resolution.
- analogSetCycles(cycles): set the number of cycles per sample. Default is 8. Range: 1 to 255.
- analogSetSamples(samples): set the number of samples in the range. Default is 1 sample. It has an effect of increasing sensitivity.
- analogSetClockDiv(attenuation): set the divider for the ADC clock. Default is 1. Range: 1 to 255.
- analogSetAttenuation(attenuation): sets the input attenuation for all ADC pins. Default is ADC_11db. Accepted values:
  - ADC_0db: sets no attenuation (1V input = ADC reading of 1088).
  - ADC_2_5db: sets an attenuation of 1.34 (1V input = ADC reading of 2086).
  - ADC_6db: sets an attenuation of 1.5 (1V input = ADC reading of 2975).
  - ADC_11db: sets an attenuation of 3.6 (1V input = ADC reading of 3959).
- analogSetPinAttenuation(pin, attenuation): sets the input attenuation for the specified pin. The default is ADC_11db. Attenuation values are the same from previous function.
- adcAttachPin(pin): Attach a pin to ADC (also clears any other analog mode that could be on). Returns TRUE or FALSE result.
- adcStart(pin), adcBusy(pin) and resultadcEnd(pin): starts an ADC convertion on attached pin’s bus. Check if conversion on the pin’s ADC bus is currently running (returns TRUE or FALSE). Get the result of the conversion: returns 16-bit integer.

Code
```
// Potentiometer is connected to GPIO 34 (Analog ADC1_CH6) 
const int potPin = 34;

// variable for storing the potentiometer value
int potValue = 0;

void setup() {
  Serial.begin(115200);
  delay(1000);
}

void loop() {
  // Reading potentiometer value
  potValue = analogRead(potPin);
  Serial.println(potValue);
  delay(500);
}

```
