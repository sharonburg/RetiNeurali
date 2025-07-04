# Progetti di Reti Neurali

Questa repository contiene una collezione di progetti che esplorano diverse applicazioni delle reti neurali e del deep learning. Ogni sottocartella rappresenta un progetto distinto, con il proprio dataset, metodologia e obiettivi specifici.

## Indice dei Progetti

- [Classificazione Binaria](#classificazione-binaria)
- [Classificazione di Immagini](#classificazione-di-immagini)
- [Classificazione di Testi](#classificazione-di-testi)
- [Regressione](#regressione)
- [Time Series Forecasting](#time-series-forecasting)




## Classificazione Binaria

Questo progetto si concentra sulla classificazione binaria utilizzando tecniche di machine learning e deep learning sui dati delle performance scolastiche degli studenti. L'obiettivo è prevedere un risultato binario (0 o 1) basato su diverse caratteristiche degli studenti.

### Dettagli del Progetto

- **Dataset**: `StudentsPerformance.csv`, contenente informazioni su genere, gruppo etnico, livello di educazione dei genitori, tipo di pranzo, partecipazione a corsi di preparazione e punteggi in matematica, lettura e scrittura.
- **Preprocessing**: Pulizia e normalizzazione dei dati, encoding di variabili categoriche, rimozione/trasformazione di colonne non utili e binarizzazione del punteggio di matematica per creare la variabile target.
- **Visualizzazione**: Generazione di una matrice di correlazione per analizzare le relazioni tra le variabili.
- **Modello**: Rete neurale con TensorFlow/Keras, architettura con layer Dense (128, ReLU), Dense (64 o 20, ReLU) e Dense (1, Sigmoid). Ottimizzatore Adam e loss Binary Crossentropy.
- **Tuning**: Modifiche alla `batch_size` e variazione del numero di nodi nei layer nascosti.
- **Risultati**: Valutazione del modello su un set di test, con visualizzazione di accuracy e loss su training e validation, e grafici delle metriche per ogni epoca.




## Classificazione di Immagini

Questo progetto si occupa della classificazione automatica di immagini relative alle Meraviglie del Mondo, sfruttando tecniche di deep learning con TensorFlow/Keras.

### Dettagli del Progetto

- **Dataset**: Immagini di 12 categorie di Meraviglie del Mondo (es. Angel Falls, Burj Khalifa, Chichen Itza, ecc.), suddivise in 70% training, 15% validation e 15% test.
- **Preprocessing**: Estrazione da file `.zip`, riorganizzazione delle cartelle per categoria, visualizzazione di immagini di esempio, conversione in array NumPy, normalizzazione dei pixel e codifica one-hot delle etichette.
- **Modello**: Implementazione di due tentativi di rete neurale convoluzionale (CNN).




## Classificazione di Testi

Questo progetto utilizza tecniche di Natural Language Processing (NLP) e Deep Learning per classificare testi in base all'emozione espressa.

### Dettagli del Progetto

- **Dataset**: Dataset di emozioni disponibile su Kaggle (Emotion Dataset), contenente frasi etichettate con emozioni come joy, anger, sadness, fear, love, surprise, ecc.
- **Obiettivo**: Addestrare un modello di deep learning in grado di classificare automaticamente il testo in una delle emozioni predefinite.
- **Workflow**: Preprocessing (rimozione delle stopwords, tokenizzazione e padding, encoding).




## Regressione

Questo progetto implementa un modello di rete neurale per prevedere il prezzo di auto usate, basandosi su caratteristiche tecniche e anagrafiche del veicolo.

### Dettagli del Progetto

- **Dataset**: `used_car_price_dataset_extended.csv`, con informazioni su anno di immatricolazione, chilometraggio, cilindrata, numero di proprietari, incidenti segnalati, tipo di carburante, marca, trasmissione, colore, assicurazione.
- **Obiettivo**: Prevedere il prezzo in USD di un’auto usata a partire dalle sue caratteristiche.
- **Workflow**: Preprocessing (rimozione colonne non rilevanti, separazione tra feature numeriche e categoriche, standardizzazione delle feature numeriche, one-hot encoding delle feature categoriche).
- **Modello**: Rete neurale con layer Dense (64, ReLU), Dense (32, ReLU) e Dense (1) per output continuo. Ottimizzatore Adam, loss Mean Squared Error e metrica MAE.
- **Addestramento**: 10 epoche con EarlyStopping e ReduceLROnPlateau, validation split del 20%.
- **Risultati**: MAE ≈ 836 USD su un prezzo medio di circa 7.179 USD, nessun overfitting evidente e apprendimento stabile.




## Time Series Forecasting

Questo progetto utilizza un modello ARIMA per analizzare e prevedere l'andamento delle macchie solari (sunspots) nel tempo.

### Dettagli del Progetto

- **Dataset**: Sunspots Dataset da Kaggle, contenente il numero medio mensile di macchie solari osservate dal 1749 in poi.
- **Obiettivo**: Prevedere il numero di macchie solari per i prossimi 20 anni (240 mesi) utilizzando un modello ARIMA ottimizzato.
- **Workflow**: Pulizia dati (rimozione colonne inutili, conversione data, impostazione indice temporale), analisi di stazionarietà (Test di Dickey-Fuller Aumentato), selezione dei parametri ARIMA (PACF per `p=5`, ACF per `q=29` o `q=15`).
- **Addestramento Modello**: Modello ARIMA con parametri `(p=5, d=0, q=29)` e previsione per 240 mesi.
- **Valutazione**: MAE, MSE, RMSE e confronto tra modelli con diversi valori di `q`.
- **Risultati**: Il modello riesce a catturare l'andamento delle macchie solari.



