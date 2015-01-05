---
layout: post
title:  "04 Push Buttons"
date:   2014-06-20 20:16:18
categories: tutorial
hype: 04-push-buttons
codebender: 36524
parts:

    - sku:	    COM-09190
      points:	D20, D22, G20, G22

    - sku:      BLACK-JUMPER
      points: B14 → B20

    - sku:      RED-JUMPER
      points: A13 → A22

intro: |
  In deze oefening komt een van de meest gebruikte en eenvoudige inputs aan bod: een drukknop. Als de drukknop wordt ingedrukt maken de contacten een verbinding met de aarde, de MicroView signaleert dit en reageert hierop. Wat gaat er gebeuren? De MicroView laat "ON" zien, als je de knop indrukt, en "OFF" als de knop niet is ingedrukt. (In de code kun je zien waarom!)    Als het niet zo werkt, controlleer dan je configuratie, het circuit en of je de code naar de MicroView hebt geupload. En hieronder zijn de troubleshooting tips.

code_to_note: |

  The digitale pinnen kunnen zowel als input als output werken. Je bepaalt de gewenste richting met de volgende code. 

      pinMode(buttonPin, INPUT);

  Om een digitale input te lezen gebruik je de digitalRead() functie. Deze geeft HIGH als er 5V op de pin staat, of LOW als er 0V op de pin staat.

      buttonState = digitalRead(buttonPin);

  Omdat de knop verbonden is met de aarde (GND - ground) zal hij bij het indrukken de pin laag (LOW) zetten. Hieronder laten we de code zien waarin gekeken wordt of de knop is ingedrukt. Het is devolgende evenwichtsvergelijking ("==").

      if (buttonState == LOW)

what_you_should_see: |
  Het scherm van de MicroView laat "ON" zien als de knop is ingedrukt. "OFF" als je de knop weer loslaat. (Kijk maar in de code!) Als het niet werkt, controlleer dan je configuratie op het breadboard en of je het juiste programma hebt geladen in de MicroView.

toubleshooting: |
  **Light Not Turning On**

  De drukknop is vierkant en het kan dus gebeuren dat je hem verkeerd geplaatst hebt. Probeer hem eens 90 graden te draaien.  
  
  **Underwhelmed**

  Geen probleem, deze voorbeelden zijn heel erg vereenvoudigd zodat we de basisprincipes kunnen uitleggen. Probeer zelf maar verschillende componenten met elkaar te combineren. De mogelijkheden zijn eindeloos.

---

## How to use logic like a Vulcan:

Een van de dingen die de MicroView zo bruikbaar maakt is dat het ingewikkelde keuzes kan maken afhankelijk wat het qua input binnen krijgt. Bijvoorbeeld, je zou een thermostaat kunnen maken die de verwarming aanzet als het te koud wordt, een ventilator aanzet als het te warm wordt en de planten water geeft zodra ze droog staan. 

Om dergelijke beslissingen te kunnen maken, zijn er in de Arduino programmeeromgeving een set van logische instructies. Hiermee kun je ingewikkelde als/dan opdrachten maken. Enkele voorbeelden van deze instructies:

<img src="/assets/logic.svg" style="width:100%" />

Je kunt deze functies combineren en zo ingewikkelde opdrachten schrijven als

    if ((mode == heat) && ((temperature < threshold) || (override == true))) {
        digitalWrite(HEATER, HIGH);
    }

... zal de verwarming aandoen als de verwarming op de automatische stand staat EN de temperatuur laag is. OF als je hem zelf handmatig aanzet, buiten het automatische programma om. Met deze "logische opdrachten" kun je de MicroView programmeren om hem intelligente beslissingen te laten maken en zo dus zijn omgeving te laten beheren. De mogelijkheden zijn eindeloos. 