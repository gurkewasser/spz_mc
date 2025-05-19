# SPZ - OMC: Zeitreihenanalyse meteorologischer Daten

Dieses Projekt analysiert historische Wetterdaten für Bakersfield, Kalifornien (USA) mit dem Ziel, klimatologische Trends und extreme Wetterereignisse zu identifizieren und Vorhersagemodelle zu evaluieren.

## 🔍 Projektbeschreibung

Das Notebook `main_spz.ipynb` führt eine umfassende Analyse historischer Wetterdaten durch. Es umfasst folgende Schritte:

1. **Datenerhebung**
   - Abruf täglicher Wetterdaten für Bakersfield von **1980 bis 2024** über das `meteostat`-Paket.
   - Fokus auf Temperatur, Niederschlag und weitere relevante meteorologische Variablen.

2. **Explorative Datenanalyse (EDA)**
   - Visualisierung der Wetterverläufe mit `matplotlib` und `seaborn`.
   - Zeitreihenzerlegung mittels STL und `seasonal_decompose`.

3. **Statistische Tests**
   - Stationaritätstests mit **ADF-Test** und **KPSS-Test**.
   - Autokorrelationsanalyse (ACF/PACF).

4. **Modellierung**
   - Zeitreihenprognosen mit folgenden Methoden:
     - **SARIMAX-Modell**
     - **Prophet-Modell**
     - **Random Forest Regressor**
   - Hyperparameter-Tuning über `GridSearchCV` und `RandomizedSearchCV`.

5. **Extremwertanalyse**
   - Anwendung von Generalized Extreme Value (GEV) und Generalized Pareto Distribution (GPD) zur Modellierung extremer Wetterereignisse.

6. **Evaluierung**
   - Vergleich der Modelle mit Metriken wie **MAE** und **RMSE**.
   - Modellvisualisierungen und Fehleranalysen.

## 🧰 Verwendete Pakete

- `meteostat`
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `statsmodels`, `scikit-learn`
- `prophet`
- `cartopy`
- `scipy`

## 📍 Standort & Zeitraum

- **Ort:** Bakersfield, Kalifornien, USA
- **Zeitraum:** Januar 1980 – März 2024

## 📂 Aufbau

- `main_spz.ipynb`: Hauptnotebook mit allen Analysen
- Daten werden direkt per API bezogen – kein separates Dataset erforderlich

## 📈 Ziel

Das Ziel dieser Arbeit ist es, auf Basis meteorologischer Zeitreihen robuste Modelle für die Temperatur- und Niederschlagsvorhersage zu entwickeln und klimatische Extremereignisse statistisch zu analysieren.

---
