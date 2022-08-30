Ab der DATAflor BUSINESS Version 2023 unterstützt der Digitale Posteingang den Import von Terminmengen in das DATAflor BUSINESS.

Der Import erfolgt über die Verzeichnisüberwachung (ein Import über die Programmoberfläche wird nicht unterstützt) und verwendet als Dateiformat XML. Der Dateiname der Importdatei spielt keine Rolle, die Dateiendung muss allerdings .xml sein. Das Encoding der Datei muss UTF-8 sein.

Der Aufbau der XML-Datei muss dem Schema DFTerminmengenImport.xsd entsprechen. Für einen erfolgreichen Import muss entweder das Feld IdPosition oder die Kombination aus den Feldern PosNr (Positions-Nr.) und LvNr (Leistungsverzeichnis-Nr.) einem Datensatz im DATAflor BUSINESS entsprechen.

Wenn ein Datensatz nicht zugeordnet werden kann oder sonstige Fehler enthält, wird die komplette Datei nicht importiert! Die importierte Datei wird dann (zusammen mit einer Fehlerbeschreibungsdatei, die den gefundenen Fehler beschreibt) in das Verzeichnis BusinessData\Inbox Files\failed (in der BUSINESS-Freigabe auf dem Server) verschoben.
