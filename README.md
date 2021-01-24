# Esercitazione_03_Zaina
//Il codice professore:


#define LED_1 5
#define LED_2 6
#define LED_3 9
#define LED_4 3
#define P1 12
#define P2 13
#define DELAY 1000
int temperatura = 0;
void setup()
{
  pinMode(LED_1, OUTPUT);
  pinMode(LED_2, OUTPUT);
  pinMode(LED_3, OUTPUT);
  pinMode(LED_4, OUTPUT);
  pinMode(P1, INPUT);
  pinMode(P2, INPUT);
}

void loop()
{
  while(temperatura <= 255 && temperatura >= 0){
    do{
      int stato_pulsante = digitalRead(P1);
      if(stato_pulsante == 1){
        temperatura++;
      int stato_pulsante = digitalRead(P2);
      if(stato_pulsante == 1){
        temperatura--;
      }
    }while(temperatura >= 63);
  analogWrite(LED_1, 63);
    if(temperatura < 63)
      analogWrite(LED_1, 0);
    do{
      int stato_pulsante = digitalRead(P1);
      if(stato_pulsante == 1){
        temperatura++;
      int stato_pulsante = digitalRead(P2);
      if(stato_pulsante == 1){
        temperatura--;
      }
    }while(temperatura >= 127);
   analogWrite(LED_2, 127);
    if(temperatura < 127)
      analogWrite(LED_2, 0);
    do{
      int stato_pulsante = digitalRead(P1);
      if(stato_pulsante == 1){
        temperatura++;
      int stato_pulsante = digitalRead(P2);
      if(stato_pulsante == 1){
        temperatura--;
      }
    }while(temperatura >= 190);
   analogWrite(LED_3, 190);
    if(temperatura < 190)
      analogWrite(LED_3, 0);
    do{
      int stato_pulsante = digitalRead(P1);
      if(stato_pulsante == 1){
        temperatura++;
      int stato_pulsante = digitalRead(P2);
      if(stato_pulsante == 1){
        temperatura--;
      }
    }while(temperatura >= 255);
      analogWrite(LED_4, 255);
    if(temperatura < 255)
      analogWrite(LED_4, 0);
  }      
}

