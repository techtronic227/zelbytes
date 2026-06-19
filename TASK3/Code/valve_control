const uint8_t BTN_MANUAL = 2;
const uint8_t LED_STATUS = 13;
const uint8_t RELAY_VALVE = 8;

const bool RELAY_ACTIVE_LOW = true;

unsigned long lastEventMs = 0;
unsigned long releaseTime = 0;
bool valveState = false;

bool debouncePressed(uint8_t pin) {
  static bool lastStable = HIGH;
  static bool lastRead = HIGH;
  static unsigned long lastChange = 0;

  bool reading = digitalRead(pin);

  if (reading != lastRead) {
    lastChange = millis();
    lastRead = reading;
  }

  if ((millis() - lastChange) > 50) {
    lastStable = reading;
  }

  return (lastStable == LOW);
}

void setValve(bool open) {
  if (RELAY_ACTIVE_LOW) {
    digitalWrite(RELAY_VALVE, open ? LOW : HIGH);
  } else {
    digitalWrite(RELAY_VALVE, open ? HIGH : LOW);
  }
}

void setup() {
  pinMode(BTN_MANUAL, INPUT_PULLUP);
  pinMode(LED_STATUS, OUTPUT);
  pinMode(RELAY_VALVE, OUTPUT);

  setValve(false);

  Serial.begin(9600);

  Serial.println(F("Manual Irrigation Ready"));
  Serial.println(F("Commands: s=status, e=ESTOP"));
}

void loop() {
  bool pressed = debouncePressed(BTN_MANUAL);

  if (pressed) {
    valveState = true;
    releaseTime = millis();
    lastEventMs = millis();
  }

  if (valveState && !pressed && (millis() - releaseTime >= 5000)) {
    valveState = false;
  }

  setValve(valveState);
  digitalWrite(LED_STATUS, valveState ? HIGH : LOW);

  if (Serial.available()) {
    char c = Serial.read();

    if (c == 's') {
      Serial.print(F("Valve="));
      Serial.println(valveState ? F("OPEN") : F("CLOSED"));

      Serial.print(F("UptimeMs="));
      Serial.println(millis());

      Serial.print(F("LastEventMs="));
      Serial.println(lastEventMs);
    }

    if (c == 'e') {
      valveState = false;
      setValve(false);
      digitalWrite(LED_STATUS, LOW);
      Serial.println(F("ESTOP"));
    }
  }
}
