# Affidabilità Creditizia – Carta di Credito

Modello ML per prevedere l’affidabilità creditizia con regole interpretabili.

## Dataset
- 338k righe, 19 colonne; target: `TARGET=1` affidabile, `0` non affidabile (sbilanciato 91/9).

## Metodo
- EDA, feature engineering (`AGE_YEARS`, `EMPLOYMENT_YEARS`, `IS_PENSIONER`), pipeline sklearn.
- Modelli: Logistic Regression (baseline) e Decision Tree (finale).
- Split 80/20 stratificato, 5-fold CV, metrica principale: ROC AUC.

## Risultati
- Decision Tree: AUC 0.977 (CV≈Test), interpretabile.
- Regola chiave (Affidabile): Reddito > €163,493.70, Età > 41.96, Occupazione > 3.97 anni.
