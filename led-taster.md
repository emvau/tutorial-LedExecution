# LED per Taster steuern @tutorial
## @fullscreen
In diesem Tutorial lernst du, wie man einen **externen Aktor** (LED) am Micro:bit ansteuert! 🔌💡
**Verkabelung:**
- LED (mit Vorwiderstand) an **Pin P0** und **GND**
- Taster: Verwende **Knopf A** des Micro:bits
Ziel: Beim **ersten Drücken** geht die LED an, beim **zweiten Drücken**
wieder aus. 🔄
## 
Zuerst brauchen wir eine Variable, die sich merkt, ob die LED gerade an
oder aus ist.
Erstelle eine neue Variable ``||variables:Variablen||`` und nenne sie **ledAn**.
Setze sie am Anfang deines Programms auf ``||variables:setze ledAn auf 0||``.
##
Jetzt müssen wir ständig prüfen, welchen Zustand die LED gerade hat.
Füge eine ``||basic:dauerhaft||`` Schleife ein.
Darin liest du den aktuellen Zustand von Pin P0 aus und speicherst ihn in
der Variable:
``||variables:setze ledAn auf||`` ``||pins:digitale Werte von Pin P0||``
💡 So weiß dein Programm immer, ob die LED gerade leuchtet oder nicht –
auch ohne extra LED-Bauteil, das seinen Zustand meldet!
## 
Jetzt reagieren wir auf den Tastendruck.
Füge den Block ``||input:wenn Knopf A gedrückt||`` ein.
Darin fügst du eine ``||logic:wenn/dann/ansonsten||`` Bedingung ein:
- **Wenn** ``||variables:ledAn||`` (die LED also gerade an ist)
  → ``||pins:schreibe digitalen Wert von Pin P0 auf 0||`` (LED ausschalten)
- **Sonst**
  → ``||pins:schreibe digitalen Wert von Pin P0 auf 1||`` (LED einschalten)
## @fullscreen
Fertig! 🎉
Schließe die LED an **P0** an, lade das Programm hoch und drücke **Knopf A**!

💡 **Aufgaben zum Ausprobieren:**
- Schließe die LED stattdessen an **Pin P1** an – was musst du im Code ändern?
- Verwende statt **Knopf A** einen **externen Taster an P2** – was musst du nun ändern?
- Kannst du die LED **blinken** lassen, solange sie "an" ist, statt dauerhaft zu leuchten? 🤔
