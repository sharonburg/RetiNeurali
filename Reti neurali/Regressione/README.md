# 🚗 Regressione - Predizione del Prezzo di Auto Usate

Questo progetto utilizza un modello di **rete neurale** per prevedere il prezzo di auto usate, basandosi su caratteristiche tecniche e anagrafiche del veicolo.

## 📊 Dataset

Il dataset contiene informazioni su auto usate, tra cui:
- Anno di immatricolazione
- Chilometraggio
- Cilindrata
- Numero di proprietari
- Incidenti segnalati
- Tipo di carburante, marca, trasmissione, colore, assicurazione

> ⚠️ Il file utilizzato è `used_car_price_dataset_extended.csv`, che deve essere presente nella directory di lavoro.

## 🧪 Obiettivo

Prevedere il **prezzo in USD** di un’auto usata a partire dalle sue caratteristiche.

## ⚙️ Workflow

1. **Preprocessing**
   - Rimozione colonne non rilevanti
   - Separazione tra feature numeriche e categoriche
   - Standardizzazione delle feature numeriche
   - One-hot encoding delle feature categoriche

2. **Modello**
   - Rete neurale con:
     - Dense(64, ReLU)
     - Dense(32, ReLU)
     - Dense(1) → output continuo
   - Ottimizzatore: Adam
   - Loss: Mean Squared Error
   - Metriche: MAE (Mean Absolute Error)

3. **Addestramento**
   - 10 epoche
   - EarlyStopping e ReduceLROnPlateau per migliorare la stabilità
   - Validation split: 20%

4. **Valutazione**
   - MAE sul test set
   - Confronto con la deviazione standard e l’intervallo dei prezzi
   - Visualizzazione della curva di apprendimento e della distribuzione dei prezzi

## 📈 Risultati

- **MAE ≈ 836 USD** su un prezzo medio di circa 7.179 USD
- Nessun overfitting evidente
- Il modello ha appreso in modo stabile e rapido

## 🛠️ Requisiti
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- tensorflow / keras

## 🚀 Come eseguire

1. Assicurati di avere il file `used_car_price_dataset_extended.csv` nella directory `/content/`
2. Esegui lo script:

```bash
pip install -r requirements.txt
python regression.py
