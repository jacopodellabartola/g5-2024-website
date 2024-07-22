---
layout: home
title: "Report"
#subtitle: "Analisi delle offerte di lavoro del mondo tech su Linkedin"
show_sidetoc: true
header_type: hero
# header_img: assets/images/stampo_biscotti.jpg
header_title: "Report tecnico"
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


ul {
    font-size: 15px; /* Modifica questo valore per adattarlo alle tue esigenze */
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
    <img src="{{site.baseurl}}/assets/images/pipeline.png" alt="Descrizione dell'immagine" class="full-width">
  </div>
</div>




<br>
<h2>RIMOZIONE OUTLIER</h2>
<br>
<div class="justified">
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dictum, est eu accumsan suscipit, purus est elementum mauris, eu commodo ex mi a odio. Phasellus tempor neque id diam elementum aliquam. Morbi volutpat mollis odio, a consequat lorem tincidunt vitae. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed venenatis a nulla at bibendum. Etiam porta odio egestas nulla ornare maximus. Vestibulum vulputate ut ante non porta.

Sed ac fringilla leo, et mollis sapien. Mauris imperdiet, ante quis pellentesque venenatis, metus lacus aliquet tortor, ultrices sollicitudin lectus risus id neque. Integer faucibus, eros nec tincidunt blandit, massa nibh sollicitudin leo, ac consectetur sem odio a nibh. Etiam vulputate orci et libero vestibulum molestie. Maecenas aliquet condimentum lectus, ut placerat purus sagittis eu. Nulla feugiat eu tortor commodo dignissim. Donec erat ex, tempor quis mattis eu, imperdiet eu arcu.
<br>
<br></p>

<h2>ANALISI DESCRITTIVA DEL FENOMENO</h2>
<div class="justified">
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dictum, est eu accumsan suscipit, purus est elementum mauris, eu commodo ex mi a odio. Phasellus tempor neque id diam elementum aliquam. Morbi volutpat mollis odio, a consequat lorem tincidunt vitae. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed venenatis a nulla at bibendum. Etiam porta odio egestas nulla ornare maximus. Vestibulum vulputate ut ante non porta.

Sed ac fringilla leo, et mollis sapien. Mauris imperdiet, ante quis pellentesque venenatis, metus lacus aliquet tortor, ultrices sollicitudin lectus risus id neque. Integer faucibus, eros nec tincidunt blandit, massa nibh sollicitudin leo, ac consectetur sem odio a nibh. Etiam vulputate orci et libero vestibulum molestie. Maecenas aliquet condimentum lectus, ut placerat purus sagittis eu. Nulla feugiat eu tortor commodo dignissim. Donec erat ex, tempor quis mattis eu, imperdiet eu arcu. 
<br>
<br></p>

<h2>CLUSTERING</h2>
<div class="justified">


<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/simone2.json"></vegachart></div>
</div>
<p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dictum, est eu accumsan suscipit, purus est elementum mauris, eu commodo ex mi a odio. Phasellus tempor neque id diam elementum aliquam. Morbi volutpat mollis odio, a consequat lorem tincidunt vitae. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed venenatis a nulla at bibendum. Etiam porta odio egestas nulla ornare maximus. Vestibulum vulputate ut ante non porta.

Sed ac fringilla leo, et mollis sapien. Mauris imperdiet, ante quis pellentesque venenatis, metus lacus aliquet tortor, ultrices sollicitudin lectus risus id neque. Integer faucibus, eros nec tincidunt blandit, massa nibh sollicitudin leo, ac consectetur sem odio a nibh. Etiam vulputate orci et libero vestibulum molestie. Maecenas aliquet condimentum lectus, ut placerat purus sagittis eu. Nulla feugiat eu tortor commodo dignissim. Donec erat ex, tempor quis mattis eu, imperdiet eu arcu.</p>
<br>
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

<br>
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
    <vegachart style="width: 80%;" schema-url="{{site.baseurl}}/assets/charts/Giulio_Report1.json"></vegachart>
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
<br>
<p>
In fase di allenamento sono stati addestrati più modelli per poter scegliere il migliore, basandosi sulle performance ottenute. I modelli implementati sono: la regressione lineare multivariata, utilizzata come benchmark e per studiare ulteriormente le caratteristiche dei dati a disposizione, la regressione lineare LASSO, l’albero di regressione, la Random Forest, la Gradient Boosting Regression e la Support Vector Regression. Essendo la variabile target di tipo quantitativo, le metriche utilizzate per valutare l’adattamento del modello ai dati sono state quelle classiche dei task di regressione: il mean squared error (MSE) e il mean absolute error (MAE).<br>
<br>
Nel grafico sottostante si riportano le migliori combinazioni di modelli tra breve e lungo periodo e si osserva come il miglior modello sia quello che modella il tasso di crescita dei candidati nella prima settimana con una Support Vector Regression e il  tasso di crescita dei candidati dall'ottavo giorno al cinquantaseiesimo con una Random Forest.<br>
<br>

<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/Giulio_Report2.json"></vegachart></div>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Il grafico mostra l’andamento del numero di candidati al variare della permanenza online.</p>
{% capture giulioreport2 %}
Per poter analizzare senza l’utilizzo di assunzioni distribuzionali, si è stimata la relazione tramite una Splines di lisciamento e questa mostra come ci sia una crescita importante del numero di candidati nei primi giorni e un rallentamento della crescita nei giorni successivi.
{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=giulioreport2 id="giulioreport2" style="width: 80%; height: 30vh;" %}
<br>
<br>
<p>
A conclusione dell’addestramento emerge che i modelli più complessi sono quelli che hanno le migliori performance, in particolare si è osservato come un contributo fondamentale provenga dalla Support Vector Regression per la predizione del tasso di crescita nella prima settimana.
</p>