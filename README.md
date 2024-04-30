# Informatik
## Theoretische Informatik
-Was ist Information?
-Was kann berechnet werden?
-Was ist eine Anweisung?
-Entscheidbarkeit("Halteproblem"), Komplexität (Landau O)
-Berechenbarkeit(P-NP), Formale Sprachen und Automaten ("Turing Machine")
### Begriffe aus der theoretischen Informatik
-Information = Wissen, das von A nach B übertragen wird
-Daten = mit Symbolen (Codewörtern) gespeicherte Information
-Shannon-Entropie $H(X) = - \sum_{x \in X}p(x)Idp(x)$ = mittlerrer Infromationsgehalt pro Symbol
-Alogrithmus = exakt ausformulierte Handlungsvorschrift aus endlich vielen Einzelschritten
-finite state machine = Modell, das Zustände (States) und Bedingungen für deren Übergänge (Guards) beschreibt
-Landau O = asymptotisches Verhalten einer Funktion Sei $Abb f, Abb g$ dann ist $f = K * O(g)$
## Technische Informatik?
Woraus besteht ein Computer?
Womit rechnet er?
-Hardware, Computerarchitektur
-Binäre Digitaltechnik verwendet "binary digits". EIn Bit hat entweder den Zustand 1 oder 0, die Basis im Dualsystem is 2
-Operationen im Computer sind mit Logic-Gates und Elektro-Bauteilen realisiert
-CPU verarbeitet die Instrukionen. Jede Instruktion besteht aus einer NUmmer, die surch einen "OpCode" gekennzeichnet wird un typischerweise 1-2 Operanden
-Instruktionen verwenden Register für die Ein- und Ausgabe und es gibt Instruktionen für den Austauch zwischen Registern und dem Speicher (RAM)
-Die Instruktionen selbst werden sequenziell aus dem Speicher gelesen. Eine Abfolge solcher (Assembler-)Insturktionen ist schon ein Programm
-Insturkioenn, die eine CPU nicht hat, müssen aus den vorhandenen zusammengesetzt werden.
-Damit wir nicht in Assembler programmieren müssen werden "höhere" Sprachen in Assembler überseztt (=kompiliert)
### Beispiel ARM Assembler
0: e0130091 muls r3, r1, r0
Dabei ist 0 die Addresse des Programms im Speicher, e... ein Instruktionswort, der rest Assembler
### Zahlendarstellung
-Mehrere Bits stellen eine Zahl dar
1101 = 1*2^3 + 1*2^2 + 0*2^1 + 1*2^0 = 13
-Eine Gruppe von 8 bits nennt man 1 Byte, 16 bits = halfword, 32 bits = word
-Präfixe SI IEC
-OFt werden Zahlen im HExadezimalsystem (Basis=16) angegeben
Zähler = 0 1 2 3 4 5 6 7 8 9 A B C D E F
### Man unterschiedet zwischen volatilen Speicher (Strom weg -> Daten weg) und nonvolatilem Speicher (die DAten bleiben ohne Strom erhalten)
-RAM (Random Access Memory)
-Whlafreier Zugriff möglich, d.h. jede beliebige Speicherstelle kann jederzeit angeforder werden
-im PC als volatiles SDRAM realisiert (als winzige Kondensatoren)
-SSD:
-FLASH-basierter nonvolatiler Speicher (auch USB Sticks)

## Praktische Informatik
-Wie schreibe ich ein Programm?
-Algorithmen und Datenstrukturen
-Software Engineering
## Angewandte Informatik
Aufgaben mit dem Computer lösen
-Simulationen und ihre Darstellung
-Datenverarbeitung

