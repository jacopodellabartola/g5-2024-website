---
layout: home
title: "Report"
#subtitle: "Analisi delle offerte di lavoro del mondo tech su Linkedin"
show_sidetoc: true
#header_type: hero
#header_img: /assets/images/pipeline_linkedin.jpg
#header_title: "Report tecnico"
vega: true
plotly: true
---


<style>
.myImage {
    height: auto;
    margin-left: -10%;
    transition: transform 0.3s ease;
  }

p {
    font-size: 15px;
    line-height:1.5; /* Modifica questo valore per adattarlo alle tue esigenze */
}




.justified {
    text-align: justify;
}

.full-width {
    width: auto;
    height: auto;
    object-fit: contain;
    max-width: 135%; /* Più grande del 100% per uscire dalla colonna */
    display: block;
    margin: 0 auto; /* Centra l'immagine */
    position: relative; /* Aggiunto per permettere l'uso di 'left' */
    left: -18%; /* Questo sposta l'immagine a sinistra del 20% */
}
</style>

<div class="justified" style="overflow: visible;">
  <div style="overflow: visible; width: 100%; text-align: center;">
    <img src="{{site.baseurl}}/assets/images/pipeline_linkedin.jpg" alt="Descrizione dell'immagine" class="full-width">
  </div>
</div>
<br>
<h1>REPORT TECNICO</h1>
<br>

<h2>RACCOLTA DATI</h2>
<div class="justified">
<p>
<br>
La fase iniziale del progetto coincide con quella di raccolta dei dati relativi agli annunci di lavoro presenti sulla piattaforma LinkedIn. Il periodo “utile” al processo di estrazione dei dati è stato di circa un mese, dal 02/05/2024 al 06/06/2024. Per automatizzare tale processo è stato realizzato uno script Python che utilizza il webdriver di Selenium, con l'obiettivo di raccogliere le informazioni sulle diverse posizioni lavorative aperte e salvare queste informazioni in un file CSV per successive analisi.<br>
Nel dettaglio le principali librerie utilizzate sono state, oltre alla già citata <i>selenium</i> per l’automatizzazione della navigazione, anche state <i>BeautifulSoup</i> per il parsing dell’HTML, <i>urllib.parse</i> per l'analisi degli indirizzi URL, <i>datetime, json, random, time</i> e <i>re</i> per la gestione delle variabili riguardanti il tempo e le variabili in stringhe, <i>csv</i> per la gestione dei file CSV in scrittura e lettura. <br>
La raccolta di dati è stata fatta seguendo una lista di professionalità delle quali sono state ricercate le posizioni lavorative aperte ciclicamente su base regionale attraverso la piattaforma LinkedIn stessa. La scelta di operare su base regionale risponde da un lato alla necessità di superare il limite dei 1000 annunci mostrati da LinkedIn per posizione lavorativa e luogo di ricerca, e dall’altro all’esigenza di una equa distribuzione dei compiti all’interno del nostro gruppo di lavoro. Con queste premesse, tutti gli annunci di lavoro ricercati sono stati consultati, analizzati, e i dati estratti sono stati salvati in un file CSV.<br>
Infine, nello script è stata implementata la gestione di possibili errori ed eccezioni per rendere il processo meno soggetto a interruzioni. I possibili arresti improvvisi dello script, anche dovuti a cause esterne, sono state gestite con una serie di funzioni tali per cui al riavvio manuale dello script la ripartenza avvenisse dal punto di avvenuta interruzione.<br>
Alla fase vera e propria di estrazione dati appena descritta, è seguita una fase di pulizia dei dati ottenuti tramite l’utilizzo di alcuni ipython notebook con i quali sono stati realizzati dei controlli preliminari sulla composizione delle variabili ottenute. Questa fase, oltre ad aver reso il dataset estratto più utilizzabile per le analisi seguenti, ha fornito anche un feedback sulla bontà dello script utilizzato per l’estrazione dei dati.  

<br>

