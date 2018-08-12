//BLuethoot-Lamp-for-aquarium
The project is based for the aquario's illuminaton. The lamp have two compartmens. The first compartmens hosts blu LED, red LED, whitw LED. The second compartmens hosts arduino nano with hc-06 and relè shield (8 relè)//
#include <SoftwareSerial.h>
SoftwareSerial bluetooth(10,11);
int A = 2;
int B = 3;
int C = 4;
int D = 5;
int E = 6;
int F = 7;
int G = 8;
int H = 9;
char DATO; 
void setup()  
{
  pinMode(A,OUTPUT);
  pinMode(B,OUTPUT);
  pinMode(C,OUTPUT);
  pinMode(D,OUTPUT);
  pinMode(E,OUTPUT);
  pinMode(F,OUTPUT);
  pinMode(G,OUTPUT); 
  pinMode(H,OUTPUT);
  digitalWrite(A,HIGH);
  digitalWrite(B,HIGH);
  digitalWrite(C,HIGH);
  digitalWrite(D,HIGH); 
  digitalWrite(E,HIGH);
  digitalWrite(F,HIGH); 
  digitalWrite(G,HIGH);
  digitalWrite(H,HIGH);
  bluetooth.begin(9600); 
  Serial.begin(9600);
}
void loop() 
{
  if (bluetooth.available()){
    DATO =(bluetooth.read());
      if (DATO == 'a')  
      {
        digitalWrite(A,LOW);
      }
      if (DATO == 'A')
      {
        digitalWrite(A,HIGH);
      }
      if (DATO == 'b')
      {
        digitalWrite(B,LOW);    
      }
      if (DATO == 'B')
      {
        digitalWrite(B,HIGH);
      }
      if (DATO == 'f')
      {
        digitalWrite(C,LOW);
      }
      if (DATO == 'F')
      {
        digitalWrite(C,HIGH);
      }
      if (DATO == 'g')
      {
        digitalWrite(D,LOW);    
      }
      if (DATO == 'G')
      {
        digitalWrite(D,HIGH);
      }
      if (DATO == 'h')
      {
        digitalWrite(E,LOW);
      }
      if (DATO == 'H')
      {
        digitalWrite(E,HIGH);
      }
      if (DATO == 'l')
      {
        digitalWrite(F,LOW);
      }
      if (DATO == 'L')
      {
        digitalWrite(F,HIGH);
      }
      if (DATO == 'm')
      {
        digitalWrite(G,LOW);
      }
      if (DATO == 'M')
      {
        digitalWrite(G,HIGH);
      }
      if (DATO == 'n')
      {
        digitalWrite(H,LOW);
      }
      if (DATO == 'N')
      {
        digitalWrite(H,HIGH);
      }
      if (DATO == 'T'){
        digitalWrite(A,LOW);
        digitalWrite(B,LOW);
        digitalWrite(C,LOW);
        digitalWrite(D,LOW);
        digitalWrite(E,LOW);
        digitalWrite(F,LOW);
        digitalWrite(G,LOW);
        digitalWrite(H,LOW);
      }
      if (DATO == 't'){
        digitalWrite(A,HIGH);
        digitalWrite(B,HIGH);
        digitalWrite(C,HIGH);
        digitalWrite(D,HIGH);
        digitalWrite(E,HIGH);
        digitalWrite(F,HIGH);
        digitalWrite(G,HIGH);
        digitalWrite(H,HIGH);
      }  
    }    
}
