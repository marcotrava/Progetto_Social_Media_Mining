# **Progetto di Social Media Mining – A.A. 2024/25**  
# Reddit Loves Rolex?  

Questo progetto analizza il comportamento degli utenti e la percezione del brand attraverso dati provenienti da Reddit, con un focus particolare su **Rolex** e un confronto con **Omega**. 
Il lavoro è stato svolto nell’ambito del corso di **Social Media Mining** dell'Università degli Studi di Milano.

## Domande di ricerca

1. Esiste una correlazione tra l’attività su Reddit e l’andamento dei prezzi Rolex?
2. Qual è il sentiment espresso nei confronti di Rolex nelle discussioni online?
3. Come si confrontano Rolex e Omega in termini di engagement e struttura comunitaria?
4. È possibile predire la preferenza verso un brand in base ai commenti degli utenti?


## Raccolta dati

- Fonte: Reddit API tramite **PRAW** (Python Reddit API Wrapper)
- Subreddit analizzati: `r/rolex`, `r/watches`
- Modelli considerati: **Submariner**, **GMT Master II**, **Datejust**
- Totale commenti raccolti: **5316**
- Integrazione con dati di **Google Trends** (2013–2025) per analisi temporale dell’interesse


## Analisi temporale e delle reti

- Confronto tra dati Reddit e Google Trends
- Creazione di **grafi bipartiti** per visualizzare relazioni tra utenti e modelli Rolex
- Proiezione dei grafi su utenti per rilevare **comunità basate su similarità**
- Metriche calcolate:
  - **Grado (degree)**
  - **Betweenness / closeness centrality**
  - **Coefficiente di clustering**
  - **Path medio**

Risultati: la comunità Rolex su Reddit è compatta e ben interconnessa, con utenti “hub” molto attivi.


## Rilevamento delle comunità e similarità

- Utilizzo dell’algoritmo di **modularità greedy** per individuare le comunità
- Similarità calcolata con **indice di Jaccard**
- Individuate 4 principali comunità coese


## Analisi del sentiment

- Libreria usata: **TextBlob**
- Analisi della polarità dei commenti che menzionano Rolex e Omega
- Risultato: sentiment **generalmente positivo**, forte affinità e fedeltà al brand. Assenza significativa di haters.


## Modello di machine learning

### Classificazione: predire preferenza Rolex vs Omega

- Feature utilizzate:
  - Embedding dei commenti
  - Numero di commenti per utente
  - Sentiment medio
  - Misure di centralità
- Algoritmi testati:
  - Regressione logistica
  - Decision Tree
  - Bagging
  - Random Forest
  |

**Conclusione**: i modelli non riescono a predire la preferenza con accuratezza sufficiente.


## Confronto tra le community Rolex e Omega

- Struttura della rete simile per entrambi i brand
- Community Rolex più densa e compatta
- Utenti che interagiscono con entrambi i brand evidenziati in un grafo bipartito combinato


## Licenza

Progetto accademico – uso educativo non commerciale.
