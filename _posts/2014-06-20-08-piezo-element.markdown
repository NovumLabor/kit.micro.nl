---
layout: post
title:  "08 Piezo Element"
date:   2014-06-20 20:16:18
categories: tutorial
hype: 09-piezo
codebender: 36528
parts:
    - sku: COM-07950
      points:	E20 → E23

    - sku: BLACK-JUMPER
      points: A14 → A23

    - sku: RED-JUMPER
      points: B13 → B20

intro: |
  In deze oefening gaan we wederom een brug slaan tussen de digitale en de analoge wereld. We gebruiken een Piezo buzzer die maakt een kleine klik zodra je er spanning op aansluit (probeer maar!). Op zich niet super spannend, maar als je nu de spanning aan en uitschakelt honderden keren per seconde zal de buzzer een toon produceren. En als je nu diverse rijen aan tonen tegelijkertijd verstuurd dan krijg je muziek! Met dit circuitje speel je een klassieke toontje!

code_to_note: |

  Tot nu toe hebben we alleen met numerieke gegevens gewerkt, maar de MicroView Arduino werkt ook met karakters (enkele, printbare, letters, getallen en andere symbolen), deze hebben een eigen type, "char" genaamd. Wanneer je rij (array) van karakters gebruikt, tussen dubbele aanhalingstekens (ook wel "string" genoemd), OF als een lijst van losse karakters, ieder tussen enkele aanhalingstekens.

      char notes[] = "cdfda ag cdfdg gf ";
      char names[] = {'c','d','e','f','g','a','b','C'};

  Een van Arduino's bruikbare ingebouwde commandos is de toon functie - tone() function. Deze functie stuurt de uitgang pin aan met een bepaalde frequentie. Ideaal voor gebruik bij het aansturen van buzzers en speakers. Als je een bepaalde hoeveelheid tijd opgeeft (in milliseconden), zal deze de toon afspelen en vervolgens stoppen. Als je geen tijd opgeeft dan blijft de toon oneindig lang spelen (of je gebruikt simpelweg de functie noTone() ).

      tone(pin, frequency, duration);

what_you_should_see: |
  Je zou dus eigenlijk niets moeten zien :) Wel horen! Een liedje. Als het niet werkt, loop dan allereerst de configuratie op het breadboard na en check of je het juiste programma hebt ingeladen.  

toubleshooting: |
  **Geen geluid**

  Gelet op de grootte en vorm van het piezo onderdeel zou zomaar de verkeerde gaatjes zijn gebruikt van het breadboard. Controlleer dus vooral de plaatsing van dit onderdeel.  
  
  **Kan je niet nadenken terwijl het melodietje speelt?**

  Haal het piezo onderdeel eruit, herlaad het programma en stop het onderdeel terug op het board. 

---
