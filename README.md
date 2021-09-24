# Readmefile
## Lämpömittari
### niko ja Daniel
![toucan-4185361_1920](https://user-images.githubusercontent.com/91183139/134325272-ba25a215-ef84-407e-8722-627107a25636.jpg)
  ![bird-6607863_1920](https://user-images.githubusercontent.com/91183139/134325617-a525e35e-a9d1-4118-b32a-ff88616bcbf5.jpg)
yritys | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
päivät |   |   |   |   |   |   |   |   |   |  | 


a | b
------------ | -------------
 1 | 2



yritys | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
komponetit |photon   |led p 8mm   | vastus 220ohm  |koekytkentä levy   |   |   |   |   |   |  | 
hinta  |28,90€   | 0,65€  | 0,25€  | 5,00€  |   |   |   |   |   |  | 


[powered by salpauksen hyvikset](https://www.salpaus.fi/opiskelija/)  

 idea oli saada vihreä keltainen ja punainen led valo palamaan yksi kerralaan tietyn aikaa.
 
 
```int led1 = D0; // Instead of writing D0 over and over again, we'll write led1
// You'll need to wire an LED to this one to see it blink.

int led2 = D1; 

int led3 = D2;


// Having declared these variables, let's move on to the setup function.
// The setup function is a standard part of any microcontroller program.
// It runs only once when the device boots up or is reset.

void setup() {

  // We are going to tell our device that D0 and D7 (which we named led1 and led2 respectively) are going to be output
  // (That means that we will be sending voltage to them, rather than monitoring voltage that comes from them)

  // It's important you do this here, inside the setup() function rather than outside it or in the loop function.

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

// Next we have the loop function, the other essential part of a microcontroller program.
// This routine gets repeated over and over, as quickly as possible and as many times as possible, after the setup function is called.
// Note: Code that blocks for too long (like more than 5 seconds), can make weird things happen (like dropping the network connection).  The built-in delay function shown below safely interleaves required background activity, so arbitrarily long delays can safely be done if you need them.

void loop() {
  // To blink the LED, first we'll turn it on...
  digitalWrite(led1, HIGH);
  digitalWrite(led2, LOW);
  digitalWrite(led3, LOW);

  // We'll leave it on for 1 second...
  delay(1000);

  // Then we'll turn it off...
 digitalWrite(led1, LOW);
  digitalWrite(led2, HIGH);
  digitalWrite(led3, LOW);


  // Wait 1 second...
  delay(1000);
  digitalWrite(led1, LOW);
  digitalWrite(led2, LOW);
  digitalWrite(led3, HIGH);
delay(1000);
  // And repeat!
}
```
