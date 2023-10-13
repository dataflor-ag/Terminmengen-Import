<dl>
<b>Ab der DATAflor BUSINESS Version 2023 unterstützt der Digitale Posteingang den Import von Terminmengen in das DATAflor BUSINESS.</b>
</dl>

Der Import erfolgt über die Verzeichnisüberwachung (ein Import über die Programmoberfläche wird nicht unterstützt) und verwendet als Dateiformat XML. Der Dateiname der Importdatei spielt keine Rolle, die Dateiendung muss allerdings .xml sein. Das Encoding der Datei muss UTF-8 sein.

Der Aufbau der XML-Datei muss dem Schema DFTerminmengenImport.xsd entsprechen. Für einen erfolgreichen Import muss entweder das Feld IdPosition oder die Kombination aus den Feldern PosNr (Positions-Nr.) und LvNr (Leistungsverzeichnis-Nr.) einem Datensatz im DATAflor BUSINESS entsprechen.

Wenn ein Datensatz nicht zugeordnet werden kann oder sonstige Fehler enthält, wird die komplette Datei nicht importiert! Die importierte Datei wird dann (zusammen mit einer Fehlerbeschreibungsdatei, die den gefundenen Fehler beschreibt) in das Verzeichnis BusinessData\Inbox Files\failed (in der BUSINESS-Freigabe auf dem Server) verschoben.


<dl>
<b>Import von Terminmengen für die Abrechnung von Pflege-LV mit dem BUSINESS-Stapeldruck</b>
</dl>
Ziel: 

Ein beauftragter Pflegegang wird in Eurer Anwendung als erledigt gekennzeichnet und diese Meldung wird mittels XML-Datei
als Terminmenge an das Auftrags-LV übertragen. Dort steht die Terminmenge für die Abrechnung mittels Stapeldruck zur Verfügung.
Diese Meldung ist unabhängig von der Zeiterfassung.

Voraussetzung: Terminmengen können nur einem LV und Positionen zugeordnet werden die das Kennzeichen „Terminabrechnung“ haben.
Denn nur dann kann der Rechnungsdruck die Daten verarbeiten.
Auf diese Felder solltet Ihr bei der Erfassung der Positionen prüfen:

LV hier: 
![image](https://user-images.githubusercontent.com/111848298/198053256-879e50ff-6253-45f5-a080-3f297405e9d0.png)
      
Tabelle LV_DATA  Feld IS_TERMIN_ABRECHNUNG=1


Positionen hier:
![image](https://user-images.githubusercontent.com/111848298/198055571-9a763603-639b-4a4d-bae0-96b2deda64e0.png)
           
Tabelle POSITIONEN_DATA  Feld  IS_TERMIN_ABRECHNUNG=1 und Feld ABRECHNUNGSART_PFLEGE = 1 oder 2

Ergänzung: Die übergebene Terminmenge im nummerischen Format kann mit einem Punkt oder Komma als Dezimaltrennzeichen übergeben werden.
