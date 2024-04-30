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
-Basiert auf Feldeffekt-Transistoren
-Zugriff in Blöcken
-begrenzte Lebensdauer, weil der Löschvorgang Schäden hinterlässt
### Kernel
Aufgaben des Kernels:
-Abstraktion von Devices
-Behandeln von Interrupts
-Ausführen von Prozessen
-Specherverwaltung
-Filesystem-Verwaltung
-Netzwerk-Verwaltung
-Verwaltung d.Zugriffsrechte

## Praktische Informatik
-Wie schreibe ich ein Programm?
-Algorithmen und Datenstrukturen
-Software Engineering
### Computersprachen
Hardware-nahe Sprachen sollen eiffizient sein
Höhere Sprachen sollen den Programmieraufwand reduzieren
Es gibt strukturierte, objektorientierte, funktionale, deklarative Sprachen
Es gibt Compiler und Interpreter und auch Mischformen
### Python
Eigenschaften: 
-Multiparadigmensprache
  -enthält Merkmale von verschiedenen Sprachengenerationen
  -alles ist ein Objekt
-Interpretersprache:
  -CPython ist die Refferenzimplementation (in C) des Interpreters
  -JIT-Compilation zu Bytecode, dieser wrid dann interpretiert
Spracheigenschaften:
-dynamische Datentypen
  -vairablen müssen nicht typdeklariert werden, der Typ wird dynmaisch ermittelt werden und ggf. erweitert
-Sammeltypen
  -Listen, Dictionaries, ...
-Ablaufsteuereng
-if ...elif ...else
-Schleifen
  -Klassisches while
  -for als Iterator
  

## Angewandte Informatik
Aufgaben mit dem Computer lösen
-Simulationen und ihre Darstellung
-Datenverarbeitung

## Was ist ein Betriebssystem?
### Human Interface
-TTY (TeleTypewriter) = an die ersten Computer wurdne Tastaturen von Telegraphen angeschlosssen. Ausgabe: erst paar Lämpchen, später Papier.
-die Ära "Glass TTYs" also Tastatur + Bildschirm für Text ein Und ausgabe begann in den 1970ern
-1974 graphische Bediung (mit Maus)
-> GUI
-die Bedienung per Text (CLI = Command Line Interface) ist bis heute geblieben:
  - Vielseitigkeit, Mächtigkeit, dennoch technisch anspruchslos -> besonders gut für Fernzgugriff

#### Shell
Shell wird für die äussere Schicht des Betriebssystems verwendet (innen Kernel, aussen Shell), die für die INteraktion mit Menschen gedacht ist (HMI = HUman-Machine Interface), also entweder CLI oder GUI.
Das CLI ist ein Programm, welches USER-Eingaben interpretiert
-primärer zweck: ander Programme ausführen
-die Shell hat eingebaute Schlüsselwärter und Variablen
-Shells können Skripte interpretieren
-BASH = BOURNE AGAIN SHELL

### Def Betriebssystem
Ein Betriebssystem ist also ein programm, das die Abwicklung von anderen Programmen steuert und als Schinttstelle zwischen Benutzer, Programmen und Hardware dient.
Mit folgenden Aufgaben:
-Schnittstelle zwischen Mensch und Hardware
  -Bedienschnittstelle (User Interface) zwischen Benutzer und Programmen: dialogorientierte Konsole oder grafische Benutzeroberfläche
-Verwaltung von Ressourcen
  -geordente und kontrollierte Zuteilung von Prozessoren, Speichereinheiten und Peripheriegeräten
-Programmierschnittstelle (API, Application Programming Interace)
  - stellt die Infrastruktur für Programmabwicklung
### Wieso Linux
Portabilität = es funktioniert auf vielen verschiedenen Architekturen, vom Handy bis zum Supercomputer
open Source
Sicherheit = es sollen viele Aufgaben von vielen Benutzern gelichzeitig ausgeführt werden können, ohne dass diese sich gegenseitig stören
Netzwerk: idealerweise emrken wir keinen Unterschied, ob wir direkt neben dem computer oder übers netz verbunden arbeiten

# BASH Zusammenfassung

## Grundelgendes

### Basics
whoami, pwd, hostname, uname, man

