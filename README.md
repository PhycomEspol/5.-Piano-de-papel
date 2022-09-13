# 5.-Piano-de-papel
#include <LiquidCrystal_I2C.h>

int pinBuzzer = 11;
int pinCancion = 9;
int Dosost= 10;

int Do = 2;
int Re = 3;
int Mi = 4;
int Fa = 5;
int Sol = 6;
int La = 7;
int Si = 8;

bool bandera=true;

LiquidCrystal_I2C lcd(0x27,16,2);
void cancion(){
  lcd.clear();
  lcd.print("SKY FULL STARS ");
  lcd.setCursor(3,1);
  lcd.print("COLDPLAY");
  tone(pinBuzzer, 370);
  delay(374);
  noTone(pinBuzzer);

  tone(pinBuzzer, 277);
  delay(374);
  noTone(pinBuzzer);

  tone(pinBuzzer, 233);
  delay(374);
  noTone(pinBuzzer);

  tone(pinBuzzer, 370);
  delay(374);
  noTone(pinBuzzer);

  tone(pinBuzzer, 277);
  delay(374);
  noTone(pinBuzzer);

  tone(pinBuzzer, 233);
  delay(374);
  noTone(pinBuzzer);

  tone(pinBuzzer, 370);
  delay(499);
  noTone(pinBuzzer);

  tone(pinBuzzer, 277);
  delay(499);
  noTone(pinBuzzer);

  tone(pinBuzzer, 233);
  delay(499);
  noTone(pinBuzzer);

  tone(pinBuzzer, 415);
  delay(499);
  noTone(pinBuzzer);

  tone(pinBuzzer, 277);
  delay(499);
  noTone(pinBuzzer);

  tone(pinBuzzer, 208);
  delay(499);
  noTone(pinBuzzer);

  
}
void setup() {
  // put your setup code here, to run once:
  for (int i = 2; i <=10 ; i++) {
    pinMode(i, INPUT_PULLUP);
  }
  //pinMode(pinLed, OUTPUT);
  pinMode(pinBuzzer, OUTPUT);
  lcd.init();
  lcd.backlight();
  lcd.print("PIANO DIGITAL");
  //lcd.clear();

}

void loop() {
  // put your main code here, to run repeatedly:
  while (digitalRead(Do) == LOW) {
    tone(pinBuzzer, 523, 100);
    //delay(1000);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical: Do");
  }
  while (digitalRead(Re) == LOW) {
    tone(pinBuzzer, 588, 100);
    //delay(1000);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical: Re");
  }
  while (digitalRead(Mi) == LOW) {
    tone(pinBuzzer, 659, 100);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical: Mi");    
  }
  while (digitalRead(Fa) == LOW) {
    tone(pinBuzzer, 698, 100);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical: Fa");
  }
  while (digitalRead(Sol) == LOW) {
    tone(pinBuzzer, 784, 100);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical:Sol");
  }
  while (digitalRead(La) == LOW) {
    tone(pinBuzzer, 880, 100);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical: La");
  }
  while (digitalRead(Si) == LOW) {
    tone(pinBuzzer, 988, 100);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical: La");
  }
  
  if(digitalRead(pinCancion)==LOW){
    cancion();
  }
 
  while (digitalRead(Dosost) == LOW) {
    tone(pinBuzzer, 262, 100);
    //digitalWrite(pinLed, HIGH);
    lcd.clear();
    lcd.print("Nota Musical: Do");
    lcd.setCursor(4,1);
    lcd.print("Sostenido");

  }
 

  
}
