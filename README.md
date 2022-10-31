# Krypto-Verfahren

Angelov (A), Eser (E), Marku (M), Tanner (T)


# Einführung

In unserem Projekt geht es um die Verschlüsselung von Botschaften mit der Cesar-Methode. Man soll in einem, von uns erstellten Programm eine Eingegebene Nachricht verschlüsseln oder entschlüsseln können. Diese Verschlüsselungsmethode verschiebt im Prinzip einfach die Buchstabenabfolge (A wird zu D, B wird zu E usw.). Mithilfe unseres Programmes muss man sie nicht selber verstehen oder schreiben, man kann einfach die Botschaft eingeben und sie wird verschlüsselt/entschlüsselt.

# Planung mit IPERKA


| IPERKA | Mitglied | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|I|Alle|Informieren über Cesar-Methode, verstehen wie diese funktioniert. In Gruppe absprechen, ob es alle verstanden haben |
|P|Alle|Auftrag in kleinere Teilaufgträge aufspalten.Einteilen wer welche Aufträge übernimmt, was für Wissen dazu nötig ist. Allfällige Fragen mit dem Auftraggeber klären|    
|E|Alle|Entscheiden, ob noch weitere Einteilungen/Informationen nötig sind. Plan nach Logik und Fehlern durchsuchen, wenn alles stimmt zur nächsten Phase übergehen|
|R|Alle|Programmieren des Projektes in Visual Studios|
|K|Alle||
|A|Alle||



# Informieren

# Cesar Verschlüsselung

Die Cesar Verschlüsselung ist die einfachste aber auch unsicherste Verschlüsselungsmethode. Man verschiebt im 26 buchstabigen lateinischen Alphabet die Zeichen zyklisch eine gewisse Anzahl nach rechts, somit geht es automatisch wieder zu "A" wenn es "Z" überschreitet.Diese Verschiebung ist der Schlüssel des ganzen. Bei dem ganzen Verfahren wird also das normale Alphabet mit dem Schlüssel auf eine neue Abfolge des Alphabets überschrieben.




### 1.1 User Stories

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1    |  Funktional     | Muss | Als Programmierer möchte ich dem Benutzer die Auswahlmöglichkeit zwischen codieren/decodieren geben |
| 2    |  Funktional     | Muss | Als Benutzer möchte ich eine Botschaft eingeben können |
| 3    |  Funktional     | Muss | Als Programmierer möchte ich die Botschaft erfolgreich verschlüsseln/entschlüsseln können |
| 4    |  Funktional     | Muss | Als Benutzer möchte ich meine Botschaft verarbeitet wieder ausgegeben angezeigt bekommen |
| 5    |  Qualität       | Muss | Als Programmierer möchte ich den Benutzer abfragen, ob er nochmals eine Eingabe tätigen will|
| 6    |  Qualität       | Muss | Als Benutzer möchte ich die Möglichkeit bekommen nochmals eine Botschaft einzugeben|
| 7    |  Qualität       | Muss | Als Programmierer möchte ich bei einer inkorrekten Eingabe eine Fehlermeldung ausgeben können |


### 1.3 Testfälle

| TC-№ | Ausgangslage | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  |Konsole startet, warten auf Eingabe|Eingabe einer Auswahlmöglichkeit|Ausgabe von meiner eingegebener Auswahl|
| 1.2  |Konsole läuft, warten auf Eingabe|Eingabe von Botschaft| Ausgabe meiner Botschaft|
| 1.3  |Konsole läuft, Botschaft erhalten| Botschaft verschlüsseln/entschlüsseln| Ausgabe von verarbeiteter Botschaft|
| 1.4  |Konsole läuft| Warten auf Verarbeitung der Botschaft| Ausgabe von verarbeiteter Botschaft|
| 1.5  |Konsole läuft, Botschaft wurde ausgegeben| Nachfrage an Benutzer über erneute Eingabe| Ausgabe von Frage, ob Benutzer nochmals eine Eingabe tätigen will|
| 1.6  |Konsole läuft, warten auf Eingabe| Eingabe einer Antwort (j/n)| Je nach Antwort, Beenden des Programmes oder Ausgabe von Antwort|
| 1.7  |Konsole läuft, warten auf Eingabe| Fehlerhafte Eingabe| Ausgeben einer Fahlermeldung, anstatt von Shutdown|


### 1.4 Diagramme




## 2 Planen

| AP-№ | Frist | Zuständig | Beschreibung | geplante Zeit |
| ---- | ----- | --------- | ------------ | ------------- |
| 1.A  |  13.9.22     |Salma Tanner| Erstellen von Benutzereingaben für Zahl|45 Min|
| 2.A  |  13.9.22     |Salma Tanner| Erstellen von zufälligem Zahlengenerator|45 Min|
| 2.B  |  13.9.22     |Salma Tanner| Erstellen von Kontrolle für Benutzerzahl/Rückmeldung |45 Min|
| 3.A  |  13.9.22     |Salma Tanner| Ausgabe von Rückmeldung an Benutzer|45 Min|
| 4.A  |  06.9.22     |Salma Tanner| Bei ungültiger Eingabe, erneuter versuch anstelle von Programmm-Ende| 45 Min|
| 5.A  |  06.9.22     |Salma Tanner| Nach erraten der Zahl, werden gebrauchte Versuche ausgegeben| 45 Min|
Total: 6h




## 3 Entscheiden



## 4 Realisieren

| AP-№ | Datum | Zuständig | geplante Zeit | tatsächliche Zeit |
| ---- | ----- | --------- | ------------- | ----------------- |
| 1.A  |30.8.22|Salma Tanner|45min|15min|
| 2.A  |30.8.22|Salma Tanner|45min|15min|
| 2.B  |30.8.22|Salma Tanner|45min|30min|
| 3.A  |30.8.22|Salma Tanner|45min|30min|
| 4.A  |06.9.22|Salma Tanner|45min|45min|
| 5.A  |06.9.22|Salma Tanner|45min|45min|


## 5 Kontrollieren

### 5.1 Testprotokoll

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |13.9.22|Alles funktioniert, korrekte Ausgabe|Salma Tanner|
| 1.2  |13.9.22|Vollständige ausgabe|Salma Tanner|
| 1.3  |13.9.22|Funktioniert alles|Salma Tanner|
| 1.4  |13.9.22|Guter Umgang mit Fehleingabe, korrekt|Salma Tanner|
| 1.5  |13.9.22|Anzeigen der Versuche funktioniert|Salma Tanner|

Das Spiel funktioniert und beinhaltet alle Vorgaben. Jedoch hat es einen Fehler bei der Eingabe. Wenn man eine höhere Zahl als hundert eingibt, wird diese auch akzeptiert, nur bei etwas anderem als einer Zahl gibt es eine Fehlermeldung aus.

### 5.2 Exploratives Testen

| BR-№ | Ausgangslage | Eingabe | Erwartete Ausgabe | Tatsächliche Ausgabe |
| ---- | ------------ | ------- | ----------------- | -------------------- |
| I    |Benutzer-Eingabe einer Zahl über oder unter 1-100|Fehlermeldung, Aufforderung zur erneuter Eingabe|Rückmeldung, dass die Zahl zu klein oder zu gross ist|                      







# Ablauf

1.A Codieren/Decodieren programmiert
1.B Wiederholungslauf mithilfe von while-Schlaufe
2.A Fehler-Debugging
