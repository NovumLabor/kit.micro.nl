---
layout: post
title:  "05 Photo Resistors"
date:   2014-06-20 20:16:18
categories: tutorial
hype: 05-photo-resistor-voltage-divider
codebender: 36525
parts:
    - sku:	    SEN-09088
      points:	A11 → A14


intro: |
  Nu heb je al kunnen spelen met een potentiometer, deze varieert de weerstand aan de hand van het draaien van een knop. In hetvolgende voorbeeld gebruik je een fotogevoelige weerstand, deze verandert ook de weerstand, alleen nu gekoppeld aan de hoeveelheid licht dat de sensor ontvangt. 

code_to_note: |

  Een variabele is de naam die je geeft aan een opgeslagen waarde. Voordat je dus een waarde kunt gebruiken moet je er een naam aankoppelen ofwel declareren. In de code is dat het Engelse woord: "declare". Bijvoorbeeld sensorValue, van het type "int" (integer). Let op de juiste spelling. Schrijf de variabele dus altijd precies zoals je hem hebt gedeclareerd. Inclusief het gebruik van kleine en hoofdletters! Net zoals je doet bij je voor en achternaam. 

      int sensorValue;

  We gebruiken de analogRead() functie om de waarde van een analoge pin uit te lezen. analogRead() takes one parameter, the analog pin you want to use ("sensorPin"), and returns a number ("sensorValue") between 0 (0 volts) and 1023 (5 volts).

      sensorValue = analogRead(sensorPin);

what_you_should_see: |
  Je ziet het lichtniveau als een waarde op het kleine scherm. 
  

toubleshooting: |
  **Werkt zo nu en dan**

  Zeer waarschijnlijk door slechte verbinding van de pootjes van de fotogevoelige weerstand. Probeer deze aan te drukken. 
  
---
## Pull Up weerstanden

Veel sensoren die je gebruikte (potentiometers, fotogevoelige weerstanden, enzovoort) zijn vermomde weerstanden. De weerstand ervan verandert gelijk aan wat de sensor meet, bijvoorbeeld het lichtniveau, de temperatuur of geluid. 

De MicroView's analoge input pinnen meten de spanning, en niet de weerstand. Maar we kunnen eenvoudig de spanning uitlezen doet de MicroView's interne pull up weerstanden.