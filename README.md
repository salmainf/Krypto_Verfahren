## Krypto-Verfahren

Angelov , Eser , Marku , Tanner 


# Einführung

In unserem Projekt geht es um die Verschlüsselung von Botschaften mit zweier Verschlüsselungsarten. In unserem Programm, welches wir in Visual Studio mit C# implementiert haben, kann man als Benutzer auswählen, mit welcher Methode die Botschaft verschlüsselt werden soll. Danach gibt man den Schlüssel/das Schlüsselwort ein. Wenn es eingelesen wurde, kann man nun seine Botschaft eingeben, welche dann verschlüsselt und auf einer neuen Zeile ausgegeben wird. Danach kann man nach Wunsch auch noch weitere Botschaften verschlüsseln.

# Definierung

# Cesar Verschlüsselung

Die Cesar Verschlüsselung ist die einfachste aber auch unsicherste Verschlüsselungsmethode. Man verschiebt im 26 buchstabigen lateinischen Alphabet die Zeichen zyklisch eine gewisse Anzahl nach rechts, somit geht es automatisch wieder zu "A" wenn es "Z" überschreitet.Diese Verschiebung ist der Schlüssel des ganzen. Bei dem ganzen Verfahren wird also das normale Alphabet mit dem Schlüssel auf eine neue Abfolge des Alphabets überschrieben.

D.h z.B wenn der Schlüssel 8 ist, wäre A=I

So könnte man das Wort "Sicher" mit diesem Schlüssel verschlüsseln. Somit käme man auf das verschlüsselte Wort: "AQKPMZ"

# Vigenère Verschlüsselung

Bei der Vignere Verschlüsselung wird nicht, wie bei der Cesar, jeder Klartextbuchstabe um eine gewisse Zahl verschoben, sonder man verschiebt mithilfe eines Schlüsselwortes. Das Schlüsselwort kann selbstständig gewählt werden vom Benutzer. Hierbei nummeriert man das Alphabet von 0-25, d.h z.B A=0 und B=1 usw. Man weist also erst einmal jedem Buchstaben des Schlüsselwortes und des Klartextes eine Zahl, also die Position des Buchstabens, zu. Dann begint man und Verschlüsselt immer den ersten Buchstaben des Klartextes, mit dem ersten Buchstaben des Schlüsselwortes. Wenn das Schlüsselwort zu Ende ist, fängt man wieder von vorne an. Nun addiert man die beiden Zahlen der zusammengehörigen Buchstaben und erhält somit die Positionszahl des verschlüsselten Buchstaben.

D.h z.B wenn das Schlüsselwort "montag" wäre und der Klartext ist "Ich liebe den Montag" verschieben wir so:

|.|.|.|.|.|.|.|.|.|.|.|.|.|.|.|.|.|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|M|O|N|T|A|G|M|O|N|T|A|G|M|O|N|T|A|
|12|14|13|19|0|6|12|14|13|19|0|6|12|14|13|19|0|
|I|C|H|L|I|E|B|E|D|E|N|M|O|N|T|A|G|
|8|2|7|11|8|4|1|4|3|4|13|12|14|13|19|0|6|


|A|B|C|D|E|F|G|H|I|J|K|L|M|N|O|P|Q|R|S|T|U|V|W|X|Y|Z|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|24|25|

Nun rechnen wir für den ersten Buchstaben 12+8=20, 20 wäre die Positionszahl von U. Der erste Buchstabe ist nun also U, so fahren wir weiter fort, bis das Wort komplett verschlüsselt ist. Das Endresultat ist "UQUEIKNSQXNSABHTG".

# Planung mit IPERKA


| IPERKA | Mitglied | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|I|Alle|Informieren über Cesar-Methode, verstehen wie diese funktioniert. In Gruppe absprechen, ob es alle verstanden haben. |
|P|Alle|Planen, Auftrag in kleinere Teilaufgträge aufspalten.Einteilen wer welche Aufträge übernimmt, was für Wissen dazu nötig ist. Allfällige Fragen mit dem Auftraggeber klären.|    
|E|Alle|Entscheiden, ob noch weitere Einteilungen/Informationen nötig sind. Plan nach Logik und Fehlern durchsuchen, wenn alles stimmt zur nächsten Phase übergehen.|
|R|Alle|Programmieren des Projektes in Visual Studios.|
|K|Alle|Kontrollieren, ob das Programm sauber läuft.|
|A|Alle|Auswerten des Endproduktes.|



## 1 Informieren


### 1.1 User Stories

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    |  Funktional     | Muss | Als Programmierer möchte ich dem Benutzer die Auswahlmöglichkeit zwischen der Cesar/Base-64/Vignere Verschlüsselung geben |
| 2    |  Funktional     | Muss | Als Programmierer möchte ich dem Benutzer die Auswahlmöglichkeit zwischen kodieren/dekodieren geben |
| 3    |  Funktional     | Muss | Als Benutzer möchte ich einen Schlüssel eingeben können, mit dem meine Botschaft verschlüsselt wird |
| 4    |  Funktional     | Muss | Als Benutzer möchte ich eine Botschaft eingeben können |
| 5    |  Funktional     | Muss | Als Programmierer möchte ich die Botschaft erfolgreich verschlüsseln/entschlüsseln können |
| 6    |  Funktional     | Muss | Als Benutzer möchte ich meine Botschaft verarbeitet wieder ausgegeben angezeigt bekommen |
| 7    |  Qualität       | Muss | Als Benutzer möchte ich die Möglichkeit bekommen nochmals eine Botschaft einzugeben|
| 8    |  Qualität       | Muss | Als Programmierer möchte ich bei einer inkorrekten Eingabe eine Fehlermeldung ausgeben können |


