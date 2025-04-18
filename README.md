// Pin Definitions
const int windSpeedPin = 2;     // Digital input from anemometer
const int rpmSensorPin = 3;     // Digital input from Hall Effect sensor
const int voltagePin = A0;      // Analog input for voltage monitoring

// Variables
volatile int windPulses = 0;
volatile int rpmPulses = 0;

unsigned long lastWindTime = 0;
unsigned long lastRPMTime = 0;
float windSpeed = 0.0;
float turbineRPM = 0.0;
float voltage = 0.0;

// Constants
const float windConversionFactor = 2.4; // Depends on anemometer specs
const float voltageDividerRatio = 5.
