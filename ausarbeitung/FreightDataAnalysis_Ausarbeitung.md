# Einfluss der Trump-Präsidentschaft auf die Entwicklung des US-internationalen Güterhandels

###### Moritz Nötzel, Henriette Sand, Tobias Kolb

## 1 Problemformulierung

Ziel dieser Arbeit ist es, die Entwicklung des grenzüberschreitenden Güterhandels der USA mit Mexiko und Kanada seit dem Amtsantritt des amerikanischen Präsidenten Donald Trump im Jahr 2017 zu untersuchen. 

Das Hauptaugenmerk liegt hierbei auf Gütertransporten zwischen den USA und Mexiko. Bereits während des Wahlkampfes kündigte der Präsident an, die Grenze zwischen den beiden Ländern durch eine Mauer zu sichern uns somit dem Einwandererfluss Einhalt zu gebieten. Im Folgenden soll untersucht werden, ob diese feindliche Haltung den Güterhandel negativ beeinflusst oder ob es andere Faktoren sind, die den Umfang der Gütertransporte bestimmen. Es wird hypothesensuchend vorgegangen.

## 2 Grundlagen

Am 8. November 2016 fand in den Vereinigten Staaten die 58. Präsidentschaftswahl statt. Mit 306 von 538 stimmen der Wahlmänner gewann der Republikaner Donald Trump gegen die demokratische Kandidatin Hilary Clinton (Quelle: https://www.bbc.com/news/election/us2016/results, letzter Aufruf: 24.06.2019, 14:57) Etwa zwei Monate später, am 20. Januar 2017 wurde er offiziell als 45. Präsident der Vereinigten Staaten vereidigt.

Bereits während des Wahlkampfes sorgte der Milliardär mit seiner "America First"-Politik für Aufsehen. Eines seiner kontroversten Wahlversprechen war es, entlang der Grenze zwischen den USA und Mexiko eine Mauer zu bauen. Die Kosten für dieses Vorhaben sollte die mexikanische Regierung tragen. (*Quelle*?)

Doch nicht nur im Bezug auf Mexiko stellt Trump die Beziehung zu den Nachbarländern in Frage. Auch die seit 1994 bestehende Freihandelsorganisation NAFTA, die Northamerican Foreign Trade Zone (Quelle: http://www.wirtschaftslexikon24.com/d/nafta/nafta.html, letzter Aufruf) kritisierte er stark. Das Abkommen schweißte die USA, Kanada und Mexiko zum größten Wirtschaftsraum der Welt zusammen. Unter Trumps Führung wurde NAFTA neu verhandelt und so unterzeichneten die drei Staaten am 30. November 2018 das United States-Mexico-Canada Agreement. (Quelle: https://ustr.gov/trade-agreements/free-trade-agreements/united-states-mexico-canada-agreement, letzter Aufruf: 24.06.2019)

## 3 Methodologie und Untersuchungsplanung

#### 3.1 Datenbeschaffung

Die Analyse beruht auf von dritten erhobenen Daten, die bereits strukturiert sind und die der Öffentlichkeit online zur freien Verfügung gestellt werden. Bevor die Daten weiter verarbeitet werden können, muss daher zuerst die Quelle überprüft werden. Hierbei ist insbesondere zu beachten, ob eine Lizenz zur Verbreitung der Daten vorliegt.

Anschließend muss überprüft werden, inwiefern die Daten sich für die Bearbeitung der Fragestellung eignen. Hierbei sind insbesondere der Zeitraum und die erfassten Merkmale von Bedeutung. Es müssen Daten vorliegen, die die Amtszeit von Donald Trump abbilden aber auch die Entwicklung der Jahre zuvor. Nur so lässt sich bestimmen, ob Trumps Politik irgendeine Auswirkung auf den Güterhandel mit Mexiko hat. 

Sollte die Untersuchung des Umfangs der Gütertransporte allein kein eindeutiges Ergebnis aufweisen, muss überprüft werden können, ob andere Faktoren den internationalen Handel bestimmen. Hierbei können sowohl wirtschaftliche, politische, geographische als auch soziale Sachverhalte eine Rolle spielen. Diese müssen in irgendeiner Form in den daten wiederzufinden sein.

#### 3.2 Datenpräparation

Da die Daten bereits in strukturierten Datensätzen vorliegen, steht bei der Datenpräparation die Aggregation und Konsolidierung im Vordergrund. Die Daten sind auf eine Vielzahl von Datensätzen verteilt und liegen in mehrfacher Ausführung und in unterschiedlichen Formaten vor. Dafür muss in einem ersten Schritt entschieden werden, welches Format die Merkmale dokumentiert, die für unsere Fragestellung am relevantesten sind. Dazu muss das Benennungsschema der einzelnen Dateien identifiziert und die in den Datensätzen genutzten Codes interpretiert werden. Erklärungen zu den Codes sind auf der Webseite des Bureau of Transportation Statistics einsehbar, für die Klärung des Benennungsschema ist eine elektronische Anfrage beim U.S. Department of Transportation erforderlich. 

Sofern Schritt Eins abgeschlossen ist und ein Konsens über das Format der weiterzuverarbeitenden Daten vorliegt, müssen die einzelnen Datensätze zusammengeführt werden.  Dafür wird der Tad Viewer verwendet, der Funktionen zum Anzeigen und Analysieren von Daten bereitstellt. Zuerst werden die entsprechenden Datensätze der jeweiligen Jahre zusammengeführt, anschließend nach Handelspartner gefiltert und die gefilterten Listen als neue CSV-Datei exportiert. An dieser Stelle wird auch kontrolliert, ob der Umfang der Daten ausreichend ist.

Im dritten Schritt muss die Qualität der Daten überprüft und die Datensätze gegebenenfalls gesäubert werden. Hierbei sind insbesondere Lücken in der Zeiterfassung und fehlende Werte zu beachten. Da die Analyse explorativen Charakter hat,  müssen darüber hinaus keine Informationen extrahiert werden. 

Am Ende der Datenpräparation steht die Portierung in den Arbeitsbereich. Dies beeinhaltet an erster Stelle die Gewährleistung, dass alle Teammitglieder den selben Datensatz als Quelle nutzen.

#### 3.3 Exploration

Für die Exploration wird vorrangig der Python Data Science Stack verwendet. Die bevorzugte Programmierumgebung ist Jupyter Notebook. Verschiedene beleuchtete Aspekte werden jeweils in eigenen Notebooks untersucht und Zwischenergebnisse zur Weiterverwendung in CSV-Dateien exportiert. Die Teammitglieder nutzen Git, um ihre Ergebnisse auszutauschen. 

Neben den numerischen Ergebnissen der Auswertung werden Grafiken erstellt um die Ergebnisse zu visualisieren. 

Zu untersuchende Aspekte sind:

- der Umfang des jährlichen Gütertransports je Handelspartner über den Verlauf des Beobachtungszeitraumes
- Die Verteilung des Gütertransports auf Import und Export
- Die Verteilung des Gütertransports auf die einzelnen US-Staaten

Weitere Untersuchungspunkte ergeben sich basierend auf den ermittelten Ergebnissen. Ziel der Exploration ist die Aufstellung von Hypothesen zur Verfeinerung der Forschungsfrage.

#### 3.4 Model-Erstellung

Basierend auf den Ergebnissen der Explorationsphase soll ein Modell zur Entwicklung des grenzüberschreitenden Gütertransports entwickelt werden, das die Auswirkung verschiedener Einflussfaktoren darstellt. Zu diesem Zweck werden verschiedene Hypothesen geprüft und anschließend angenommen oder verworfen. Ein besonderes Augenmerk liegt hierbei auf der Beurteilung der Passfähigkeit des Modells im Kontext des Problems. Hierbei wird auch die Möglichkeit berücksichtigt, dass sich aus den vorhandenen Daten kein passendes Modell generieren lässt. In diesem Fall muss abschließend analysiert werden, welche Gründe dies haben könnte. 

## 4 Untersuchungsdurchführung und Ergebnisse

#### 4.1 Datenbeschaffung

Den Ausgangspunkt unserer Untersuchung bilden Rohdaten, die  vom U.S. Department of Transportation auf der Webseite des Bureau of Transportation Statistics kosten- und lizenzfrei zur Verfügung gestellt werden. Es handelt sich um einen strukturierten Datensatz, der auf mehrere Quellen verteilt ist. Enthalten sind Daten zum grenzüberschreitenden Güterhandel der USA mit Canada und Mexico.  Betrachtet werden hierbei einzelne Warentransporte, wobei Informationen zu folgenden Merkmalen erhoben wurden:

- Monat und Jahr
- Handelspartner
- Handelsart: Import oder Export
- US-Staat 
- Wert der Lieferung in US-Dollar
- Gewicht der Lieferung
- Kanadische Provinz bzw. mexikanischer Staat
- Warengruppe
- Transportmittel
- US-Port

Vorhanden sind Daten der Jahre 1993 bis 2019. Allerdings liegen nur die Datensätze des Jahres 2007 und jünger im aktuellen Datenformat vor, weshalb wir hier bereits eine erste Beschränkung des Beobachtungszeitraumes vorgenommen haben. Die Daten sind nach Jahr sortiert bereitgestellt. Pro Datensatz werden einzelne Monate bzw. der Jahresposten bis zum jeweiligen Monat dargestellt. Zudem gibt es drei unterschiedliche Formate, in denen die Daten abgebildet sind. Um welches Format es sich handelt und welche Eigenschaften im jeweiligen Datensatz enthaltet sind, ist am Dateinamen ablesbar:

- 1: US-Staat und US-Port
- 2: US-Staat und Warengruppe
- 3:  US-Port und Warengruppe

Dieser enthält außerdem Informationen zum Jahr und Monat. Datensätze, in denen Daten aus mehreren Monaten gesammelt sind, sind mit "ytd" (year to date) gekennzeichnet. Für unsere Analysen beschränken wir uns auf Datensätze, die ein komplettes Jahr abbilden. Da die Entwicklung der Handelsbeziehung über mehrere Jahre betrachtet wird, sind Monate als die kleinste Granularität ausreichend. 

Um die Auswirkung der Politik von US-Präsident Donald Trump analysieren zu können, muss der Beobachtungszeitraum mindestens die Jahre seiner Amtszeit umfassen. Zählt man das Wahljahr 2016 hinzu ergäbe das einen Zeitraum von vier Jahren: 2016-2019. Da das Jahr 2019 allerdings noch nicht sehr weit fortgeschritten ist, liegt nur ein unvollständiger Datensatz vor. Um einer Verfälschung der Ergebnisse vorzubeugen, wird 2019 daher nicht berücksichtigt. 

Im Zentrum unserer Analyse steht die Frage, ob der Güterhandel zwischen den USA und Mexico durch die Mexiko-feindliche Politik Trumps beeinträchtigt wird. Es ist daher auch von Bedeutung, die Entwicklung der Handelsbeziehung vor der Trump-Administration zu untersuchen. Um eine möglichst realitätsgetreue Darstellung dieses Zeitraumes zu erhalten, betrachten wir daher zunächst alle im aktuellen Format vorhandenen Datensätze (2007-2015), um dann später eine engere Eingrenzung vornehmen zu können. 

Da Donald Trump's Ideologie in der US-Amerikanischen Bevölkerung unterschiedlich viel Zuspruch bekommt, ist für unsere Untersuchung auch relevant, wie sich der Güterhandel auf die einzelnen Staaten verteilt. Wir beschränken uns daher auf Datensätze, die dieses Merkmal berücksichtigen und arbeiten ausschließlich mit solchen, deren Dateiname mit der Ziffer 2 gekennzeichnet ist.

Um darüber hinaus sicherstellen zu können, dass es sich tatsächlich um Mexiko-spezifische Entwicklungen handelt, schauen wir uns vergleichsweise ebenfalls die Handelsbeziehung mit Canada in diesem Zeitraum an.

#### 4.2 Datenpräparation

Da die vorhandenen Rohdaten nun eingegrenzt sind, muss als nächstes die Qualität der Daten überprüft werden. Hierbei fällt auf, dass im Jahr 2009 mehrere Monate nicht erfasst wurden. 2009 kann daher in der Model-Erstellung nicht berücksichtigt werden, was eine weitere Eingrenzung des Beobachtungszeitraumes bedeutet. 

Hinderlich für die Analyse ist außerdem die Aufteilung der Daten in verschiedene Dateien. Der zweite Schritt ist daher die Aggregation. Die Datensätze werden zu einem großen zusammengefasst, der die Jahre 2007-2018 ohne 2009 beinhaltet. Diese Datei wird dann nochmals gefiltert und Daten zum Handel mit Mexiko von denen zum Handel mit Canada getrennt. Das Ergebnis sind zwei gefilterte Datensätze, die jeweils mehrere Millionen Einträge enthalten und die Grundlage für die Exploration bilden. Im weiteren Verlauf der Untersuchung werden diese weiter angepasst und eingegrenzt. 

Da der Datensatz bereits einem bestimmten Format entspricht, muss keine Normalisierung vorgenommen werden. Es wird jedoch ersichtlich, dass bei einigen Transporten kein Wert für das Liefergewicht aufgezeichnet wurde. Dieser eignet sich also nicht, um den Umfang der Transporte zu bestimmen und die Spalte kann entfernt werden.

Abschließend erfolgt die Portierung in den Arbeitsbereich. Dies bedeutete in unserem Fall, dass die Dateien per GoogleDrive mit allen Teammitgliedern geteilt und dann vom jeweiligen Bearbeiter in die bevorzugte Programmierumgebung importiert werden.

#### 4.3 Exploration

Zu Beginn der Exploration muss festgelegt werden, wonach der Umfang der Transporte bemessen wird. Hier kommen nur zwei Einheiten infrage: Die absolute Anzahl der grenzüberschreitenden Transporte oder der monetäre Wert in US-Dollar. Alle folgenden Berechnungen nutzen den monetären Wert als Vergleichsmaß. 

Als Ausgangspunkt für die Exploration eignet sich ein grober Überblick über den jährlichen Umfang der Gütertransporte. Die folgenden Diagramme spiegeln die Entwicklung zwischen 2013 und 2018 wieder.

![TotalMX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\TotalMX.png)

![TotalCA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\TotalCA.png)

Diese Werte lassen sich nochmals verfeinern, indem Export und Import getrennt von einander betrachtet werden:

###### Mexico

![ExportMX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\ExportMX.png)

![ImportMX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\ImportMX.png)

###### Canada 

![ExportCA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\ExportCA.png)

![ImportCA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\ImportCA.png)

Beim Vergleich der Mittelwerte erkennt man hier bereits, dass der Güterhandel mit Canada deutlich ausgeprägter ist als der mit Mexiko.

###### Mexiko

![meanMX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\meanMX.png)

###### Canada

![1561468328344](C:\Users\henni\AppData\Roaming\Typora\typora-user-images\1561468328344.png)

Aufgrund der flächenmäßigen Größe der USA und den damit einhergehenden Unterschieden zwischen verschiedenen Regionen bezüglich politischer Einstellung, Bevölkerungsdichte und geographischen Gegebenheiten, bietet es sich an, in einem nächsten Schritt die Verteilung dieser Handelsmengen auf die einzelnen Staaten zu untersuchen. 

Allein bei der Betrachtung des Jahres 2018 wird hier deutlich, dass es bedeutende Diskrepanzen zwischen dem Handelsvolumen der einzelnen Staaten gibt und dass sich diese Verteilung auch bei Transporten nach und von Mexico und nach und von Canada unterscheiden. 

###### Mexico

![StatesExport2018MX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\StatesExport2018MX.png)

![StatesImport2018MX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\StatesImport2018MX.png)

###### Canada

![StatesExport2018CA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\StatesExport2018CA.png)

![StatesImport2018CA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\StatesImport2018CA.png)

Es fällt auf, dass der Jahresumsatz von Waren, die die amerikanische Grenze überqueren, in den Staaten besonders hoch ist, die dem Handelspartner geographisch besonders nahe liegen. Daher empfiehlt sich die Untersuchung der Transportmittel, die für die Transporte zum Einsatz kommen. 

Im Jahr 2018 gestaltete diese sich wie folgt:

![DisagmotMX2018](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\DisagmotMX2018.png)

![DisagmitCA2018](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\DisagmitCA2018.png)

Das meist genutzte Transportmittel ist unverkenntlich der Truck. Ein Vergleich der jährlichen Trucktransporte im Beobachtungszeitraum zeigt auf, dass der Einsatz dieser Lastenträger tendenziell steigend ist.

![TruckMX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\TruckMX.png)

![TruckCA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\TruckCA.png)

Daraus leitet sich die Frage ab, ob sich das auch bezogen auf einzelne, handelsstarke US-Staaten so verhält. Betrachten wir also Mexikos stärksten Ex- und Importeur Texas.

![DisagmotExTX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\DisagmotExTX.png)



![DisagmotImTX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\DisagmotImTX.png)

In beide Richtungen werden Waren hauptsächlich per Truck transportiert. Ein ähnliches Bild zeichnet sich ab, wenn man sich den Warenfluss zwischen Michigan und Canada anschaut:

![DisagmotExMI](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\DisagmotExMI.png)

![DisagmotExMI](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\DisagmotImMI.png)

Es lohnt sich also, einen Blick auf die Karte der Vereinigten Staaten zu werfen:

*Heatmap + Legende*

Texas und Michigan stechen aufgrund der hohen Transportraten hervor. Doch noch ein weiterer Aspekt fällt auf: beide US-Staaten grenzen an das Nachbarland an, mit dem aktiv Handel betrieben wird. Basierend auf diesen Ergebnissen lässt sich die Hypothese aufstellen, dass das Handelsvolumen der einzelnen Staaten von der geographischen Nähe zum Handelspartner abhängt. Diese Hypothese soll im späteren Verlauf der Arbeit noch überprüft werden. 

Trumps Politik stellt mit seiner "America First"-Philosophie die Belange des Landes an die erste Stelle, insbesondere in wirtschaftlicher Hinsicht. Er setzt auf wirtschaftspolitischen Nationalismus. Es ist daher naheliegend anzunehmen, dass ein Interesse besteht, den Import von Waren zu reduzieren und somit den Geldfluss in Nachbarsländer zu minimieren. Insbesondere in Staaten, deren Stimmen in der Wahl 2016 an den republikanischen Kandidaten gingen, sollte daher eine Abnahme des Imports aus Mexico und Canada zu erkennen sein. Betrachtet man beispielsweise den Import aus Mexiko des vorwiegend republikanische Louisianas (Quelle: https://www.nytimes.com/elections/2016/results/president, letzter Zugriff: 24.06.2019, 24.06.2019) über die letzten 10 Jahre, so lässt sich eine solche Tendenz erkennen:

![ImportLA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\ImportLA.png)

Daraus ergibt sich eine weitere Hypothese, um die Entwicklung der Handelsbeziehungen seit Trumps Amtseintritt zu beschreiben: In Staaten, deren Stimmen an Präsidentschaftskandidat Donald Trump gingen, reduzierte sich nach der Wahl 2016 der Import.

#### 4.4 Model-Erstellung

Welche politische Einstellung in den einzelnen Staaten vorherrschend ist, lässt sich anhand der Stimmenverteilung in der Präsidentschaftswahl 2016 beurteilen:

![wahlergebnis2016](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\wahlergebnis2016.jpg)



*Bildquelle?*

Nun gilt es zu prüfen, ob in diesen Staaten der Güterhandel seit 2016 zurückgegangen ist. Da eine Reduktion des Exports auch eine Senkung von Einnahmequellen für die einzelnen Staaten bedeuten würde und dies nicht der "America First"-Philosophie entspricht, konzentriert sich die Untersuchung auf den Import aus Mexiko. 

##### Importvolumen in republikanischen Staaten

###### H0: In Staaten, die in der Präsidentschaftswahl 2016 für Donald Trump gestimmt haben, reduzierte sich der Import nach Amtsantritt nicht. 

###### H1: In Staaten, die in der Präsidentschaftswahl 2016 für Donald Trump gestimmt haben, reduzierte sich nach Amtsantritt der Import aus Mexiko

Da Trump im Januar 2017 ins Amt gehoben wurde, muss hier das Importvolumen aus dem Jahr 2016 gegen das Importvolumen des Jahres 2017 abgewogen werden. Damit ergibt sich folgendes Hypothesenpaar:

**H0: µ17 >= µ16**

**H1: µ17 < µ16** 

Betrachtet wird das arithmetische Mittel der Monate des jeweiligen Jahrs.

Erinnern wir uns zurück an die Verteilung des Importvolumens auf einzelne US-Staaten. 2016 und 2017 sah diese folgendermaßen aus: 

![StatesImport16](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\StatesImport16.png)

![StatesImport17](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\StatesImport17.png)

Von den Staaten, die ein besonders hohes Importvolumen aufweisen, haben folgende 2016 ihre Stimmen Donald Trump gegeben: Alabama, Arizona, Texas, Florida, Georgia, Kentucky, North Carolina, Pennsylvania und Tennessee. Bei Anwendung des Hypothesenpaars auf die einzelnen Staaten erhält man folgende Ergebnisse: 

Anmerkung: Getestet wird jeweils die Nullhypothese

###### Alabama

```
print("Rein Value Vergleich: ", sum(df_17_al) > sum(df_16_al))
print(sum(df_16_al)/float(len(df_16_al)))
print(sum(df_17_al)/float(len(df_17_al)))
print(sum(df_17_al)/float(len(df_17_al)) > sum(df_16_al)/float(len(df_16_al)))
```

![Alabama](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\Alabama.png)

###### Arizona

Vergleich der reinen Werte: True

µ16: 621196836.9166666

µ17: 659659908.0

µ17 > µ16:  True



###### Texas

Vergleich der reinen Werte: True

µ16: 6753110302.166667

µ17: 7486071020.0

µ17 > µ16: True



###### Florida

Vergleich der reinen Werte: True

µ16: 482607344.5

µ17: 557353266.8333334

µ17 > µ16: True



###### Georgia

Vergleich der reinen Werte: True

µ16: 539118299.8333334

µ17: 571555194.0

µ17 > µ16: True



###### Kentucky

Vergleich der reinen Werte: True

µ16: 433310505.5

µ17: 466582918.3333333

µ17 > µ16: True



###### North Carolina

Vergleich der reinen Werte: True

µ16: 382191389.75

µ17: 394413212.5833333

µ17 > µ16: True



###### Ohio

Vergleich der reinen Werte: True

µ16: 663132856.25

µ17: 687423467.9166666

µ17 > µ16: True



###### Pennsylvania

Vergleich der reinen Werte: True

µ16: 335496777.4166667

µ17: 448847049.1666667

µ17 > µ16: True



###### Tennesee

Vergleich der reinen Werte: False

µ16: 610443682.5

µ17: 588397981.4166666

µ17 > µ16: False



Mit der Ausnahme von Tennessee wird bei allen Staaten die Nullhypothese angenommen. Der Import ist in den republikanisch gesonnen Staaten also nicht nur konstant geblieben, er ist sogar gestiegen. Dies wird auch deutlich, wenn man sich die Entwicklung des monatlichen Importvolumens von Texas über die zwei Jahre anschaut: 

![MonthsTX](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\MonthsTX.png)

Die Alternativhypothese, dass sich in Trump-affinen Staaten nach der Wahl 2016 der Import reduzierte, muss abgelehnt werden. Ein Modell, dass die Verbindung zwischen der politischen Einstellung eines Staates und seinen Handelsaktivitäten mit den Nachbarländern beschreibt, kann nicht erstellt werden. 

Es ist also notwendig, noch andere Faktoren zu berücksichtigen. Die Ergebnisse der Explorationsphase deuten auf einen Zusammenhang zwischen der Entfernung eines US-Staates zum Handelspartner und den transportierten Waren hin. Bei der Überprüfung dieser Hypothese müssen die Handelsbeziehungen mit Mexiko und Canada einzeln betrachtet werden. Es müssen also zwei Hypothesentests durchgeführt werden.

##### Warentransporte zwischen den USA und Mexiko

Gearbeitet wird mit folgenden Hypothesen:

###### H0: Das Handelsvolumen der einzelnen US-Staaten hängt nicht von der Nähe zu Mexiko ab. 

###### H1: Das Handelsvolumen der einzelnen US-Staaten hängt von der Nähe zu Mexiko ab.

Daraus ergibt sich folgendes Hypothesenpaar:

**H0: µdis != µval**

**H1: µdis = µval** 

Um diese Hypothese überprüfen zu können, muss zunächst definiert werden, welche Staaten "nah" an Mexiko liegen. Dazu werden sie manuell in drei Gruppen eingeteilt: 

| Entfernungs-Gruppe                    | Anzahl Staaten |
| ------------------------------------- | -------------- |
| 1: keine/geringe Entfernung zu Mexiko | 5              |
| 2: mittlere Entfernung zu Mexiko      | 14             |
| 3: große Entfernung zu Mexiko         | 33             |

Basierend auf den Größenordnungen dieser Gruppen, müssen die Staaten nun nach ihrem jährlichen Umsatz an grenzüberschreitenden Transporten gruppiert werden. Genutzt wird dafür jeweils das arithmetische Mittel des Jahreswertes in US-Dollar über den Beobachtungszeitraum von 2013 bis 2018. Dabei entsteht folgende Verteilung:

| Wert-Gruppe                                        | Anzahl Staaten |
| -------------------------------------------------- | -------------- |
| 1: hoher jährlicher Transportwert in US-Dollar     | 5              |
| 2: mittlerer jährlicher Transportwert in US-Dollar | 14             |
| 3: niedriger jährlicher Transportwert in US-Dollar | 33             |

Die Entfernungs-Gruppen müssen getrennt voneinander gegen die entsprechende Wert-Gruppe getestet werden. Da die beiden Stichproben aus der selben Grundgesamtheit stammen, kann angenommen werden, dass sie die selben Varianzen haben. 

###### Test 1: geringe Entfernung zu Mexiko und großer Transportwert

```
# |T| ermitteln
t.test(dis1[,1], val1[,1], var.equal = TRUE)
```

![t.test1](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\t.test1.png)

```
# T* ermitteln
qt(p = 0.05/2, df = 8, lower.tail = FALSE)
```

**Ergebnis:**

|T| = -0.2933

T* = 2.30600413520417

|T| < T* Nullhypothese annehmen, Alternativhypothese ablehnen



###### Test 2: mittlere Entfernung zu Mexiko und mittlerer Transportwert

```
# |T| ermitteln
t.test(dis2[,1], val2[,1], var.equal = TRUE)
```

![t.test2](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\t.test2.png)

```
# T* ermitteln
qt(p = 0.05/2, df = 26, lower.tail = FALSE)
```

**Ergebnis**

|T| = -3.2433

T* = 2.05552943864287

|T| < T* Nullhypothese annehmen, Alternativhypothese verwerfen



###### Test 3: große Entfernung zu Mexiko und niedriger Transportwert

```
# |T| ermitteln
t.test(dis3[,1], val3[,1], var.equal = TRUE)
```

![t.test3](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\t.test3.png)

```
# T* ermitteln
qt(p = 0.05, df = 64, lower.tail = FALSE)
```

**Ergebnis** 

|T| = 1.9244

T* = 1.66901302502409

|T| > T* Nullhypothese verwerfen, Alternativhypothese annehmen



Selbst unter Berücksichtigung eines möglichen Fehlers muss bei zwei von drei Tests die Alternativhypothese abgelehnt werden. Es gilt: **H0: µdis != µval** 

Die Analyse der jährlichen Transporte von und nach Mexiko weist also nicht daraufhin, dass die Entfernung zum Handelspartner das entscheidende Kriterium für den Umfang der grenzüberschreitenden Warentransporte ist. Es gilt also nun zu überpüfen, wie sich dies in Bezug auf Canada verhält.

###### Warentransporte zwischen den USA und Canada

Analog zur Analyse der Handelsbeziehung mit Mexiko lauten die Hypothesen für Canda wie folgt:

###### H0: Das Handelsvolumen der einzelnen US-Staaten hängt nicht von der Nähe zu Canada ab. 

###### H1: Das Handelsvolumen der einzelnen US-Staaten hängt von der Nähe zu Canada ab.

Und das dazugehörige Hypothesenpaar: 

**H0: µdis != µval**

**H1: µdis = µval** 

Wieder müssen die Daten zuerst nach den Kriterien "Entfernung zu Canada" und "jährlicher Transportwert in US-Dollar" gruppiert werden.

| Entfernungs-Gruppe                    | Anzahl Staaten |
| ------------------------------------- | -------------- |
| 1: keine/geringe Entfernung zu Canada | 16             |
| 2: mittlere Entfernung zu Canada      | 23             |
| 3: große Entfernung zu Canada         | 13             |

| Wert-Gruppe                                        | Anzahl Staaten |
| -------------------------------------------------- | -------------- |
| 1: hoher jährlicher Transportwert in US-Dollar     | 16             |
| 2: mittlerer jährlicher Transportwert in US-Dollar | 23             |
| 3: niedriger jährlicher Transportwert in US-Dollar | 13             |

Auch hier müssen wieder drei separate Tests durchgeführt werden.

###### Test 1: geringe Entfernung zu Mexiko und großer Transportwert

```
# |T| ermitteln
t.test(dis1[,1], val1[,1], var.equal = TRUE)
```

![t.test1CA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\t.test1CA.png)

```
# T* ermitteln
qt(p = 0.05/2, df = 30, lower.tail = FALSE)
```

**Ergebnis:**

|T| = -1.1191

T* = 2.04227245630124

|T| < T* Nullhypothese annehmen, Alternativhypothese verwerfen



###### Test 2: mittlere Entfernung zu Mexiko und mittlerer Transportwert

```
# |T| ermitteln
t.test(dis2[,1], val2[,1], var.equal = TRUE)
```

![t.test2CA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\t.test2CA.png)

```
# T* ermitteln
qt(p = 0.05/2, df = 44, lower.tail = FALSE)
```

**Ergebnis**

|T| = 0.16644

T* = 2.01536757444376

|T| < T* Nullhypothese annehmen, Alternativhypothese verwerfen



###### Test 3: große Entfernung zu Mexiko und niedriger Transportwert

```
# |T| ermitteln
t.test(dis3[,1], val3[,1], var.equal = TRUE)
```

![t.test3CA](C:\Users\henni\Documents\HTW - Angewandte Informatik\Viertes Semester\Grundlagen_Data_Science\FreightDataAnalysis\ausarbeitung\bilder\t.test3CA.png)

```
# T* ermitteln
qt(p = 0.05, df = 24, lower.tail = FALSE)
```

**Ergebnis** 

|T| = 2.146

T* = 1.71088207990943

|T| > T* Nullhypothese verwerfen, Alternativhypothese annehmen

Das Ergebnis der Analyse des Gütertransports zwischen den einzelnen US-Staaten und Canada gleicht dem mit Mexiko: Nur in der letzten Gruppe lässt sich ein eindeutiger Zusammenhang erkennen. Wieder gilt:  **H0: µdis != µval**

Es kann also nicht pauschalisiert werden, dass die Entfernung zum Handelspartner im direkten Zusammenhang zum wertmäßigen Umfang des Güterhandels steht. Es kann jedoch statiert werden, dass die Wahrscheinlichkeit, dass ein US-Staat umfassende grenzüberschreitende Warentransporte in ein Nachbarland verzeichnet, mit zunehmender geographischer Distanz zur Grenze sinkt. 

Um ein passendes Modell im Kontext der Trump-Administration zu erstellen, reicht diese Aussage jedoch nicht.

## 5 Zusammenfassung

Ausgangspunkt für die Analyse der Daten zu Warentransporten über die US-amerikanischen Grenzen war die "America First"-Politik des aktuellen US-Präsidenten Donald Trump. Das Vorhaben, die amerikanisch-mexikanische Grenze durch eine Mauer zu sichern, sowie die Überarbeitung NAFTAs, ließen einen Rückgang des Güterflusses erwarten. Bereits zu Beginn der Explorationsphase jedoch wurde ersichtlich, dass eine bloße Auswertung des jährlichen Gesamtumsatzes diesbezüglich zu keinem eindeutigen Ergebnis führen würde. Die explorativ-hypothesensuchende Vorgehensweise war daher von Vorteil.

Entscheidend für den Verlauf der Analyse war die Meinungsverschiedenheit, die innerhalb der amerikanischen Bevölkerung bezüglich der Politik Trumps vorherrscht. Die Stimmenverteilung der Präsidentschaftswahl im Jahr 2016 ermöglichte eine Untersuchung einzelner Staaten. Dabei konnte zwar für den Beobachtungszeitraum keine politisch beeinflusste Auswirkung auf Handelstätigkeiten identifiziert werden, jedoch weitete sich das Verständnis für das Zusammenspiel verschiedener Faktoren, die den Umfang der Warentransporte bestimmen. So konnte herausgestellt werden, dass ein Zusammenhang zwischen der geographischen Distanz zum Handelspartner und den gegenseitigen Warenlieferungen besteht. Dennoch wurde außerdem deutlich, dass diese Verbindung kritisch zu beurteilen ist. Für die Erstellung eines zuverlässigen Models waren die Ergebnisse nicht hinreichend.

## 6 Diskussion

Zusammenfassend lässt sich sagen, dass Trumps aggressive Haltung gegenüber Mexiko in wirtschaftlicher Hinsicht keine Auswirkungen zu haben scheint. Nun muss allerdings berücksichtigt werden, dass nur Messwerte zu den ersten zwei Jahren seiner Amtszeit als US-amerikanischer Präsident vorliegen. Die Unterzeichnung des neu verhandelten United States-Mexico-Canada Agreement fand erst am Ende des Beobachtungszeitraumes statt, sodass von den vorhandenen Daten nicht auf die zukünftige Entwicklung geschlossen werden kann. 

In dieser Hinsicht wäre es vorteilhafter gewesen, den Güterhandel unabhängig von Trumps Politik zu betrachten. Der zugrundeliegende Datensatz liefert weitaus mehr Informationen, als in der Analyse berücksichtigt wurden. 

So hätte die geographische Analyse der einzelnen Staaten viel weiter ausgebaut werden können. Neben der Distanz zum Handelspartner spielen auch Faktoren wie Fläche, Bevölkerungszahl und Infrastruktur eine Rolle. Ein solcher Ansatz hätte möglicherweise Untersuchungsbefunde generiert, die auch extern valide sind. 

Sofern die zugrundeliegenden Rohdaten nicht erweitert werden erfordern weiterführende Untersuchungen also eine Überarbeitung der Problemformulierung und eine Neueinbettung in einen passenderen Kontext.

### Quellen

### Anhang

- TotalImportExportValuesByCountry
- GeographicAnalysis-MX
- GeographicAnalysis-CA
- Code für Heatmaps mit Name und Matrikelnummer von Tobias
- Trump-Staaten-Analyse mit Name und Matrikelnummer von Moritz

