https://github.com/WI13-project/infosaeule/blob/master/prototyp2/doku/nutzungsinfo.md

# Softwaredoku, Teil 1

## Auswahl der Architektur und Umsetzung 
Da beim gewünschten Einsatzszenario der Bedarf nach mehreren Benutzern, Einfachheit, Aktualität und Portabilität besteht, entschieden wir uns für eine dynamische Generierung der Inhalte. Für diesen Zweck prädestiniert ist die serverseitige Skriptsprache PHP. Dadurch bietet sich viele Vorteile:

* plattformunabhängige Nutzung
* hohe Datenintegrität
* leicht portierbar durch weite Verbreitung

Davon ausgehend begannen wir mit einer an den Bedürfnissen des Auftraggebers orientierten Dateistruktur, welche stetig erweitert wurde.
https://github.com/WI13-project/infosaeule/blob/master/prototyp2/doku/prototyp2.svg
Beispielhaft dafür sei die Nutzerverwaltung des Administrationsbackends genannt:

* **Schritt 1:** "security through obscurity", die Dateien waren ungeschützt aber nur durch den genauen Link zu finden
* **Schritt 2:** einfache dateibasierte Nutzerrechte mittels htaccess
* **Schritt 3:** Erweiterung der htaccess um die drei Nutzergruppen, enthalten in einer zusätzlichen htgroups-Datei
* **Schritt 4:** Umstellung der Nutzerdaten auf eine SQLite-Datenbank
* **Schritt 5:** Authentifizierung aus der Datenbank wird in einer Session gespeichert. Logout möglich

Zur besseren Wartung wurden größere Dateien modularisiert und alle Pfade relativ gesetzt. Für bessere Anschaulichkeit kamen HTML, CSS und JavaScript zum Einsatz.
Als Datenbanksystem wurde sich bewusst für SQLite3 entschieden da dieses keinen Datenbankserver benötigt und die Anforderungen vollends erfüllt.

## Auswahl der Versionsverwaltung und Umsetzung 
Die Entwicklung sollte lokal und verteilt erfolgen. Auch die Absicherung gegen ungewollte Änderungen galt es dabei zu beachten. Ausgehend von diesen Eigenschaften entschieden wir uns für den Einsatz von git. Der bekannteste, zudem auch kostenlose, Anbieter von git-repositories ist das amerikanische Unternehmen GitHub. Hervorzuheben sind dabei die Erweiterung der Versionsverwaltung um soziale Funktionen wie Kommentare und "Sternchen" (zum Ausdruck des Gefallens), unbegrenzter Speicherplatz, zahlreiche Schnittstellen (siehe nächster Punkt), hohe Stabilität und die Möglichkeit des Webzugriffs.
Weiterhin existieren git-Plugins für alle erdenklichen Entwicklungswerkzeuge so dass ein nahtloser Arbeitsablauf erfolgen kann.
Zum Verwalten der Teilgruppen gründeten wir die Organisation WI13-project in GitHub und erstellten die repositories doku, protokolle und infosaeule für die jeweiligen Gruppen.

## Auswahl des Vorgehensmodells und Umsetzung 
-> SCRUM


