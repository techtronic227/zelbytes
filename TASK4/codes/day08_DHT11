#include <DHT.h>
#define DHT_PIN 4
#define DHT_TYPE DHT11
DHT dht(DHT_PIN, DHT_TYPE);
unsigned long lastRead = 0;

void setup() {
  Serial.begin(9600);
  dht.begin();
  Serial.println(F("ms,temp_c,humidity_pct"));
}

void loop() {
  if (millis() - lastRead < 2000) return;
  lastRead = millis();
  float h = dht.readHumidity();
  float t = dht.readTemperature();
  if (isnan(h) || isnan(t)) {
    Serial.println(F("ERR,NaN,NaN"));
    return;
  }
  Serial.print(lastRead); Serial.print(',');
  Serial.print(t, 1); Serial.print(',');
  Serial.println(h, 1);
}
