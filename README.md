Markdown
# Data Pipeline & Linear Regression: Optische Polarisationsanalyse

Automatisierte Python-Pipeline zur Verarbeitung, Bereinigung und mathematischen Modellierung experimenteller Labordaten aus Polarisationsmessungen. Inspiriert von den Forschungsprojekten der Fakultät für Naturwissenschaften.

## 📊 Projektübersicht

Dieses Projekt demonstriert die erfolgreiche **Fehlerreduktion durch die Umstellung von manuellen Excel-Tabellen auf skriptbasierte, automatisierte Workflows**. Die Pipeline liest fehleranfällige Rohdaten aus optischen Sensoren ein, bereinigt statistisches Rauschen und nutzt lineare Regressionsmodelle zur präzisen Bestimmung von physikalischen Rotationskonstanten.

### Kernfeatures:
* **Data Engineering (Pandas):** Automatisierte Filterung von Sensorfehlern und Bereinigung unphysikalischer Messwerte (Rauschunterdrückung).
* **Statistische Modellierung (SciPy):** Anwendung der linearen Regression zur Validierung der Messwerte gegen die theoretischen Modelle.
* **Visual Analytics (Matplotlib):** Automatisierte Erstellung von Publikationsgrafiken zum direkten Abgleich zwischen Theorie und Experiment.

---

## 🛠️ Technologie-Stack

* **Programmiersprache:** Python 3.12
* **Bibliotheken:** Pandas, SciPy (statistische Regressionsanalysen), Matplotlib
* **Ehemaliges System:** MS Excel (vollständig automatisiert via Python-Skript)

---

## 📐 Mathematisches Modell

Die Linearisierung der optischen Intensitätsdaten erfolgt über das physikalische Gesetz zur Polarisation. Die Bestimmung der Rotationskonstante wird über die Methode der kleinsten Quadrate berechnet:

$$I(\theta) = I_0 \cdot \cos^2(\theta) + c$$

Das Modell evaluiert das Bestimmtheitsmaß ($R^2$), um die Güte der experimentellen Daten im Vergleich zur Theorie direkt auszugeben.

---

## 📈 Validierungsergebnisse

Die automatisierte Pipeline liefert nach der Bereinigung folgende Kennzahlen:
* **Berechnete Rotationskonstante (Steigung):** ~5.02 (Abweichung innerhalb der Toleranzgrenze)
* **Bestimmtheitsmaß ($R^2$):** > 0.98 (Bestätigt eine exzellente Modellgüte)

Die Ergebnisse werden vollautomatisch im Report-Plot `optical_validation_plot.png` ausgegeben.

---

## 📂 Repository-Struktur

```bash
├── optical_pipeline.ipynb         # Haupt-Pipeline für ETL & Lineare Regression
├── optical_validation_plot.png    # Automatisierter Validierungs-Plot
└── README.md                      # Projektdokumentation (Deutsch)
🔧 Installation & Ausführung
Erforderliche Bibliotheken installieren:

Bash
pip install pandas numpy scipy matplotlib

Pipeline ausführen:
Starten Sie Jupyter Notebook und führen Sie alle Zellen der Datei optical_pipeline.ipynb aus.