# time_series_python
# Bitcoin Price Forecasting – Vergleich klassischer Zeitreihenmodelle

In diesem Projekt untersuche ich, wie gut sich klassische Zeitreihenmodelle für die Prognose des Bitcoin-Preises eignen.  
Bitcoin ist bekannt für seine hohe Volatilität und starke Marktbewegungen – genau deshalb ist es interessant zu sehen, wie weit man mit klassischen statistischen Methoden kommt.

Das Projekt ist im Rahmen eines Data-Analysis-Projekts entstanden und orientiert sich methodisch am **CRISP-DM-Prozess**.

---

## Ziel der Analyse

Die zentrale Frage des Projekts lautet:

> Können klassische Zeitreihenmodelle sinnvolle Prognosen für ein hochvolatiles Asset wie Bitcoin liefern?

Dafür werden mehrere Modelle miteinander verglichen und ihre Prognosequalität bewertet.

---

## Datengrundlage

Die Daten stammen aus der Python-Bibliothek **yfinance**.

- Asset: **BTC-USD**
- Zeitraum: **2016 – 2026**
- Frequenz: **Tägliche Schlusskurse**

---

## Vorgehensweise

Die Analyse orientiert sich an den typischen Schritten eines Data-Science-Projekts.

### Data Understanding

Zunächst wurde die Zeitreihe explorativ analysiert:

- Visualisierung des Kursverlaufs
- Untersuchung von Trends und Marktphasen
- STL-Decomposition zur Trennung von Trend und Residuen
- Analyse von Ausreißern

Dabei wurde schnell deutlich, dass der Bitcoin-Preis **stark volatil und nicht stationär** ist.

---

### Data Preparation

In diesem Schritt wurden die Daten für die Modellierung vorbereitet:

- Prüfung auf fehlende Werte und Duplikate
- Untersuchung möglicher Ausreißer
- **Train-Test-Split** für eine saubere Modellbewertung
- **ADF-Test zur Stationaritätsprüfung**

Da die Zeitreihe nicht stationär ist, wird dies im ARIMA-Modell über den Differenzierungsparameter berücksichtigt.

---

### Modeling

Zur Prognose wurden drei unterschiedliche Modelle implementiert:

- **Naive Forecast** – einfaches Benchmark-Modell
- **ETS (Exponential Smoothing)**
- **ARIMA**

Ziel war es, die Modelle sowohl visuell als auch quantitativ miteinander zu vergleichen.

---

### Evaluation

Die Modelle wurden anhand folgender Kennzahlen bewertet:

- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **RMSE (Root Mean Squared Error)**

Das **ETS-Modell** zeigte insgesamt die stabilsten Prognosen und die geringsten Fehlerwerte.

---

## Erkenntnisse

Ein paar wichtige Learnings aus der Analyse:

- Bitcoin weist starke Volatilität und klare Trendphasen auf.
- Klassische Zeitreihenmodelle stoßen an ihre Grenzen wenn es darum geht hochvolatile Assets abzubilden.


Mit anderen Worten:  
**Sie funktionieren als Benchmark – aber nicht als vollständige Lösung für Kryptomärkte.**

---

## Mögliche nächste Schritte

Um die Modellierung zu verbessern, könnten folgende Ansätze interessant sein:

- **GARCH-Modelle**, um die Volatilität explizit zu modellieren
- **ARIMAX / SARIMAX**, um zusätzliche Einflussfaktoren zu integrieren
- Einbindung technischer Indikatoren wie **RSI, MACD oder EMA**
- Kombination mit **Machine Learning Methoden**

---

## Verwendete Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn
- yfinance

---

## Fazit

Das Projekt zeigt gut, wie weit man mit klassischen Zeitreihenmethoden kommt – und wo ihre Grenzen liegen.  
Gerade bei Assets wie Bitcoin wird deutlich, dass **Volatilität und externe Markteinflüsse** eine große Rolle spielen und in einfachen Modellen nur begrenzt abgebildet werden können.