### 1.3 Testfälle

| TC-№ | Ausgangslage | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  |Konsole startet, warten auf Auswahl|Auswahl einer Verschlüsselung-Art|Ausgabe von meiner Auswahl|
| 1.2  |Konsole läuft, Abfragen, welchen Dienst, Codieren/Decodieren|Eingabe des gewüschten Dienstes| Ausgabe meiner Wahl|
| 1.3  |Konsole läuft, warten auf Eingabe von Schlüssel| Eingabe eines Schlüssels | Einlesen des Schlüssels|
| 1.4  |Konsole läuft, warten auf Eingabe von Botschaft| Eingabe einer Botschaft | Einlesen der Botschaft|
| 1.5  |Konsole läuft, Botschaft erhalten|Verschlüsseln/Entschlüsseln der Botschaft| Ausgabe von verarbeiteter Botschaft|
| 1.6  |Konsole läuft, Botschaft wurde verarbeitet|-| Ausgabe von fertig verarbeiteten Botschaft|
| 1.7  |Konsole läuft, warten auf Eingabe| Eingabe einer Antwort (j/n)| Je nach Antwort, Beenden des Programmes oder Neustart |
| 1.8  |Konsole läuft, warten auf Eingabe| Fehlerhafte Eingabe| Ausgeben einer Fahlermeldung, anstelle von Shutdown|

### 1.4 Diagramme




## 2 Planen

# Cesar

| AP-№ | Frist | Zuständig | Beschreibung | geplante Zeit |
| ---- | ----- | --------- | ------------ | ------------- |
| 1.A  |  24.10.22     |Erik Marku|Auswahl der Verschlüsselungs-Art |180 Min|
| 2.A  |  24.10.22     |Angel Angelov|Kodieren/Dekodieren, mithilfe von Variablen |180 Min|
| 2.B  |  31.10.22     |Salma Tanner| Eingabe des Schlüssels |180 Min|
| 3.A  |  31.10.22     |Angel Angelov/Erik Marku| Verchlüsselung/Entschlüsselung implementieren|180 Min|
| 4.A  |  07.11.22     |Sudenas Eser| Speichern und Ausgabe der Botschaft | 90 Min|
| 5.A  |  07.11.22     |Sudenas Eser| Fragen nach erneuter Eingabe| 90 Min|
| 5.A  |  07.11.22     |Salma Tanner| Fehlermeldung generieren, try/catch| 60 Min|
Total: 1000 Min

# Vignere

| AP-№ | Frist | Zuständig | Beschreibung | geplante Zeit |
| ---- | ----- | --------- | ------------ | ------------- |
| 1.A  |  14.11.22    |Sudenas Eser|  |180 Min|
| 2.A  |  14.11.22    |Salma Tanner| Erstellen von zufälligem Zahlengenerator|180 Min|
| 2.B  |  21.11.22    |Sudenas Eser | Erstellen von Kontrolle für Benutzerzahl/Rückmeldung |180 Min|
| 3.A  |  21.11.22    |Salma Tanner| Ausgabe von Rückmeldung an Benutzer|180 Min|
| 4.A  |  28.11.22    |Sudenas Eser| Bei ungültiger Eingabe, erneuter versuch anstelle von Programmm-Ende| 180 Min|
| 5.A  |  28.11.22    |Salma Tanner| Nach erraten der Zahl, werden gebrauchte Versuche ausgegeben| 90 Min|
| 6.A  |  5.11.22     |Salma Tanner| Nach erraten der Zahl, werden gebrauchte Versuche ausgegeben| 60 Min|
Total: 930 Min






## 3 Entscheiden

Wir haben die Cesar Verschlüsselung erfolgreich Programmieren können und haben dann begonnen, die Vignere Verschlüsselung zu implementieren. Die Aufteilung ist bei uns durchmischt, da wir uns Freiheiten lassen wollten. Somit hat jeder einen Teil programmiert aber die Interessen wurden doch noch abgedeckt.


## 4 Realisieren




## 5 Kontrollieren

 AA-

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |13.9.22|Alles funktioniert, korrekte Ausgabe|Salma Tanner|
| 1.2  |13.9.22|Vollständige ausgabe|Salma Tanner|
| 1.3  |13.9.22|Funktioniert alles|Salma Tanner|
| 1.4  |13.9.22|Guter Umgang mit Fehleingabe, korrekt|Salma Tanner|
| 1.5  |13.9.22|Anzeigen der Versuche funktioniert|Salma Tanner|
| 1.6  |13.9.22|Anzeigen der Versuche funktioniert|Salma Tanner|
| 1.7  |13.9.22|Anzeigen der Versuche funktioniert|Salma Tanner|


AA-Das Spiel funktioniert und beinhaltet alle Vorgaben. Jedoch hat es einen Fehler bei der Eingabe. Wenn man eine höhere Zahl als hundert eingibt, wird diese auch akzeptiert, nur bei etwas anderem als einer Zahl gibt es eine Fehlermeldung aus.







