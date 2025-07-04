# ☀️ Time Series Forecasting - Sunspot Prediction

Questo progetto utilizza un modello **ARIMA** per analizzare e prevedere l'andamento delle **macchie solari** (sunspots) nel tempo.

## 📊 Dataset

Il dataset utilizzato è disponibile su Kaggle:
🔗 Sunspots Dataset – [id]: https://www.kaggle.com/datasets/robervalt/sunspots "Kaggle"

Contiene il numero medio mensile di macchie solari osservate dal 1749 in poi.

## 🧪 Obiettivo
Prevedere il numero di macchie solari per i prossimi **20 anni** (240 mesi) utilizzando un modello ARIMA ottimizzato.

## ⚙️ Workflow

1. **Pulizia dati**
   - Rimozione colonne inutili
   - Conversione della colonna `Date` in formato datetime
   - Impostazione dell'indice temporale

2. **Analisi di stazionarietà**
   - Test di Dickey-Fuller Aumentato (ADF)
   - La serie risulta stazionaria → `d = 0`

3. **Selezione dei parametri ARIMA**
   - **PACF** → scelta di `p = 5`
   - **ACF** → scelta di `q = 29` (poi testato anche con `q = 15`)

4. **Addestramento modello**
   - Modello ARIMA con parametri `(p=5, d=0, q=29)`
   - Previsione per 240 mesi

5. **Valutazione**
   - MAE, MSE, RMSE
   - Confronto tra modelli con diversi valori di `q`

## 📈 Risultati

- Il modello riesce a catturare