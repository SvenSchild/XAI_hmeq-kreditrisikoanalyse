# Explainable AI – HMEQ Kreditrisikoanalyse

## 1. Projektbeschreibung

In diesem Projekt beschäftigen wir uns mit der Vorhersage von Kreditausfällen mithilfe von Machine Learning und Explainable Artificial Intelligence (XAI).

Auf Grundlage des HMEQ-Datensatzes untersuchen wir, ob ein Kreditnehmer wahrscheinlich einen Kreditausfall erleidet.

Dabei werden zwei Klassifikationsverfahren trainiert, bewertet und miteinander verglichen:

- Logistische Regression
- Entscheidungsbaum (Decision Tree)

Neben der Vorhersageleistung liegt ein besonderer Fokus auf der Nachvollziehbarkeit und Interpretierbarkeit der Modellentscheidungen.

## 2. Datensatz

Für die Analyse wird der HMEQ-Datensatz (`hmeq.csv`) verwendet.

Die Zielvariable ist:

- `BAD = 0`: Kein Kreditausfall
- `BAD = 1`: Kreditausfall

Der Datensatz enthält Informationen über Kreditnehmer, bestehende Kredite, Kredithistorien und finanzielle Merkmale.

Die Datendatei befindet sich im Ordner `data` und wird von den Notebooks unter folgendem Pfad eingelesen:

`data/hmeq.csv`

## 3. Explorative Datenanalyse (EDA)

Im ersten Schritt wird der Datensatz untersucht und für die Modellierung vorbereitet.

Dabei werden unter anderem folgende Aspekte betrachtet:

- Aufbau und Eigenschaften des Datensatzes
- Verteilung der Merkmale
- Fehlende Werte
- Zusammenhänge zwischen den Variablen
- Auffälligkeiten und Datenqualität

## 4. Modellierung

### Logistische Regression

Die logistische Regression dient als Klassifikationsmodell zur Vorhersage von Kreditausfällen.

Dabei werden unter anderem folgende Schritte durchgeführt:

- Datenvorverarbeitung
- Umgang mit fehlenden Werten
- Kodierung kategorialer Merkmale
- Standardisierung numerischer Merkmale
- Hyperparameter-Optimierung
- Modellbewertung und Interpretation

### Entscheidungsbaum (Decision Tree)

Als zweites Modell wird ein Entscheidungsbaum eingesetzt.

Schwerpunkte der Analyse sind:

- Training eines unbeschränkten Entscheidungsbaums
- Untersuchung von Overfitting
- Begrenzung der Modellkomplexität
- Hyperparameter-Optimierung mittels GridSearchCV
- Globale und lokale Modellinterpretation
- Untersuchung der Merkmalswichtigkeit

## 5. Modellbewertung und Vergleich

Für einen fairen Modellvergleich werden dieselbe Datenaufteilung und vergleichbare Bewertungsmethoden verwendet.

Die Datengrundlage wird folgendermaßen aufgeteilt:

- Trainings-/Testaufteilung: 80/20
- Stratifizierte Aufteilung
- Random State: 42
- Cross-Validation: 5 Folds

Zur Bewertung der Modelle werden folgende Kennzahlen verwendet:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

Der F1-Score der Ausfallklasse dient als zentrale Optimierungsmetrik.

## 6. Explainable AI (XAI)

Ein wesentlicher Bestandteil des Projekts ist die Erklärbarkeit der Modellentscheidungen.

Dabei betrachten wir:

- Welche Merkmale besonders wichtig für die Vorhersagen sind.
- Welche Zusammenhänge das Modell erkennt.
- Wie einzelne Vorhersagen zustande kommen.
- Wie sich die Entscheidungen der beiden Modelle unterscheiden.

Ziel ist es, die Vorhersagen nicht nur quantitativ zu bewerten, sondern auch inhaltlich nachvollziehbar zu machen.

## 7. Installation und Ausführung

### Voraussetzungen

- Python
- Git
- Visual Studio Code
- Jupyter-Unterstützung in VS Code

### Repository klonen

```bash
git clone <repository-url>
cd <repository-name>

