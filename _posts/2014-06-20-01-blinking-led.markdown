---
layout: post
title:  "01 Blinking an LED"
date:   2014-06-20 20:16:18
categories: tutorial
hype: 01-blinking-an-led
codebender: 36521
parts:
    - sku:	    COM-09590
      points:	B14 [Cathode] → B15 [Anode]

    - sku:      COM-08377
      points:	A10 → A15

intro: |
  LEDs (light-emitting diodes ofwel licht-uitstralende diodes/gelijkrichters) zijn kleine, krachtige lichtjes die veel worden gebruikt en in uiteenlopende toepassingen. Ideaal dus om deze  MicroView workshop mee te beginnen, allereerst laten we een LED knipperen. En ja - het is zo eenvoudig als het aan en uitdoen van een lamp. Misschien vind je het wel erg simpel, maar dit soort oefeningen zijn ideaal om een goede basis op te bouwen. Zodat je binnen de kortste keren zelfstandig kunt experimenteren met ingewikkelde opzetjes.

code_to_note: |
  Voordat je de pinnen van de MicroView gaat aansluiten moet je eerst vertellen of je ze als ingang (INPUT) of uitgang (OUTPUT) gaat gebruiken. Hiervoor gebruik je de ingebouwde "functie" met de naam `pinMode()`.

      pinMode(A3, OUTPUT);

  Als je een pin als een uitgang gebruikt dan kun je het commando hoog geven om 5 volt spanning aan te zetten of het commando laag om de uitgang op 0 volt te zetten.

      digitalWrite(A3, HIGH);

  Het Arduino programma loopt in een loop. Als de MicroView het commando `delay()` ziet, dan zal deze wachten. Hoelang? Als de wachttijd bijvoorbeeld 1000 is - delay(1000) - dan stopt de loop voor 1 seconde, omdat er 1000 millisecondes in een seconde zit.

      delay(1000);

What_zou_je_moeten_zien: |
  Een knipperende LEDje. Zoniet, controlleer of je circuit klopt en check of je het juiste programma naar de MicroView hebt geupload. Werkt het nog steeds niet? Kijk daan naar troubleshooting tips hieronder.

toubleshooting: |
  **LED Not Lighting Up?**

  LEDs werken alleen in een richting. Haal de LED van het breadboard, draai de LED zodat de pootjes omgewisseld worden en probeer opnieuw. (geen zorgen: de LED beschadigt niet bij verkeerde montage).

---