---
layout: post
title:  "02 Potentiometer"
date:   2014-06-20 20:16:18
categories: tutorial
hype: 02-potentiometer
codebender: 36522
parts:
    - sku:	    COM-09806
      points:	E18, E19 and E20

    - sku:      BLACK-JUMPER
      points: B14 → B18

    - sku:      BLUE-JUMPER
      points: A12 → A19
    
    - sku:      RED-JUMPER
      points: J8 → B20

intro: |
  In dit circuit werk je met een potentiometer, ook potmeter genoemd. Een potentiometer is een variable weerstand. De buitenste pinnen zijn verbonden met 5 volt, de middelste pin geeft een output tussen 0 and 5, afhankelijk van de positie van de draaiknop bovenop de potentiometer. Een potentiometer is een ideaal voorbeeld van een variabele spanning verdelingscircuit. De spanning is proportioneel verdeeld over de weerstand tussen de middelste pin en de aarde pin. In dit circuit leer je hoe je een potentiometer gebruiken en de waarde weer te geven op het scherm van de MicroView.
  
code_to_note: |

  Een “variabele” is een opgeslagen waarde waaraan je een naam hebt gegeven. Je zult eerst een variabele moeten opgeven, ofwel "declareren" voordat je deze kunt gebruiken. In deze oefening declareer je een variabele met de naam sensorValue, van het type "int" (integer). Let op het gebruik van kleine en hoofdletters!

      int sensorValue;

  We gebruiken de analogRead() functie voor het uitlezen van de waarde van de analoge pin. analogRead() gebruikt slechts een parameter, de analoge pin die je gebruikt ("sensorPin"), geeft een waarde terug ("sensorValue") tussen de 0 (0 volt) en 1023 (5 volt).

      sensorValue = analogRead(sensorPin);

what_you_should_see: |
  Door het draaien aan de knop van de potentiometer zie je op het scherm van de MicroView twee verschillende widget stijlen. Deze komen overeen met de waarde uitgelezen van de potentiometer.

toubleshooting: |
  **Sporadically Working**

  Zeer waarschijnlijk door de aansluiting van de pinnen van de potentiometer. Meestal opgelost door de potentiometer aan te drukken.  
  
  **Not working?**

  Let op dat je de potentiometer pin NIET aan de digitale pin 0 hebt aangesluiten. De juiste pin is de analoge pin, de rij onder de voeding.

---
## Digitaal versus Analoog

De MicroView heeft twee type pinnen, "DIGITALE" pinnen en "ANALOGE" pinnen. Wat is het verschil?


De meeste componenten die je aansluit, zoals LEDs en drukknoppen, hebben slecht twee standen: aan en uit, of zoals de MicroView het ziet, hoog: "HIGH" (5 volt) en laag: "LOW" (0 volt). De digitale pinnen op een MicroView zijn uitstekend om de signalen van en naar de buitenwereld te herkennen en sturen. Ze kunnen zelfs wat trucjes, zoals het dimmen nabootsen (door erg snel te knipperen) en seriele communicatie (versturen en ontvangen van gegevens van een ander apparaat door encoderen via hoog en laag patronen). 

<img src="/assets/digital_example.svg" style="width:100%" />

Echter zijn er ook veel dingen die niet werken met slechts aan en uit signalen. Het meten van de temperatuur, volumeknoppen, etc. hebben een continue bereik van waardes tussen hoog en laag. Voor deze situatiea heeft de MicroView vijf analoge ingangen die de spanningswaarde vertaald in een waarde tussen 0 (0 volt) en 1023 (5 volt). De analoge pinnen zijn dus perfect voor het meten van dingen uit je directe omgeving.  

<img src="/assets/analog_example.svg" style="width:100%" />