### Standardbefehle und Kürzel
grep: durchsucht Dateien
find: gibt Dateinamen aus
sed, awk: nichtinteraktives Editieren, ("sed ist das Word, awk das Excel der Kommandozeile")
convert: nichtinteraktive Bildbearbeitung
tar: Datenarchivierung
ssh: Verbindung zu einem Server/Rechner
ps, top, bg, fg, kill: Umgang mit Prozessen
su - <username>: Benutzerwechseln
CTRL-C: abbrechen
CTRL-D: exit
CTRL-A/-E: Zeilenanfang/Ende
CTRL-K: Zeile löschen (und kopieren)
CTRL-Y: einfügen (aus Kill-Buffer)
CTRL-S: pausieren
CTRL-Q: weitermachen
CTRL-Z: Vordergrundprozess anhalten

## Bash Basics

Ausführen bedeutet:
  -die BASH erzeugt eine separate Umgebung
  -das Programm wird als eigenständiger Prozess gestartet
  -die Bash "wartet" im Hintergrund, bis das Programm beendet ist
das gestartete Programm kann POSIX-Signale empfangen --> man 7 signal
  -das wichtigste Signal ist SIGINT: CTRL-C

### File-Hierarchy

/ Root
/bin grundlegende Befehle und Programme
/boot Bootloader und Kernelimage
/dev an Computer angeschlossene Geräte
/etc Konfigurationsdateien
/home Benutzerverzeichnis
/liv Kernelmodeule und Bibliotheken
/sbin grundlegende Systembefehle
/tmp temporäre Dateien
/usr Bibliotheken, installierte Programme, ...
/var Unterverzeichnisse, deren INhalt sich ändert

### File-System-Tools

ls [option] [dir] INhalt des Verzeichnisses dir anzeigen
            -l    Mehr Informationen abnzeigen
            -a /--all Auch versteckte Dateien anzeigen wie . ..
mv src dst Dateien oder Verzeichnis umbenennen bzw verscheiben

cp [option] src dst srch nach dst kopieren
        -r/ -R /--recursive Rekursiv (inkl. Unterverzeichnisse)

ln [option] src dst Einen Link namens dst anlgen, der auf src verweist
  -s /--symbolic Einen Softlink anlegen

touch file Leere Datei namens File erstellen

rm [option] obj Datei bzw. Verzeichnis obj löschen
  -r/-R /--recursive Rekursiv (inkl. Unterverzeichnisse)
  -f/--force Nicht nochmals nachfragen
cd [dir] Change directory

mkdir dir make directory

rmdir dir remove directory

du [optioni] [dir] Belgenten Speicher-Platz von dir anzeigen
  -s/--summarize Nur eine Gesamtsumme zeigen

~zeigt zum Home Verzeichnis
- zeigt zum vorherigen Verzeichnis
. zeigt zum aktuellen Verzeichnis
.. zeigt zum übergeordneten Verzeichnis
* steht fpr irgendeine Zeichenkette
? steht für irgendein Zeichen
[] halten Platz für bestimmte einzelne Zeichen (,) oder einen Bereich (-)
{} halten Platz für bestimmte Zeichenketten
! oder ^ steht für Gegenteil
& führt Prozess im Hintergrund aus
\ leitet Escape-Sequenz ein
/ trennt Verzeichnisse voneinander
> leitet Ausgabe in eine Datei um
| leitett Ausgabe an anderen Befehl witer (Pipe)

## Basics Zugriffsrechte

### Superuser
In Unix-artigen Systemen gibt es einen Superuser: root
- mit su können wir zu jemand anderem werden, auch root
- mit sudo führen wir einzelne Kommandos als root aus (sofren wir das dürfen)

Die Benutzer gehören überdies noch einer oder mehreren Gruppen an, die ihnen weitere REchte gewähren:
- wer zu "wheel" gehört, darf sudo verwenden

### Zugriffsrechte

Nur mit den richtigen Rechten kann eine Datei /betrachtet /verändert/ ausgeführt werden oder in ein Verzeichnis gewechselt werden
- read r : Datei/Verzeichnis Inhalte lesen
- write w: Datei: verändern, Verzeichnis: INhalte hinzufügen/ entfernen
- execute x: Datei: als Programm ausführen, Verzeichnis: hineinwechseln

#### ls - l
Zeigt ganz links die einzelnen Rechte des usrs für spezifische Dateien und Verzeichnisse an

### chmod und chown
User U: r=4, w=2, x=1
Gruppe g: r=4, w=2, x=1
Reste o: r=1, w=2, x=1

chmod [option] file
chmod u+rwx datei Setzt Dateirechte für Besitzer auf lesbar, schreibbar, ausführbar
chmod g-w datei Entfernt schreibrechte für Gruppe
chmod 744 datei Setzt Dateirechte auf rwxr--r--

chown [option][user][:[gruppe]] file Ändert Besitzer und Gruppe einer Datei /eines Verzeichnisses

chown root datei Macht den User root zum Besitzer der Datei

