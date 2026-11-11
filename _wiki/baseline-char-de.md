---
layout: default
title: "Ausgangscharakteristika"
lang: de
permalink: /de/wiki/baseline-char/
math: true
---
*[Read this article in English](/en/wiki/baseline-char/)*


| Kategorie | Parameter / Merkmale | Typische Darstellung | Relevanz für das Prädiktionsmodell |
| :--- | :--- | :--- | :--- |
| **Demografie** | • Alter<br>• Geschlecht / Gender<br>• BMI / Körpermaße<br>• Soziodemografie (z. B. Bildungsstand, Ethnie) | Stetig (Mittelwert $\pm$ SD / Median [IQR])<br>Kategorial ($n$, %) | Basis-Prädiktoren; essenziell zur Überprüfung von Repräsentativität, Fairness und Subgruppeneffekten. |
| **Klinischer Status & Anamnese** | • Komorbiditäten (Diabetes, KHK, Hypertonie etc.)<br>• Komorbiditäts-Scores (z. B. Charlson Index)<br>• Akute Krankheitsschwere (z. B. SOFA, APACHE, NYHA)<br>• Vitalparameter (Blutdruck, Puls, SpO₂, Temperatur)<br>• Vormedikation & Lebensstil (Rauchstatus, Mobilität) | Binär ($0/1$ bzw. ja/nein)<br>Ordinal / Summenscores<br>Stetig | Hauptquelle für Feature Engineering zum Vorhersagezeitpunkt $t_0$; zentral zur Erkennung von Confoundern. |
| **Diagnostik & Biomarker** | • Routinelabor (Kreatinin, eGFR, CRP, Leukozyten)<br>• Spezifische Biomarker (Troponin, Laktat, HbA1c)<br>• Apparative Befunde (z. B. EKG-Befund, LVEF) | Stetig (mit Maßeinheiten)<br>Kategoriale / binäre Befundmuster | Häufig stärkste Prädiktoren; erfordert strikte zeitliche Zuordnung vor Eventeintritt (Vermeidung von *Data Leakage*). |
| **Kohorten- & Studiendesign** | • Gesamtstichprobe ($N$)<br>• Prävalenz / Ereignisrate (Zielereignisse, $n$, %)<br>• Rekrutierungssetting (Normalstation, ICU, Ambulanz)<br>• Zentren (Single- vs. Multicenter)<br>• Follow-up-Dauer (bei Time-to-Event-Modellen) | Absolute Fallzahlen<br>Prozentanteile (%)<br>Median [IQR] Zeiträume | Definiert die Baseline-Prävalenz und Stichprobenpower; deckt *Covariate Shift* und *Spectrum Bias* bei externer Validierung auf. |
| **Datenqualität (Missingness)** | • Fehlende Werte pro Variable (*Missing Data*)<br>• Fehlmuster (MCAR, MAR, MNAR) | Fehlend absolute Zahl ($n$)<br>Prozentualer Anteil (%) | Bestimmt Imputationsstrategien; hoher Missing-Anteil kann Modelle verzerren oder auf mangelnde Routine-Verfügbarkeit hinweisen. |
