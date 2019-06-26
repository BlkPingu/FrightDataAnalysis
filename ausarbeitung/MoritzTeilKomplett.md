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