<h2>RIMOZIONE OUTLIER</h2>
<br>
Per eliminare le job offer non relative all’ambito da noi analizzato si è cercato di automatizzare il processo di eliminazione del rumore, applicando una serie di tecniche che utilizzano algoritmi di clusterizzazione in grado di raggruppare le istanze considerate anomalie in cluster appositi.<br>
Le feature per noi interessanti ai fini della rimozione degli outlier - la descrizione (<i>descriptionComplete2</i>) e il titolo (<i>title</i>) - sono state tradotte dall’italiano all’inglese. Queste, infatti, non risultavano omogenee a livello linguistico e questo avrebbe potuto causare problemi con l’utilizzo delle tecniche scelte. Inoltre, è stato eseguito un mapping dei titoli sotto macrocategorie (e.g. ‘senior HR data analyst’ è stato mappato nella macrocategoria ‘data analyst’).<br>
In seguito, sono state utilizzate le API di Mistral per pulire ogni descrizione dalla parte riguardante l’azienda e inserirla in una nuova variabile chiamata “role_description” (prompt utilizzato: <i>Given the following job description: {description}. Eliminate the part related to the enterprise (including the benefits of the enterprise) and keep only the part related to the role. Do not write anything else beside the new description</i>). A questa variabile è stato applicato TagMe per identificare le entità presenti nel testo (creando la nuova feature <i>TMbis</i>. La feature <i>TM2</i>, invece, contiene le entità estratte con TagMe sulla descrizione totale pre utilizzo di Mistral.)<br>
Il pre-processing dei dati è stato eseguito attraverso una pipeline che ha incluso la conversione del testo in caratteri minuscoli (lower), la rimozione della punteggiatura, la tokenizzazione del testo, la rimozione delle <i>stop word</i> e la lemmatizzazione dei token.<br>
Di seguito i metodi utilizzati:
<br>
<h3 style="text-align: left;">RIMOZIONE OUTLIER - METODI INEFFICACI</h3>
<br>
<div class="justified">
<p>
Abbiamo optato per la rimozione degli outliers attraverso 3 metodi:
<h4>BERTopic</h4>
<br>
BERTopic è un metodo di modellazione degli argomenti tratti da un corpus di documenti che utilizza modelli BERT pre-allenati per generare embedding e per creare cluster densi- utilizzando di default HDBSCAN.
Le feature utilizzate sono state:
<ul>
    <li><b>role_description:</b> in questo caso, il cluster -1 rappresentante gli outlier, contiene 7796 righe, rappresentate dalle parole [‘data’, ‘experience’,‘knowledge’,‘solution’,‘team’, ‘software’, ‘development’, ‘skill’, ‘technical’, ‘system’]. Solamente alcuni dei cluster che si sono formati a partire da questo metodo potrebbero essere intesi come outlier, ma il numero è estremamente esiguo e non ci permette di considerare la rimozione di questi cluster per eliminare il rumore.</li>
    <li><b>TMbis:</b> in questo caso, il cluster -1 contiene 10247 istanze considerate outlier dal metodo. Queste sono rappresentate dalle parole [‘management’, ‘skill’, ‘software’, ‘business’, ‘engineering’, ‘development’, ‘process’, ‘knowledge’, ‘technology’, ‘data’]. Alcuni degli altri cluster formati potrebbero essere considerati outlier (e.g. 7_hobby_mass_sport_medium, di dimensione 21 istanze), ma, anche in questo caso, non troviamo un vero criterio per rimuovere gli outlier post clusterizzazione.</li>
    <li><b>skillsList:</b> in questo caso, il cluster -1 contiene 4364 record. Questi sono rappresentati con[‘data’, ‘communication’, ‘skills’, ‘management’, ‘analytical’,’analysis’, ‘language’]. Tutti gli altri cluster, tranne il 2-7-8 presentano caratteristiche del mondo tech, rendendo molto difficile scindere le istanze utili dal rumore.</li>
</ul>
<p>In conclusione, BERTopic non ci ha permesso di effettuare una rimozione efficace degli outlier tramite clusterizzazione.</p>

<h4>DBSCAN</h4>
<br>
Il secondo metodo utilizzato è l’algoritmo di clusterizzazione basato su densità DBSCAN, che restituisce un cluster di outlier (cluster -1). Come in precedenza, l’algoritmo è stato applicato alle 3 diverse feature. Il numero di MinPoints è stato scelto rifacendosi alla regola 2*D nel caso di dataset di grandi dimensioni, dopo vari tentativi con MinPoints diversi.
<br>
        <ul>
            <li><b>role_description</b>: utilizzando il metodo del ginocchio, l’eps ottimale è stato fissato a 18.22. In questo caso i cluster prodotti sono 2, di cui 2149 nel cluster -1 (outlier). In questo caso si ottiene una silhouette di 0.26. Osservando i titoli dei lavori presenti in entrambi i cluster, però, ci rendiamo conto che non è possibile fare una distinzione tra lavori tech o meno con questo tipo di soluzione, in quanto non risultano divisi.</li>
