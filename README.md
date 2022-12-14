# Wurstpresse
## Description
The Wurstpresse is a simple Script in Jupyter Notebook developed in the Project "FAIR.rdm" in the SPP2143 "Entangled Africa" to support the curation and import workflow for pictures into the database iDAI.objects (Arachne).
The Jupyter-Notebook-file consists of annotations in markdown and codeblocks in python, which have to be executed one by one. The structure and the python code are very simple and straightvorward, so anyone with a basic unterstanding of python code could use the script and edit it easily.
The current Version is 1.7 (December 2022).
## Changelog (in German)
Die Version 1.5 der Wurstpresse vom März 2022 erfüllte folgende Aufgaben:
- automatisches Umbenennen der Bilder nach einer vorgegebenen Konkordanz, welches Bild zu welcher Seriennummer gehört
- Erfassung des Stands der laufenden Nummer der Bildbestände zu jeder Seriennummer
- Verschieben der Bilder in die für den Import benötigen Ordnerstrukturen und ggf. Erstellung dieser Strukturen

Änderungen in der Version 1.6 vom Oktober 2022:
- Das Skript liest nun eine CSV-Tabelle ein, in der die Fundplatzhierarchie dargestellt ist.
- Das Skrpt liest nun eine CSV Tabelle ein, in der alle Lokalisierungsbezeichnungen und die zugehörigen Seriennummern aufgelistet sind (Seriennummer-Tieltel-Konkordanz)
- Mit diesen beiden Informationen werden die passenden Seriennumern automatisch jedem Bild zugeordnet.
	Es werden zwei Tabellen ausgegeben:
	Aussortierte Bilder:
	Bilder mit Materialangaben werden aussortiert, um Inventarobjekte erzeugenn zu können und fehlerhafte Lokaliserungsbezeichnungen, die sich nicht der zugehörigen Konkordanztabelle befinden, werden aussortiert, um die Angaben in den Importtabellen zu berichtigen.
	df_import:
	Mit dieser Tabelle kann das weitere Skript ausgeführt werden (Umbennen und Verschieben). Es enthält aber alle Bildmetadaten und Bilder mit Fehler- oder Artefakt-Vermerken müssen manuell entfernt werden, sofern ein Import zunächst ohne diese durchgeführt werden soll.

Änderungen in der Version 1.7 vom Dezember 2022:
- Nach zwei Importen mit der 1.6er Version wurden weitere Verbesserungen vorgenommen, insbesondere wurde die Benutzerfreundlichkeit verbessert.
- Konvertierung der bisherigen Annotationen in Markdown und Hinzufügen weiterer ausführlicher, nun besser lesbaren Instruktionen.
- Check2 (Überprüfung der Dateipfade) ist jetzt kein manueller Test mehr sondern wird mit Code durchgeführt.
- Das Skript gibt nun zwei Tabellen mit aussortierten Bilder aus: Fehler und Artefakte, die noch importiert werden müssen, separat.
- Im zweiten Teil kann nun der Modus umgestellt werden, ob mit df_import Topographien oder mittels der artefaktliste Artefaktbilder importiert werden sollen.

The Version 1.7 is the first version uploaded here on GitHub.
