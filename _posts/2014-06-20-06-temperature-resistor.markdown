---
layout: post
title:  "06 Temperature Sensor"
date:   2014-06-20 20:16:18
categories: tutorial
hype: 06-temperature-sensor
codebender: 36526
parts:
    - sku:	    SEN-10988
      points:	A14, A15, A16

    - sku: BLUE-JUMPER
      points: B13 → B15

    - sku: RED-JUMPER
      points: I8 → E16

intro: |
  Een temperatuursensor werkt precies zoals hij klinkt - een sensor die de temperatuur meet van de omgeving. Deze sensor heeft drie pinnen – een positieve, een aarde (GND) en een signaal. Dit is een lineaire temperatuursensor. Een verandering in temperatuur van 1 graad Celcius is gelijk aand de verandering van 10 millivolt van de sensor uitgang. De TMP36 sensor heeft nominaal 750 mV bij 25°C (ongeveer kamertemperatuur). In dit circuit leer je hoe je de temperatuursensor integreert met de MicroView, en gebruik je de seriele monitor om de temperatuur op het scherm zichtbaar te maken.
  
  Let op bij het maken van het circuit! Verwissel niet de transistor met de temperatuursensor, ook al zien ze er hetzelfde uit. Zoek naar “TMP” op sw behuizing van de temperatuursensor.

  <img src="/assets/tmp36-pinout.png" />

what_you_should_see: |
  Terwijl je de temperatuursensor laat opwarmen en afkoelen zie je de meter op het scherm van de MicroView op en neer bewegen. 

toubleshooting: |
  
  **Temperature Value is Unchanging**

  Probeer de sensor tussen je vingers vast te houden, zodat hij op kan warmen of houd er een zak met ijs tegen om hem af te koelen.

---
