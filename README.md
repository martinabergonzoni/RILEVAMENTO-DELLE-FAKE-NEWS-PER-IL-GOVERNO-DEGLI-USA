# RILEVAMENTO-DELLE-FAKE-NEWS-PER-IL-GOVERNO-DEGLU-USA
Questo progetto sviluppa un sistema di Machine Learning capace di classificare automaticamente la veridicità degli articoli di stampa in lingua inglese.

## TECNICHE UTILIZZATE
Per questo progetto ho implementato una pipeline di elaborazione del linguaggio naturale completa:

- *Data preprocessing*: rimozione di  dateline per evitare che il modello impari la fonte invece del contenuto.

- *Pulizia* da caratteri speciali, URL e Stopwords (parole comuni che non aggiungono valore informativo).

- *Normalizzazione del testo*

- *Vettorizzazione*: trasformazione del testo in numeri tramite TfidfVectorizer, utilizzando n-grammi (unigrammi e bigrammi) per catturare il contesto delle frasi.

- *Modellazione*: utilizzo di LinearSVC (Support Vector Machine), un algoritmo efficace per la classificazione di testi ad alta dimensionalità.

- *Ottimizzazione*: implementazione di GridSearchCV per la ricerca dei migliori iperparametri.

Il modello, inoltre, permette di **interpretare perché una notizia è considerata sospetta** tramite:

- Matrice di confusione: analisi dettagliata dei falsi positivi e falsi negativi per garantire l'affidabilità del sistema.

- Feature importance: identificazione delle parole chiave più associate alle fake news rispetto alle notizie reali (es. l'uso di determinati aggettivi o riferimenti politici).
