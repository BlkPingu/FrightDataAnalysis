# Einfluss der Trump-Präsidentschaft auf die Entwicklung des US-internationalen Güterhandels

###### Moritz Nötzel, Henriette Sand, Tobias Kolb

## 1 Problemformulierung

Ziel dieser Arbeit ist es, die Entwicklung des grenzüberschreitenden Güterhandels der USA mit Mexiko und Kanada seit dem Amtsantritt des amerikanischen Präsidenten Donald Trump im Jahr 2017 zu untersuchen. 

Das Hauptaugenmerk liegt hierbei auf Gütertransporten zwischen den USA und Mexiko. Bereits während des Wahlkampfes kündigte der Präsident an, die Grenze zwischen den beiden Ländern durch eine Mauer zu sichern uns somit dem Einwandererfluss Einhalt zu gebieten. Im Folgenden soll untersucht werden, ob diese feindliche Haltung den Güterhandel negativ beeinflusst oder ob es andere Faktoren sind, die den Umfang der Gütertransporte bestimmen. Es wird hypothesensuchend vorgegangen.

## 2 Grundlagen

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



#### 4.4 Model-Erstellung



## 5 Zusammenfassung



## 6 Diskussion



### Quellen

### Anhang



