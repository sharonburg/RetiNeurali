# 🧠 Classificazione Binaria
Questo progetto utilizza tecniche di **machine learning** e **deep learning** per eseguire una classificazione binaria basata sui dati delle performance scolastiche degli studenti.

## 📁 Dataset

Il dataset utilizzato è `StudentsPerformance.csv`, contenente informazioni su:
- Genere
- Gruppo etnico
- Livello di educazione dei genitori
- Tipo di pranzo
- Partecipazione a corsi di preparazione
- Punteggi in matematica, lettura e scrittura

## ⚙️ Preprocessing

Le principali operazioni di preprocessing includono:
- Pulizia e normalizzazione dei dati
- Encoding di variabili categoriche (`gender`, `lunch`, `race/ethnicity`, `test preparation course`)
- Rimozione o trasformazione di colonne non utili
- Binarizzazione del punteggio di matematica (`math score`) per creare la variabile target

## 📊 Visualizzazione
È stata generata una **matrice di correlazione** per analizzare le relazioni tra le variabili.

## 🧪 Modello

È stato costruito un modello di rete neurale con TensorFlow/Keras:
- **Input**: variabili pre-elaborate
- **Architettura**: 
  - Dense(128, ReLU)
  - Dense(64 o 20, ReLU)
  - Dense(1, Sigmoid)
- **Output**: classificazione binaria (0 o 1)
- **Ottimizzatore**: Adam
- **Loss**: Binary Crossentropy

## 🔍 Tuning

Sono stati effettuati diversi tentativi di tuning:
- Modifica della `batch_size`
- Variazione del numero di nodi nei layer nascosti

## 📈 Risultati

Il modello è stato valutato su un set di test, con visualizzazione di:
- Accuracy e loss su training e validation
- Grafici delle metriche per ogni epoca

## 📦 Requisiti

- Python 3.x
- pandas
- scikit-learn
- matplotlib
- seaborn
- tensorflow

## 🚀 Avvio

```bash
pip install -r requirements.txt
python gruppo_4_classificazione_binaria.py
