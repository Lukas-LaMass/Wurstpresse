# Wurstpresse
## Description
The Wurstpresse is a simple script in Jupyter Notebook developed in the Project "FAIR.rdm" in the SPP2143 "Entangled Africa" to support the curation and import workflow for pictures into the database iDAI.objects (Arachne).
The Jupyter-Notebook-file consists of annotations in markdown and codeblocks in python, which have to be executed one by one. The structure and the python code are very simple and straightvorward, so anyone with a basic unterstanding of python code could use the script and edit it easily.
The current Version is 2.0 (April 2026).

## Changelog der Wurstpresse

Die Version 2.0 wurde an HacVia angepasst. Da nun ausschließlich Entity IDs verwendet werden konnten viele Funktionen im Zusammenhang mit alten Seriennumern entfernt werden. Außerdem wird die laufende Nummer nun über die API aktualisiert.

Version 2.1 (30.04.2026)

Schritt 2.2 verwendet jetzt ein Set anstelle eine Liste. Dies beschleunigt den Abgleich über die API, da Mehrfachabfragen der gleichen Entity ID vermieden werden.

Im selben Schritt wurde ein Fallback eingebaut, falls die REST API etwas anderes als 200 meldet. Bspw. bei verstecken Datensätzen 403. In diesem Fall wird die laufende Nummer aus dem lokalen Bestand weitergezählt.

Der Fortschrittsindikator in 4.2 funktioniert nun richtig; er zählt bis 100 % und nicht darüber hinaus.

Fortschrittsindikator in 4.3 hinzugefügt.

Das Limit für die Größe von ZIP-Dateien in HacVia sind 20 GB. Die Wurstpresse überprüft nun, ob ein ZIP-Verzeichnis diese Grenze überschreitet und erzeugt ggf. weitere ZIP-Archive.

Unter 1.1 Variable für das Trennzeichen einer CSV eingefügt.