## Ausgabe von Dateien

Mit < lässt sich die Standardeingabe umleiten.
Mit > lässt sich die Standardausgabe und der Standardfehler umleiten.
  - 1: Standard output (stdout)
  - 2: Standard error (stderr)
  - &: Beide

### Redirection

> und >> repräsentieren beide output redirection in Linux. Beides sind stdout redirections, jedoch überschreibt > eine schon bestehende Datei oder eine neue Datei wird erstellt, vorrausgesetzt  dass der dateiname noch nicht im Verzeichnis vorhanden ist. Das bedeutet, dass wenn man bestehendes aus einer Datei überschreiben will, dann sollte man > verwenden.
Wohingegen >> zu einer bestehenden Datei appendet/hinzufügt oder eine neue Datei erstellt, vorrausgesetzt der Dateiname ist noch nicht in diesem Verzeichnis vorhanden.

## Anführungszeichen
### "weiche Quotes"
sind durchlässig, d.h. $Variablen werden durch ihre WErte erstzt

$ echo "In diesem Terminal läuft $SHELL"
IN diesem Terminal läuf /bin/bash

### 'harte quotes'
sind undurchlässig, d.h. alles darin ist verbos

$ echo 'In diesem Terminal läuft $SHELL'
In diesem Terminal läuft $SHELL

### `Backquotes`
führen eine Anweisung aus und geben das Resultat zurücl

$ var = `echo "In diesem Terminal läuft $SHELL"`
$ echo $var
In diesm Terminal läuft /bin/bash

Quotes können auch verschachtelt und escpaed werden

$ echo 'Frage: "Was für eine Shell läuft in diesem Terminal?"'; echo "Antwort: \"Immer noch $SHELL\""
Frage
Antwort

## Prozessüberwachung
ps [option] Informationen über Prozesse anzeigen
  -u User Prozesse von User anzeigen
top oder htop Prozesse fortlaufend anzeigen

kll [signal] PID Signal an Prozess PID senden
    -9       SIGKILL: Prozess abbrechen

Kann zusammen mit grep verwendet werden um process id zu finden und dann kill -9 oder sigkill um den Prozess abzubrechen

## Dateien finden und anschauen

$find ~/ -name "punxsutawney*"
-> output

### Nach Muster suchen
$ grep "no shadow" *
$ grep -v "no shadow" *
$grep "no shadwo.*warmer" *

### cat
Catch => $cat datei gibt die datei in Terminal je nach dem in ASCII oder UTF-8 aus.

## Dateien bearbeiten und analysieren
### Dateien bearbeiten: sed
$sed -e 's/no shadow/early spring/g' -e 's/shadow/long winter/g' punxsutawney_phil.txt > punxsutawney_phil_2.txt
$cat file name
alles was die oberen Bedingungen in sed erfüllt

### Textanalyse: awk /oder auch cut
$cut -f 2 < file2.txt > forecasts.txt
$awk -F'\t+' '{print $2}' file2.txt > file_forecasts.txt
$cat file_forecasts.txt
alles nach einmal tabulator

### sortieren
$ sort < file.txt > file_sorted.txt

### Duplikate löschen
$ uniq -c < file_sorted.txt

### Dateien vergleichne

$ diff --color file.txt file_sorted.txt

## Exit Status von Anweisungen
Jede Anweisung hat einen Exit Status. Das ist ein Byte, welches angibt, ob die Anweisung erfolgreich ausgeführt werden konnte (=0 gut, ungleich 0 schlecht)

Anweisung führt die Anweisung aus und gibt den Exit Status zurücl
ANweisung1 && ANweisung2 führt Anweisung 2 aus falls Anweisung 1 erfolgreich war

Der Exit Status der letzten Anweisung wir in der Variable $? gespeichert

## {}
{ Anweisungen; } führt mehrere Anweisungen aus und gibt Exit Status zurück
$ a = apfel
$ { a = birne; mkdir $a; }
$ echo $a
brine
$ ls
brine

{Sequenz} führt eine Klammererweiterung durch

$ echo {1..10}
1 2 3 4 5 6 7 8 9 10
$ echo {1..10}{a..d}
1a etc.

${Parameter} führt eine Parameterexpansiondurch

$ name = pHil
$ echo ${ name:-`whoami`}
Phil

Funktionsname() definiert eine Bash-Funktion. Aufruf mit Funktionsnamen
{ Anweisungen; }

$ begrüsse() { echo "hallo $1"; }
$ begrüsse $name
Hallo Phil

## ()
(Anweisungen)

