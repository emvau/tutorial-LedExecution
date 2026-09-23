# LED per Taster steuern @tutorial

## Schritt 1 @fullscreen

In diesem Tutorial lernst du, wie man einen **externen Sensor** (Taster)
und einen **externen Aktor** (LED) am Micro:bit ansteuert! 🔌💡

**Verkabelung:**
- LED (mit Vorwiderstand) an **Pin P0** und **GND**
- Taster: Verwende **Knopf A** des Micro:bits – oder schließe alternativ
  einen externen Taster **parallel an Pin P5** an (das ist intern mit
  Knopf A verbunden)

Ziel: Beim **ersten Drücken** geht die LED an, beim **zweiten Drücken**
wieder aus. 🔄

## Schritt 2

Zuerst brauchen wir eine Variable, die sich merkt, ob die LED gerade an
oder aus ist.

Erstelle eine neue Variable ``||variables:Variablen||`` und nenne sie **ledAn**.

Setze sie am Anfang deines Programms auf ``||variables:setze ledAn auf 0||``.

## Schritt 3

Jetzt müssen wir ständig prüfen, welchen Zustand die LED gerade hat.

Füge eine ``||basic:dauerhaft||`` Schleife ein.

Darin liest du den aktuellen Zustand von Pin P0 aus und speicherst ihn in
der Variable:

``||variables:setze ledAn auf||`` ``||pins:digital lese Pin P0||``

💡 So weiß dein Programm immer, ob die LED gerade leuchtet oder nicht –
auch ohne extra LED-Bauteil, das seinen Zustand meldet!

## Schritt 4

Jetzt reagieren wir auf den Tastendruck.

Füge den Block ``||input:wenn Knopf A gedrückt||`` ein.

Darin fügst du eine ``||logic:wenn/dann/sonst||`` Bedingung ein:

- **Wenn** ``||variables:ledAn||`` (die LED also gerade an ist)
  → ``||pins:digital schreibe Pin P0 auf 0||`` (LED ausschalten)
- **Sonst**
  → ``||pins:digital schreibe Pin P0 auf 1||`` (LED einschalten)

## Schritt 5 @fullscreen

Fertig! 🎉

Schließe die LED an **P0** an, lade das Programm hoch und drücke **Knopf A**
(oder deinen externen Taster)!

💡 **Aufgaben zum Ausprobieren:**
- Schließe die LED stattdessen an **Pin P1** an – was musst du im Code ändern?
- Verwende statt **Knopf A** den **externen Taster an P5** – funktioniert es genauso?
- Kannst du die LED **blinken** lassen, solange sie "an" ist, statt dauerhaft zu leuchten? 🤔
