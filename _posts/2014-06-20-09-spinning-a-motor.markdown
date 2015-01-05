---
layout: post
title:  "09 Spinning a Motor"
date:   2014-06-20 20:16:18
categories: tutorial
hype: 10-motor
codebender: 36529
parts:
    - sku:	    COM-08377
      points:	  G15 → E15

    - sku:      COM-12852
      points:   A14, A15, A16

    - sku:      COM-08588
      points:   C24 → C28

    - sku:      ROB-11696
      points:   D24 → D28

    - sku:      RED-JUMPER
      points:   J8 → W10

    - sku:      RED-JUMPER
      points:   A24 → W25

    - sku:      BLUE-JUMPER
      points:   I11 → I15

    - sku:      YELLOW-JUMPER
      points:   B16 → B28

intro: |
  Hiervoor heb je geoefend met de servo motor. Nu gaan we aan de slag met het draaien van een motor. Hiervoor heb je een transistor nodig, deze schakelt de MicroView over naar een hogere stroom dan dat het zelf kan leveren. Als je een transistor gebruikt moet je zeker zijn dat je voldoet aan de maximale specificaties. De transistor die we gebruiken in dit circuit kan maximaal 40 volt aan en 200 milliamperes – prima voor het speelgoed motortje! Als de motor ronddraait en plotseling uit wordt gezet, zal het magnetische veld in de motor uitvallen. Dit veroorzaakt een spanningspiek en kan de transistor beschadigen. Om dit te voorkomen gebruiken we een "flyback diode", deze leidt de spanningspiek om de transistor.


what_you_should_see: |
  De gelijkspanningsmotor ofwel DC Motor zal draaien als je hem goed hebt aangesloten. Loop anders de configuratie op het board na en kijk of je het programma die hoort bij deze oefening hebt geladen. 

code_to_note: |

  In de code wordt het commando `setPwmFrequency(motorPIN,1)` gebruikt om de functie (een klein programmaatje) aan te roepen die de PWM frequentie instelt. Pulsbreedtemodulatie is in het Engels: Pulse Width Modulation, ofwel PWM. Dit is een technische methode om analoge uitkomsten te krijgen via digitale informatieoverdracht. 

  De `setPwmFrequency` functie is gedefinieert op regel 25. 

      void setPwmFrequency(int pin, int divisor){
        ...
      }
  



toubleshooting: |
  **USB Port levert niet voldoende stroom of stottert?**

  Sommige USB porten leveren niet voldoende stroom om een motor aan te sturen. Als dat bij jouw het geval is, test met een andere USB port of gebruik een externe voeding via batterijen. Checkout <a href="/powering-motor-with-batteries.html">this circuit</a> voor het aansluiten van batterijen.

  **Motor draait niet**

  Probeer een andere transistor. Wel gelijk aan de specificaties: P2N2222AG.  
  
  **Nog steeds geen resultaat**

  Kijk of je motor uberhaupt wel werkt door hem direct op 5 volt aan te sluiten.

  **Het werkt echt niet**
  Misschien is de MicroView niet verbonden met de computer. Probeer eens door de kabel eruit te halen en opnieuw in de USB port aan te sluiten. 

---