((Arithmetik)) oder let Arithmetik berechnet den arithmetischen Ausruck, gibt Exit Status 1 zurück wenn das Resultat 0 ist sonst 0

$(Anweisung) führt die Anweisung in einer Subshell aus und gibt deren Ausgabe statt Exit Status zurück (gleich wie `Anweisung`)

$((Arithmetik)) berehcnet den arithmetischen Ausdruck und gibt das Resulatat zurück

## []

[Ausdruck] ioder test Ausrdruck testet einen Ausdruck und gibt Exit Statzs 0 True oder 1 False zurück

[[ Ausdruck ]] ist eine Erweiterung von [ Ausdruck ], unterstützt Mustervergleich und Paramtererweiterung und spaltet Wörter nicht auf

Zeug[Index] greift auf ein Array-Element zu (String) Abruf mit ${Zeug[index]}

## Shell Scripts

Alle KOmmandozeilen-Befehle können auch ein ein Script verpackt werden. So können repetitive Aufgaben automatisiert werden. Mögliche Anwendungen:

Programmiereung:
  .Verschiedene Programme werden nacheinander aufgerufen
  .Dateien werden nach einen besimmten Muster durchsucht und bearbeitet
Datensicherungen:
  .Alle neuen oder geönderten Benutzerdateien werden über Nacht automatisch auf einer entfernten Maschnine gesichert
Überwachung von Prozessen und Ressourcen:
  .Laufende Proezesse werden regelmässig überwacht und wenn nötig abgebrochen
./ file.sh falls chmod x file.sh oder bash file.sh

## Bash Kontrollsrtukturen

### Verzweigungen
if ... then ... (elif ... then) ... else .. fi

### Fallunterscheidung
case ... in ... esac

### Schleifen
for ... in ... do ... done
while ... do ... done
until ... do ... done

## RC Files

Is a Data placement structure that determines how to store relational tables on a computer

Werden beim Start eines Programms aufgerufen
.bashrc

matplotlibrc

# Datentypen

Der Datentyp beschreibt, um welche Art Daten es sich handelt bzw. woraus der Datensatz zusammengesetzt ist und welche Operationen darauf erlaubt sind. Wir unterschieden:
- Elementare Datentypen sind diskret und begrenzt. Bsp.: Integer, Char;
- Auch floats sind im computer diskret d.h. nur endlich genau!
Pointer, d.h. Adressen auf die Daten im RAM, die als Refernezen fungieren bzw. einen indirekten Zugriff erlauben
Zusammengesetzte Datentypen (z.B.: Strings, Strukturen)

## Echte Datentypen
"Echte" Datentypen sind, was Prozessor/FPU wirklich verwenden (Floating Point UNit, eine Recheneinheit nur für floats)

Der Prozessor/die FPU hat Instruktionen und Register für:
- Integer in (8), (16), (32), (64) bit, signed (d.h. mit Vorzeichen bzw. auch negativ) und unsigned, sind eine Teilmenge von $Z$
- IEEE-754 Floats in single (32 bit) und double precision (64 bit) zur Darstellung von Gleitkommazahlen

alle anderen Datentypen sind von der SW erzeugt. z.B.: Booleans gibt es eigentlich so nichtm weil sie immer in 8 bzw. 32 Bit gespeichert werden. Generell gilt False=0 und True ungleich 0

## Datentypen im RAM

-Weil in den Registern zu wenig Platz ist, werden Daten zwischen RAM und Prozessor ausgetauscht
-Damit die Daten im riesigen RAM auffindbar sind, muss ihre Speicheradresse bekannt sein
-Im RAM können Datentypen auch zusammengesetzt, d.h. Mischungen und ganze Datensammlungen sein.
-Das Programm, das damit arbeitet, muss sie verstehen

# Daten im Speicher
## Alignment
Datentypen können i.A. nicht von beliebigen Adressen geladen werden, sondern müssen ausgerichtet werden (d.h. die Startadresse z.B. durch 8 teilbar). Das wird vom Compiler erledigt.

## Endianess
Die Daten sind entweder:
  - in Leserichtung angeordnet (Big Endian)
  - oder umgekehrt (Little Endian, z.B. PC)

# Type-Casting

