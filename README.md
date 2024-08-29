# Analisi Esplorativa del Titanic Dataset

L'affondamento del Titanic è uno dei naufragi più famosi della storia. Il 15 aprile 1912, durante il suo viaggio inaugurale, il Titanic affondò dopo aver colliso con un iceberg, causando la morte di 1502 delle 2224 persone tra passeggeri e membri dell'equipaggio. La costruzione del Titanic costò circa 7,5 milioni di dollari, e affondò nell'oceano a causa della collisione.

Dataset:   [Titanic - Kaggle](https://www.kaggle.com/competitions/titanic)

## Obiettivo
L’obiettivo è quello di creare un notebook per effettuare un’analisi esplorativa dei dati e capire se chi è sopravvissuto è semplicemente stato fortunato o se ci fossero persone che avessero più probabilità di altre di salvarsi, in relazione alle loro caratteristiche.

Per questo progetto utilizzeremo le librerie `pandas` per la manipolazione dei dati, `matplotlib` per la visualizzazione dei dati.

## Passaggi dell'Analisi

### 1. Importazione del Dataset
Importare il dataset con `pandas` e visualizzare la tabella.

### 2. Esplorazione dei Valori Nulli
Esplorare la situazione dei valori nulli nel dataset.

### 3. Analisi dei Sopravvissuti
Numero di sopravvissuti: è la variabile che ci interessa esplorare e comprendere, mentre esploreremo tutte le altre feature in relazione ad essa. Iniziamo creando dei grafici sul numero di sopravvissuti (ad esempio a Torta o a Barre).

### 4. Analisi delle Features
- **Quali sono le feature Categoriche?**
- **Quali sono le feature Ordinali?**
- **Quali sono le feature Continue?**

#### Sex (Genere)
- Che tipo di variabile è?
- Quanti sono gli uomini e le donne sopravvissuti? E i non sopravvissuti?
- Scegliere una visualizzazione per riassumere al meglio l’informazione.
- **Quali insights possiamo trarre?**

#### Pclass (Classe di Biglietto)
- Che tipo di variabile è?
- Come si suddividono le varie classi tra sopravvissuti e non sopravvissuti? C’è una relazione tra la ricchezza dei passeggeri e la loro probabilità di sopravvivere?
- Scegliere una visualizzazione per riassumere al meglio l’informazione.
- **Quali insights possiamo trarre?**

### 5. Relazione tra Sex e Pclass
La classe influenza in qualche modo le probabilità di sopravvivere maggiormente per uno o per l’altro sesso, oppure è indifferente? Suggerimento: qui potrebbe essere una buona scelta una visualizzazione che consenta di distinguere tre dimensioni.

### 6. Età
- Che tipo di variabile è?
- Descrivi la distribuzione: trova il valore minimo, massimo, la media, la mediana e la moda.

### 7. Data Cleaning e Feature Extraction
Studiamo meglio la variabile per migliorare la qualità del dato:
- **Valori Nulli:**
  - Quanti sono valori nulli?
  - Quali approcci generici possiamo usare per imputare i valori nulli? Quale potrebbe essere il problema di un approccio generico in questo caso?
- **Feature Extraction:**
  - Per questo dataset, possiamo utilizzare un approccio specifico: la colonna `Name` contiene anche il titolo (Master, Miss, Mr, Mrs). Effettuiamo una feature extraction, creando una nuova colonna a partire da quella del nome, che contenga solo il titolo.
  - Per ottenere questo risultato bisogna utilizzare una regex che è la seguente: `'([A-Za-z]+)\.'`.
  - Una volta ottenuta la colonna dei titoli, computare la media per ognuno di essi ed imputare i valori nulli di età sulla base di questo risultato.

- **Relazioni dell'Età:**
  - Come si relaziona l’età con la classe? E con il sesso? Suggerimento: qui potrebbe essere una buona scelta creare due visualizzazioni che consentano di distinguere tre dimensioni (età, sesso o classe, sopravvisuto).
  - **Quali insights possiamo trarre sui salvataggi delle diverse demografiche?**

### 8. Correlazioni tra le Feature (Correlazione Lineare di Pearson)
- Creare una heatmap di correlazioni tra le feature.
- **Quali informazioni possiamo estrarre da questa heatmap?**

### 9. Sommario dei Findings per ogni Feature
- Riassunto delle osservazioni e degli insights per ogni feature analizzata.
