# Projektplan: WORDERY(Java / MVC)


## Teammitglieder
- **Projekmeneger:** Volodymyr SHCHYROV
- Toni GUGIC
- Nazar TYMOSHENKO
  
---



Ein strukturierter Entwicklungsplan für ein dreiköpfiges Entwicklerteam zur Erstellung eines Lernspiels in Java unter Anwendung des **MVC-Entwurfsmusters (Model-View-Controller)**.



## 1. MVC-Architektur

### Model (`model/`)
* **`Word`**: Repräsentiert ein Wortpaar (z. B. Begriff, Übersetzung, Kategorie/Fachbereich wie *Softwareentwicklung* oder *Englisch*).
* **`Dictionary`**: Verwalter aller Wörter. Unterstützt das Laden aus Dateien (z. B. JSON/CSV) nach Themengebieten.
* **`GameSession`**: Speichert den aktuellen Spielstand, die verbleibenden Leben, verbrauchte Zeit, Punkte und falsche Antworten.

### View (`view/`)
* **`MainFrame`**: Das Hauptfenster der Anwendung.
* **`MenuView`**: Bildschirm zur Auswahl des Faches (*Englisch*, *Softwareentwicklung*) und des Spielmodus.
* **`GameView`**: Die eigentliche Spieloberfläche (Wortkarte, Antwortmöglichkeiten/Eingabefeld, Timer, Punkteanzeige).
* **`ResultView`**: Ergebnisbildschirm mit Auswertung und Fehleranalyse.

### Controller (`controller/`)
* **`GameController`**: Registriert Events aus der `View` (Button-Klicks, Tastatureingaben), aktualisiert das `Model` und steuert den Wechsel der Ansichten in der `View`.

---

## 2. Phaseninhalte & Meilensteine

### Phase 1: Projektvorbereitung & Architektur
* [ ] Dateiformat für Wörterbücher festlegen (z. B. JSON oder CSV).
* [ ] Git-Repository einrichten und Verzeichnisstruktur anlegen.
* [ ] Alle Idee einsameln, beschprechen und vorbereiten

### Phase 2: Kernentwicklung (Core Development)
* **Entwickler 1 (Model):**
  * [ ] Klassen `Word` und `Dictionary` implementieren.
  * [ ] Parser zum Einlesen der Wörterbücher für Fachbegriffe (*Softwareentwicklung*, *Englisch*) schreiben.
  * [ ] Logik für Zufallsauswahl der Fragen und Antwortprüfung entwickeln.
* **Entwickler 2 (View):**
  * [ ] `MainFrame` und Layout-Container (Panels) erstellen.
  * [ ] `GameView` gestalten (Fragekarte, Antwort-Buttons / Textfeld, Scoreboard).
  * [ ] `ResultView` für die Zusammenfassung entwerfen.
* **Entwickler 3 (Controller):**
  * [ ] `GameController` aufsetzen und Navigation zwischen Ansichten steuern (Menü $\rightarrow$ Spiel $\rightarrow$ Ergebnis).
  * [ ] Event-Listener (z. B. `ActionListener`) an GUI-Komponenten anbinden.

### Phase 3: Integration & Gamification
* **Model:**
  * [ ] Schwierigkeitsgrade und Highscore-Speicherung implementieren.
* **View:**
  * [ ] Visuelles Feedback einbauen (z. B. Grün/Rot-Färbung bei richtigen/falschen Antworten).
  * [ ] Fortschrittsbalken für den Timer und Lebensanzeige hinzufügen.
* **Controller:**
  * [ ] Countdown-Timer für Fragen implementieren.
  * [ ] Fehlerbehandlung und Spiel-Endbedingungen verknüpfen.

### Phase 4: Testen & Feinschliff
* [ ] **Gemeinsam:** Unit-Tests mit JUnit für die Logik im `Model` und das Einlesen der Dateien schreiben.
* [ ] Durchgängigen Durchlauf der Anwendung auf Stabilität und Fehlerfreiheit testen.
* [ ] Befüllen der Wörterbücher mit relevanten Fachbegriffen (z. B. OOP-Konzepte, Design Pattern, Datenbanken).

---
[Back to README ](./README.md)