-implizit = vom Compiler/ Interpreter durchgeführt z.B. float a = 3.14 * 5
-explizit = vom Programm vorgeschrieben z.B. int a = (int(3.99); ergibt 3
Wir unterscheiden:
  .Type promotion
  .Type demotion

# Under- and Overflow
Overflow errors come up when working with integers and floating points, and underflow errors are generally just associated with floating points.
## Overflow
Lets assume we have an integer stored in 1 byte. The greatest number we can store in one byte is 255, so let’s take that. This is 
11111111. Now, suppose we add 2 to it to get 00000010. The result is 257, which is 100000001. The result has 9 bits, whereas the integers we are working with consist of only 
8. What does a computer then do in this scenario? A computer will discard the most-significant bit (MSB) and keep the rest.


#include <iostream>
using namespace std;

int main() {
    // Define a variable to store the value (1 byte)
    unsigned char value = 255; // Maximum value for 1 byte

    // Add 2 to the value
    value = value + 1;

    // Print the result
    cout << "The result after adding 2: " << static_cast<int>(value) << endl;

    return 0;
}

## Underflow
Underflow is a bit trickier to understand because it has to do with precision in floating points. Again, due to the discrete nature of storage in computers, we cannot store an arbitrarily small number either. The floating-point convention comes up with techniques to represent fractional numbers. When we use these in calculations that result in a smaller number than our least value, we again exceed our designated space. Without going into details of floating-point representation, we can see how this problem would manifest by considering a decimal example.
Example: Suppose we are given designated boxes to write decimal numbers in. We have one box on the left of the decimal point and three boxes on the right. So, we can easily represent 0.004. Now, we want to perform a calculation, 0.004×0.004. The answer to this is 0.000016, but we simply do not have this many places available to us. So we discard the least-significant bits and store 0.000, which is quite obviously an erroneous answer.

#include <iostream>
using namespace std;

int main() {
    // Define a variable to store the value (1 byte)
    unsigned char value = 0; // Minimum value for 1 byte

    // Subtract 2 from the value (underflow)
    value = value - 1;

    // Print the result
    cout << "The result after subtracting 2: " << static_cast<int>(value) << endl;

    return 0;
}

# IEEE-754 Gleitkommazahlendarstellung
IEEE-754 schreibt die Formate für single und double precision vor.
Eine Gleitkommazahl berechnet sich aus:
-Vorzeichen s (in 1 bit)
-Mantisse m(in p=23 bzw. 52 bit)(=Nachkommatiel 1,m)
-Exponent (Charackteristik)e(in 8 bzw. 11.bit)
-Basis b (=2) und Bias B(=127 bzw 1023)

$X = (-1)^s (1+\frac{m}{2^p})b^{e-B}$

Achtung: float ist in:
  -C single
  -Python double

# Strings
Sind Arrays von Charactern
-Array = sequenzielle Abfolge von Elementen desselben Datentyps
-Character = Zeichen aus einer Symboltabelle, das durch seinen INdex als unsigned integer (8,16,32 bit) gegeben ist
-z.B. ACII (7 bzw. 8 bit)

# Python 3 Datentypen
in Python ist alles ein Objekt, Variablennamen sind Refferenzen
-type() gibt Objektklasse zurück
-help(type(a)) gibt die Dokumentation des Objekts aus

Built-in Data Types
-Numerische Typen
-bool--True(=1),False(=0)
int..signed integer von unlimitierter Länge
float...double precision floating point number (IEEE-754, 64 bit)
complex ... z.B. 1.2 + 3.4j

-Sequenzen: Strings, Listen, Tupel
-string... "Zeichenketten" können belieblig lang sein, acih leer:
-list .. Listen sind gereihte Mengen
  -unterschiedliche datentypen
  -nested arrays
  -dicts
-weitere sequenzen
  -(n)Tuple wie eine Liste, aber immutable z.B.: (2,3) oder (2,3,"hallo")
  -reange ... Zählersdequenz (als Generator)
-Sequenzen sind iterable
"Veränderbarkeit
  -numerische Typen, Strings und Tupel sind immutable
  -Listen und Dctionaries sind mutable, d.h. sie unterstützen add, delete, insert, rearange auf Komponentenebene

-Mappings: machen immuatble Datentypen zu Mutables
  -dict "Liste" von Key:Vlaue Paaren
  -Keys müssen immutable sein weil eine Hasthable erzeugt wird

# Escape Sequences
\n 
\t
\xhh ASCII Zeichen mit angegebenem hex-index hh
\uxxxx bzwe \Uxxxxxxxx stehen für 16 bzw. 32 Bit Unicde zeichen

# keywords
help("keywords")

# Numpy
numpy api.org

Dtype consistency for array scalars. Less memory space allocation. More precise and faster.

# Class Structures

## Class
class definiert eine neue Objektklasse analog zu def für Funktionen
Klasse = Bauplan, Instanz = damit im Speicher
angelegtes Objekt
● Klassenobjekte unterstützen
− Attributreferenzierungen obj.name
● Variablen, Operationen/Methoden (Fkt.)
− Instanzierung
● Funktionsnotation obj = MeineKlasse()
● spezielle Komponenten
− ist eine __init__-Methode vorhanden, wird sie bei Instanzierung automatisch
aufgerufen (=default constructor)
− ist eine __del__-Methode vorhanden, wird sie bei del() ausgeführt
− ist eine __str__-Methode vorhanden, wird sie bei Zuweisungen verwendet
− __doc__ ist ein Attribut, das den Docstring der Klasse enthält

## Atribute
sind Namen im Scope des Klasseninstanzobjekts, also alles hinter einem .
● Scope des Moduls, das die Klasse enthält, nicht der Klasse
− ein Modul (Sourcefile) kann mehrere Klassen enthalten
− self erlaubt Zugriff auf die Instanzattribute aus der Klasse heraus
● Datenattribute
− Instanzvariablen
− müssen nicht deklariert werden,
d.h. man kann einfach im Scope der Klasse Variablen deklarieren: obj.neu = 123
● Methoden: Konstruktor, Instanz-, Klassen- u. Statische Methoden
− zum Objekt gehörende Funktionen
− in Python wird das Objekt implizit als erstes Argument der Methode übergeben.
(implizites self). → Konvention: erster Parameter self (bzw. cls für Klassenmethoden)
− auch Funktionen können als Objekt zurückgegeben werden (ohne ())
− Methoden können auch in eine Klasse nachträglich eingebaut werden (schlechter Stil!)
− Aufruf anderer Methoden derselben Klasse über self
● Achtung: Datenattrib. überdecken gleichlautende Methodenattrib. und umgek.

## Objekte Speichern
Objekte speichern
Ein Objekt enthält Referenzen auf Elemente, die im Speicher verstreut sind. Will
man ein Objekt in ein File speichern, müssen die Daten erst in eine Bytefolge
(byte stream) umgewandelt werden = Objektserialisierung. Umgekehrt kann ein
Objekt geladen und de-serialisiert werden.
● einfache aber unsichere (repr/eval) Methode: pickle
● sichere Alternative: Javascript Object Notation: import json

## OOP Konzepte
Objektorientierte Programmierung: Konzepte
Neben dem Konzept von Klassen bzw. Objekten sprechen wir bei OOP noch von:
● Verkapselung (Encapsulation)
= Daten werden innerhalb einer Klasse „versteckt“
(geht in Python ja nicht so gut, siehe name mangling)
● Abstraktion
wird durch die Methoden einer Klasse erreicht.
z.B.: Person.kaufen(Buch)
● Vererbung (Inheritance)
eine Klasse überordnen, um die Attribute zu übernehmen
z.B.: class Student_in (erbt Attribute von Person)
● Polymorphie (Polymorphism)
übergeordnete Attribute verdecken. „verkehrte Vererbung“
z.B.: wenn wir Person.Name durch Student_in.Name verdecken

## Access modifiers
Private Instanzvariablen gibt es nicht in Python.
→ Konvention: lass Attribute mit Underscore (z.B. _name) in Ruhe.
● Name mangling: __name wird ersetzt durch __
classname_name
dies verhindert Namenskollisionen bei Erweiterungen.
● Iteratoren (for i in meineInstanz : )
definiere __iter__(self), welches self zurückgibt
definiere __next__(self), welches ein Element zurückgibt und
z.B. den Index intern anpasst.
● eine Klasse wird mit folgenden Methoden sortierbar:
def __eq__(self, other):
def __lt__(self, other):

# Decorators
Decorators erlauben Modifikationen an Funktionen und Klassen
● Definition von Properties
(= Attribut, dessen Wert über e. Fkt. erstellt wird)
● Definition von Wrapperfunktionen
● @classmethod zur Definition
zusätzlicher Konstruktoren
● @staticmethod erlaubt
Funktionsaufruf vom Objekt
ohne Instanzierung

# Modul erzeugenb
Funktionalität eines gewissen Umfanges wird am besten in Form
eines externen Moduls bereitgestellt.
- Distutils (alte Methode): https://docs.python.org/3/install/index.html#install-index
- Setuptools: https://setuptools.readthedocs.io/en/latest/setuptools.html
● hierarchische Struktur mit __init__.py in jedem Verzeichnis anlegen, diese
kann z.B. Unterpakete importieren, muss im Prinzip aber nichts enthalten.

# Files und Filetypen
 File (Datei) = zusammenhängende Binärdaten
(zur dauerhaften Speicherung)
● Metadaten = Daten über Daten. z.B. Filename, Dateigröße,
diverse Timestamps (creation, modification, last access), …
− Fileattribute = je nach Filesystem unterstützte Eigenschaften
(ugoa-+=rwxXst – siehe man chmod)
− Filename extension, Suffix = Die Typbezeichnung angehängt an
den Filenamen (.jpg, .mp3, …), ist eine Konvention aus den
1970ern, wurde von MS-DOS und Windows übernommen.

# Filetypen und Magic Numbers
Daten muss man anschauen, um sie richtig deuten zu können.
● So gut wie alle Datenformate beginnen mit einer magic number.
● Bekannte Signaturen (aus magic.mgc) werden von file verwendet.
● Achtung: bei Containerformaten (z.B. mp4) muss man noch tiefer
hineinschauen!
(z.B. mplayer -identify)

# MIME
Multipurpose Internet Mail Extensions
● Das e-Mail Protokoll sieht ASCII vor.
● Durch MIME werden Datentyp und
Zeichencodierung im Mail festgelegt.
● base64 = 3 Bytes werden in 4 ASCII-
druckbaren Zeichen codiert.

# Beispiele für Fileformate
Text (ASCII, UTF, …) - basierte Dateien wie .py, .txt, .html, .csv, …
Auch bei einem Textfile muss man wissen,
was drin steckt, um es richtig lesen zu können.
In Python setzt read UTF-8 voraus.
>>> myFile = open('scopetest.clean.py','r')
>>> print(myFile.read()) # .readline()
…
>>> myFile.close()

● .wav - Audiodaten im Rohformat
● Meist gibt es viele Möglichkeiten,
ein File eines gewissen Formates
zu decodieren.
● Will man unbedingt selbst mit den
Binärdaten arbeiten, hilft das
Paket struct.
>>> from scipy.io import wavfile
>>> rate, data = wavfile.read('unbenannt.wav')
>>> # jetzt haben wir die Datenpunkte als Liste
>>> import sounddevice as sd
>>> import soundfile as sf
>>> data, rate=sf.read('unbenannt.wav',dtype='int16')
>>> sd.play(data, rate)
>>> status = sd.wait()
>>> import struct
>>> f = open('unbenannt.wav', 'rb')
>>> data = f.read()
>>> hlen = 44
>>> s=(len(data)-hlen)//2
>>> fs = '<' + str(s) + 'h'
>>> myData = struct.unpack_from(fs, data, hlen)

BMP - Windows Bitmap
Rohformat für Bilddaten
14 B Fileheader + 40 B Infoheader
danach rohe Pixeldaten

JPEG (Joint Photographic Experts Group):
gängigstes Format für Bilder.
● (verlustbehaftete) Kompression:
Diskrete Kosinustransformation (DCT) auf
8x8 Blöcken + Quantisierung

PNG (Portable Network Graphics): gängigstes
verlustfreies Format für Bilder mit viel Redundanz.
● Redundanz = Wiederholung von Merkmalen
● Vorhersage (prediction) eines Pixels durch die
Werte seiner Nachbarn, Kodierung der Differenz
● Differenzen werden gezippt, d.h. mit dem Deflate
Algorithmus komprimiert.

ZIP ist ein Containerformat zur verlustfreien Kompression von Dateien (bzw.
Verzeichnissen). (Python: import zipfile)
● Zumeist wird mit dem dem Deflate Algorithmus komprimiert.
● Der wesentliche Unterschied zu .tar.gz ist, dass bei ZIP jede enthaltene Datei
einzeln für sich komprimiert wird.

PDF (Portable Document Format) ist ein Dokumentenformat, welches als
Weiterentwicklung von PostScript gesehen werden kann.
● Das Format beschreibt exakt das Layout von Texten inkl. Schriften,
geometrischen Elementen (Vektorgrafiken) und von eingebundenen
Bilddaten. Diese können auch komprimiert sein.
● PDF Dateien sind als Endprodukt gedacht und nicht leicht editierbar.
● Es gibt Eingabefelder für die Erstellung leicht ausfüllbarer Formulare.
● Es gibt (eingeschränkte) Möglichkeiten zur Darstellung von und Interaktion
mit 3D Grafiken (Einbettung von PRC Daten).

# Datenkompression
= Reversible Darstellung von Daten mit weniger Speicherplatz
● Wir unterscheiden einfache Methoden (z.B. Lauflängencodierung),
Wörterbuchbasierte Methoden (z.B. Deflate)
und Entropiekodierungen (z.B. Huffman-Codes).
● Run-Length compression ersetzt Sequenzen identischer Symbole (Lauflängen)
durch das Symbol und die Anzahl der Wiederholungen.
z.B.: H A L L L L L O ! → H A 5L O !
Unterschiede gibt es in der Art der Markierung der Lauflängen (Escape Symbol).
● Entropy Coder verwenden Tabellen mit eindeutig decodierbaren Codewörtern
unterschiedlicher Länge. Sie stellen häufiger auftretende Symbole mit kürzeren
Codes dar.
● Dictionary-based (Lexikalische) Kompression ersetzt identisch wiederkehrende
Passagen durch Referenzen.

Einfachstes Beispiel für eine Entropiecodierung:
Der sog. Unäre Code ist eindeutig decodierbar:
Index fixer
Code
Codewort
variabler Länge
unser
Beispiel
0 00 1 L
1 01 01 H
2 10 001 A
3 11 0001 O
HALLLLLO =
fix:
0110000000000011
variabel:
01001111110001

Lexikalische Daten-
kompression geht auf LZ77
(Lempel und Ziv) zurück.
● funktioniert gut bei
strukturierten Daten-
sätzen, wie Text (Wort-
wiederholungen)
● nicht gut für
verrauschte Daten
● gängigster Algorithmus:
Deflate

# Fehlertoleranz
Um Daten vor Übertragungsfehlern zu schützen, werden redundante Codes
verwendet. D.h. auch, die Datenmenge wird etwas vergrößert.
● Checksum = Prüfsumme, z.B. Quersumme, Paritätsbit, CRC, …
● CRC (Cyclic Redundancy Check): Bessere Prüfsumme. Die Datenpunkte
werden als Koeffizienten eines Polynoms aufgefasst. Durch Division durch ein
Generatorpolynom wird ein Rest berechnet und als Prüfsumme verwendet.
Kurze CRCs haben begrenzte Korrekturmöglichkeiten.
● Reed-Solomon-Codes: Jede Folge von n Symbolen kann als Polynom n−1-ten
Grades betrachtet werden. Durch Lagrange-Interpolation werden mehr
Datenpunkte erzeugt. Solange n korrekte Symbole vorhanden sind, sind die
Originaldaten rekonstruierbar.
Einsatz in allen möglichen Speichermedien (CD), Bar- und QR-Codes, …

# CRC und Polynomdivision
Wir betrachten unsere Daten als Polynom mit Binärkoeffizienten:
0x12345678 = 00010010001101000101011001111000
und dividieren das durch unser „Generatorpolynom“, bei CRC-16 ist das G(x)=x^16+x^12+x^5+1,
d.h.: 10001000000100001
Syndrom = da wir die Daten nicht „auf einmal“ dividieren, sondern byte- oder wortweise, brauchen
wir einen Übertragswert. Bei CRC-16 starten wir mit S=0xFFFF
Wir berechnen:
000100100011010001010110011110000000000000000000 % 10001000000100001 = 0011000011101100
S=1111111111111111
Unsere Daten mit CRC-16 versehen:
0x1234567830EC

# Lagrange Interpolation

Lagrange Interpolation Formula finds a polynomial called Lagrange Polynomial that takes on certain values at an arbitrary point. It is an nth-degree polynomial expression of the function f(x). The interpolation method is used to find the new data points within the range of a discrete set of known data points.

In this article, we will learn about, Lagrange Interpolation, Lagrange Interpolation Formula, Proof for Lagrange Interpolation Formula, Examples based on Lagrange Interpolation Formula, and others in detail.

## What is Lagrange Interpolation

Lagrange Interpolation is a way of finding the value of any function at any given point when the function is not given. We use other points on the function to get the value of the function at any required point.

Suppose we have a function y = f(x) in which substituting the values of x gives different values of y. And we are given two points (x1, y1) and (x2, y2) on the curve then the value of y at x = a(constant) is calculated using Lagrange Interpolation Formula.

# Fileformate in unseren Disziplinen

● CSV (Comma Separated Values), d.h. eine Text-Tabelle
→ entweder selber einlesen oder mit dem Paket csv
● rohe, unformatierte Binärdaten, meist .dat – selber einlesen, mit
struct verarbeiten, binascii, numpy.fromfile mit custom datatype, …
● hdf5 (Hierarchical Data Format): modernes Dateiformat zur effizienten
Speicherung riesiger Datenmengen. (Python: import h5py)
● FITS (Flexible Image Transport System): seit 1981 der Astronomen
liebstes Format: from astropy.io import fits
FITS ist ein Containerformat für gemischte Tabellen und Binärdaten.
● ASDF (Advanced Scientific Data Format) strebt an, das FITS-
Nachfolgeformat zu werden. import asdf