<li><b>TMbis</b>: in questo caso, l’eps ottimale è fissato a 7. I cluster formati sono 2, di cui quello di outlier contiene 1997 record. La silhouette che si ottiene è di 0.32. Come nel caso precedente, è impossibile tracciare una vera separazione tra le job offer utili e rumore.</li>
<li><b>skillsList</b>: in questo caso, l’eps ottimale è fissato a 4.35. I cluster che si sono formati sono 2. Il cluster rappresentante il rumore contiene 2384 record e silhouette di 0.23. Anche in questo caso, analizzando i titoli delle offerte di lavoro, ci rendiamo conto che non possiamo dividere con questo metodo il rumore dai lavori utili.</li> </ul>
<p>In conclusione, DBSCAN non ci ha permesso di effettuare una rimozione efficace degli outlier tramite clusterizzazione.</p>

<h3>RIMOZIONE OUTLIER - METODI EFFICACI</h3>
<br>
Abbiamo optato per la rimozione degli outliers attraverso 2 metodi:
<br>

<h3>TECH WORDS</h3>
<br>
Innanzitutto è stata stilata una lista di parole chiave, circa 50,  inerenti al mondo tech (come skills, linguaggi di programmazione, librerie per analisi dei dati, ecc…)  e sono state tolte tutte quelle job description che non contenevano nessuna di queste parole, questo ha permesso di eseguire una scrematura iniziale rimuovendo molti lavori non inerenti al tech che sono stati raccolti tramite scraping.<br>
<h3>SENTENCE TRANSFORMER</h3>
<br>
Si è caricato un modello pre addestrato, nello specifico "all-MiniLM-L6-v2". Abbiamo poi convertito le descrizioni in embedding e utilizzato UMAP per la riduzione della dimensionalità di quest’ ultimi. Infine calcolato i cluster con il metodo k-means. Abbiamo rimosso le job description che non contenevano informazioni utili riguardanti competenze e skills richieste. Il numero ottimale dei cluster è stato ottenuto con  il coefficiente di Silhouette e il metodo del gomito.<br>
<br>
<h3>COUNTVECTORIZER E TF-IDF </h3>
<br>
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; max-width: 50%;">
    <div style="display: flex; justify-content: center; align-items: center;">
      <vegachart schema-url="{{site.baseurl}}/assets/charts/chart_dimensionecluster_istogrammi 1.json" style="width: 100%;"></vegachart>
    </div>
  </div>
  <div style="flex: 1; max-width: 50%; padding-left: 20px;">
    <p>È stata utilizzata una pipeline con CountVectorizer e Tf-idf, eseguendo poi un clustering con k-means e plottando con PCA il risultato in due dimensioni. Una volta eseguito abbiamo visualizzato la frequenza dei vari job title all’interno di ogni cluster. Si è visto come erano presenti ancora dei lavori non inerenti / utili in quanto si era formato un cluster con lavori non pertinenti. Abbiamo quindi rimosso, attraverso la label, il cluster in questione e ripetuto la clusterizzazione con k-means ottenendo i cluster definitivi. Il numero ottimale dei cluster è stato ottenuto con il coefficiente di Silhouette e il metodo del gomito.</p>
  </div>
</div>
<br>

<h2>ULTERIORI ANALISI</h2>
<br>
<div class="justified">
<p>
Dopo aver confrontato se ci sia o meno un riscontro tra le job description e i titoli dei lavori, si è valutata l’efficacia di inserire o meno certe caratteristiche. Come variabile “proxy” si è utilizzato il numero di candidati, definendo un annuncio maggiormente efficace all’aumentare del numero di candidati attratti. Questa leva aumenta anche le probabilità che il processo di assunzione vada a buon fine, infatti ci sono due modi per raggiungere il risultato, migliorare la qualità dei candidati, difficilmente misurabile, oppure aumentare il numero di candidati attratti. <br>
<br>
A causa del tipo di dati estratti, che non permette di avere l’intera dinamica del numero di candidati nel tempo, si è proceduto a rielaborare la quantità “proxy”, concentrandosi sul tasso di crescita giornaliero del numero di candidati all’offerta. Questa quantità è calcolata come rapporto tra il numero di candidati misurati al momento dell’estrazione dell'annuncio di lavoro e il tempo di permanenza online dello stesso, calcolato come differenza in giorni tra la data di estrazione dell’annuncio e quella di pubblicazione.<br>
<br>
<div class="justified" style="display: flex; justify-content: center; overflow: visible;">
  <div style="overflow: visible; width: 70%;">
    <img src="{{site.baseurl}}/assets/images/equazione.jpeg" alt="Descrizione dell'immagine">
  </div>
