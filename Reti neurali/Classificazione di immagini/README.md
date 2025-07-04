# 🖼️Image Classification

Questo progetto si occupa della classificazione automatica di immagini relative alle **Meraviglie del Mondo**, utilizzando tecniche di **deep learning** con **TensorFlow/Keras**.

## 📁 Dataset

Il dataset contiene immagini di 12 categorie:
- Venezuela Angel Falls
- Burj Khalifa
- Chichen Itza
- Christ the Redeemer
- Great Wall of China
- Machu Picchu
- Taj Mahal
- Pyramids of Giza
- Stonehenge
- Roman Colosseum
- Eiffel Tower
- Statue of Liberty

Le immagini sono state suddivise in:
- **70%** training
- **15%** validation
- **15%** test

## 🧹 Preprocessing

- Estrazione da file `.zip`
- Riorganizzazione delle cartelle per categoria
- Visualizzazione immagini di esempio
- Conversione in array NumPy
- Normalizzazione dei pixel
- Codifica one-hot delle etichette

## 🧠 Modello

Due tentativi di rete neurale convoluzionale (**CNN**) sono stati implementati