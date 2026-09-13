# Analisi del catalogo Netflix con Power BI

## Panoramica del progetto

Questo progetto analizza il catalogo Netflix utilizzando Power BI.

L'obiettivo è esplorare la composizione dei contenuti presenti sulla piattaforma e individuare tendenze relative a film, serie TV, anni di uscita, rating, durata e distribuzione dei contenuti.


## Strumenti utilizzati

- Power BI
- DAX
- Data Cleaning
- Data Visualization
- Data Analysis

## Dataset

Il dataset utilizzato è:

**Netflix Movies and TV Shows**

Fonte: Kaggle  
Autore: Shivam Bansal

File principale utilizzato:

`netflix_titles.csv`

Il dataset contiene informazioni relative a film e serie TV presenti su Netflix, tra cui:

- Titolo
- Tipo di contenuto
- Regista
- Cast
- Paese
- Anno di uscita
- Rating
- Durata
- Genere

## Anteprima della dashboard

![Netflix Power BI Dashboard](preview/Netflix analisi.png)

## KPI principali

La dashboard include i seguenti indicatori:

- Totale titoli
- Numero di film
- Numero di serie TV
- Anno medio di uscita
- Durata media dei film

## Analisi effettuate

La dashboard permette di analizzare:

- Film vs Serie TV
- Titoli per anno di uscita
- Distribuzione dei rating
- Durata dei contenuti
- Composizione del catalogo Netflix
- Principali categorie di contenuto

## Preparazione dei dati

Prima della creazione della dashboard, il dataset è stato pulito e trasformato in Power BI.

Le principali operazioni effettuate sono state:

- Controllo dei valori mancanti
- Pulizia dei dati sulla durata
- Distinzione tra film e serie TV
- Creazione di campi calcolati
- Creazione di misure DAX
- Preparazione dei dati per la visualizzazione

## Misure DAX

Alcune delle misure utilizzate nel progetto:

```DAX
Totale Titoli =
COUNTROWS(netflix_titles)

Film =
CALCULATE(
    [Totale Titoli],
    netflix_titles[type] = "Movie"
)

Serie TV =
CALCULATE(
    [Totale Titoli],
    netflix_titles[type] = "TV Show"
)