</div>
<br>
<p>
Questa quantità è stata confrontata con le variabili a disposizione e rielaborazioni effettuate. I principali risultati dell’analisi sono riportati nell’articolo della pagina principale.</p>

<br></p>
<h2>SERVIZIO FINALE</h2>
<br>
<div class="justified">
<p>
Il servizio offerto finale rielabora in chiave predittiva l’analisi precedente, infatti utilizza come variabile target il tasso di crescita giornaliero del numero di candidati. <br>
<br>
Dopo aver analizzato la relazione che intercorre tra le quantità che compongono il numeratore e il denominatore, si è compreso che il tasso di crescita è differente nei vari periodi di vita dell’annuncio. In particolare, si è notato come il numero di candidati cresca velocemente nei primi giorni, per poi rallentare in quelli a seguire.<br>
<br>
<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%; display: flex; justify-content: center;">
    <vegachart style="width: 80%;" schema-url="{{site.baseurl}}/assets/charts/Giulio_Report1_NUOVO_v2.json"></vegachart>
  </div>
</div>

<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Il grafico mostra l’andamento del numero di candidati al variare della permanenza online.</p>
{% capture giulioreport %}
Per poter analizzare senza l’utilizzo di assunzioni distribuzionali, si è stimata la relazione tramite una Splines di lisciamento e questa mostra come ci sia una crescita importante del numero di candidati nei primi giorni e un rallentamento della crescita nei giorni successivi.
{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=giulioreport id="giulioreport" style="width: 80%; height: 30vh;" %}
<br>
<br></p>

<p>
Per questo motivo, si è preferito creare un modello che fosse formato da due componenti: una prima che modellasse il tasso di crescita dei candidati nei primi 7 giorni e una seconda che si è concentrata sul tasso di crescita dei candidati dall’ottavo giorno al cinquantaseiesimo (8 settimane).<br><br>

Le variabili esplicative utilizzate nei modelli implementate riguardano:<br></p>
<p>
        <ul>
            <li><b>Caratteristiche dell’azienda che ha aperto la posizione</b> (presenza di profilo aziendale, presenza del nome del gestore risorse umane che seguirà il processo di recruiting, numero di dipendenti, dichiarazione del settore di appartenenza);</li>
            <li><b>Caratteristiche dell’annuncio di lavoro </b> (modalità di lavoro, ripubblicazione di un annuncio esistente, tipo di contratto proposto dall’azienda, livello di esperienza richiesto, principali skill sia di tipo hard che soft che hanno una relazione forte con la variabile target o che sono molto utilizzate all’interno della job description)</li>
            <li><b>Caratteristiche spazio-temporali dell’annuncio </b>(regione della sede lavorativa, orario di pubblicazione e giorno della settimana)</li>
        </ul>
</p>
<br>
<p>
In fase di allenamento sono stati addestrati più modelli per poter scegliere il migliore, basandosi sulle performance ottenute. I modelli implementati sono: la regressione lineare multivariata, utilizzata come benchmark e per studiare ulteriormente le caratteristiche dei dati a disposizione, la regressione lineare LASSO, l’albero di regressione, la Random Forest, la Gradient Boosting Regression e la Support Vector Regression. Essendo la variabile target di tipo quantitativo, le metriche utilizzate per valutare l’adattamento del modello ai dati sono state quelle classiche dei task di regressione: il mean squared error (MSE) e il mean absolute error (MAE).<br>
<br>
Nel grafico sottostante si riportano le migliori combinazioni di modelli tra breve e lungo periodo e si osserva come il miglior modello sia quello che modella il tasso di crescita dei candidati sia nella prima settimana che dall'ottavo giorno al cinquantaseiesimo con una Support Vector Regression.<br>
<br>

<div style="display: flex; justify-content: center; align-items: center; margin-left: -15%;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/Giulio_Report2_Nuovo_v2.json"></vegachart></div>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Il grafico mostra il confronto tra le performance del modello finale proposto.</p>
{% capture giulioreport2 %}
Il risultato è la combinazione pesata degli indicatori di performance (MSE,MAE) sulla base del numero di osservazioni appartenenti a ciascun segmento.
{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=giulioreport2 id="giulioreport2" style="width: 80%; height: 30vh;" %}
<br>
<br>
<p>
A conclusione dell’addestramento emerge che i modelli più complessi sono quelli che hanno le migliori performance, in particolare si è osservato come un contributo fondamentale provenga dalla Support Vector Regression per la predizione del tasso di crescita nella prima settimana.
</p>