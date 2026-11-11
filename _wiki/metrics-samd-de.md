---
layout: default
title: "Metriken - SAMD (Software as a Medical Device)"
lang: de
permalink: /de/wiki/metrics-samd/
---
*[Read this article in English](/en/wiki/metrics-samd/)*

# Übersicht
| Kategorie | Metrik / Parameter | Fokus & Interpretation |
| :--- | :--- | :--- |
| **Gesamtleistung (Overall Performance)** | • Brier Score<br>• Brier Baseline Score<br>• Brier Skill Score<br>• Log-Loss / Cross-Entropy | Kombiniertes Maß aus Diskriminierung und Kalibrierung. |
| **Diskriminierung (Schwellenwertfrei)** | • ROC-AUC / Concordance Index (C-Index)<br>• PR-AUC (Precision-Recall AUC) | Trennfähigkeit über alle Schwellenwerte hinweg (besonders PR-AUC bei stark unbalancierten Klassen). |
| **Kalibrierung (Zuverlässigkeit)** | • Calibration Intercept (Ziel: 0)<br>• Calibration Slope (Ziel: 1)<br>• O:E-Ratio (Observed-to-Expected)<br>• ECE (Expected Calibration Error)<br>• ICI (Integrated Calibration Index)<br>• Kalibrierungsplot (Loess- / Spline-geglättet) | Übereinstimmung von geschätzten Risiken mit den beobachteten Ereignisraten (systematische Über-/Unteranpassung). |
| **Klassifikationsleistung (Schwellenwertabhängig)** | • Sensitivität & Spezifität<br>• Positive & Negative Predictive Value (PPV, NPV)<br>• F1-Score / Youden-Index | Gütemaße an einem spezifischen klinischen Entscheidungspunkt (Cut-off); PPV/NPV interpretierbar unter Kenntnis der Kohortenprävalenz. |
| **Klinischer Nutzen (Clinical Utility)** | • Decision Curve Analysis (DCA)<br>• Net Benefit (über klinische Schwellenwertbereiche) | Tatsächlicher Nutzen für Handlungsentscheidungen gegenüber einfachen Standardstrategien. |

> ℹ️ **Kontextfaktor Prävalenz (Ereignisrate)**  
> Die Prävalenz ist keine Eigenschaft oder Güte des Modells selbst, sondern eine Eigenschaft der untersuchten Population/Kohorte. Sie ist jedoch die entscheidende Bezugsgröße für die Modellbewertung:  
> - Sie definiert die Baseline für Gesamtleistungsmaße (z. B. Brier Baseline Score).  
> - Sie bestimmt direkt die klinische Aussagekraft von PPV und NPV.  
> - Bei seltenen Ereignissen (starkem Klassenungleichgewicht) erfordert sie den Wechsel von ROC-AUC zu PR-AUC.  
>  
> 📖 *Grundlagenartikel: [Bedeutung der Prävalenz für die Modellvalidierung](link-zum-wiki-artikel)*
