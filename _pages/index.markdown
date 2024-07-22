---
layout: home
title: "Home"
subtitle: "Analisi delle offerte di lavoro del mondo tech su Linkedin"
show_sidetoc: true
header_type: hero
# header_img: assets/images/stampo_biscotti.jpg
header_title: "Nasci ingegnere muori data scientist"
vega: true
plotly: true
---

<style>
p {
    font-size: 15px;
    line-height:1.5; /* Modifica questo valore per adattarlo alle tue esigenze */
}
</style>

<div class="justified">
<p>
“Nasci ingegnere, muori data scientist”: potrebbe essere la didascalia che descrive la trasformazione che il mondo del lavoro ha subito con l’avvento, tra le altre cose, dell’intelligenza artificiale. Al buon vecchio “ingegnere”, adesso si contrappongono una vasta serie di figure che di fatti svecchiano o, meglio, tentano <b>di dare nuovo lustro o di rendere più cool, più catchy, più al passo coi tempi</b>, la stessa figura professionale. Adesso, infatti, tra i vari annunci di LinkedIn è facilissimo trovare gli internazionalissimi data scientist, data engineer, pronti per attirare lo sguardo di eventuali candidati e perfetti per riempire bocca e CV. <br>
<br>
Difatti, una job opportunity del tutto simile a quella di qualche anno fa, adesso si ammanta di nuovo splendore. Diciamocelo: alla domanda “Che lavoro fai?”, rispondere un “Artificial intelligence engineer” ha tutto un altro sapore rispetto a “sviluppatore informatico”. Leggere, infatti, “programmatore” in un annuncio di lavoro ha ormai un sapore retrò - come ci ha segnalato Gabriella Pepi, HR di DataPizza.<br>
<br>
Marketing? Strategia di recruiting? Evoluzione vera e propria? Possiamo dare a questo fenomeno molti nomi, ma ormai è innegabile che abbia contribuito sensibilmente a rimappare una serie di ruoli, un tempo ben definiti, lasciando spazio, adesso, ad una sempre più <b>selvaggia libera interpretazione della job opportunity</b>, sfrangiando spesso i confini. Così, l'analista si “vende” come data scientist, uno sviluppatore per data engineer perché cambiare pelle, agghindare ruolo e nome, “rende”, in termini di riuscita e di mera apparenza. <br>
<br>

</p>
</div>
<br>
<div>
<div class="container">
    <div class="row justify-content-center">
        <div class="col-lg-8">
            <blockquote style="font-size: 1.5em; font-weight: bold; font-style: italic; text-align: center;">
                "Cosa spinge (o cosa attrae) l’individuo a candidarsi per un annuncio piuttosto che un altro?"
            </blockquote>
        </div>
    </div>
</div>

</div>
<br>
<br>

<br>
# AI + H > AI or H
<br>
<div class="justified">
<p>
Partiamo da una certezza, come sostiene Stefano Gatti -attualmente head of Data & Analytics presso Nexi e autore del libro "La cultura del dato”- la disequazione del prossimo futuro sarà questa: 
<br>
<br><p>

<div style="font-size: 20px; text-align: center;">
    AI + H &gt; AI or H
</div>
<br>
<p>
Il punto cruciale da sottolineare è che la coniugazione tra AI e “umano” è fondamentale e imprescindibile: la <b>sinergia </b> di una e l’altra parte, la somma delle potenzialità di ciascuna, porta ad un risultato maggiore della mera somma delle singole. L’ambizione massima deve essere la coniugazione di questi due fattori, senza che uno prevalga o escluda l’altro.
Difatti, la parte umana rimane insostituibile, soprattutto agli occhi dei recruiter - basti pensare alla quantità di soft skills richieste ai candidati - al punto che tanti e tali sono i requisiti richiesti che spesso risulta difficile chiarire quali siano le <b>reali aspettative dell’HR, dell’azienda e del datore di lavoro.</b><br> 
</p>
<br>
<br>


<div style="display: flex; justify-content: center;">
{% include graficobollenuovo2.html %}
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">In questo grafico sono rappresentate in percentuale le 10 competenze più richieste suddivise in tre categorie: soft skill, hard skill e linguaggi di programmazione.</p>


{% capture skills %}
Il grafico mostra una distribuzione equilibrata tra le tre categorie, con un leggero sbilanciamento verso le soft skill. Tra quest'ultime, le più richieste sono la capacità di prendere decisioni e assumersi le conseguenti responsabilità, il lavoro in team e le competenze comunicative. Per quanto riguarda le hard skill le più richieste sono la programmazione, database management system e la conoscenza della lingua inglese. Infine, i linguaggi di programmazione più richiesti sono SQL, Python e Excel.

Le diverse skill necessarie per creare questo grafico sono state estratte da ciascuna descrizione del ruolo dell’insieme degli annunci di lavoro. Il dataset utilizzato per mappare le soft skill proviene dall’istituto GESIS Leibniz-Institut für Sozialwissenschaften. Per le hard skill, ci siamo rifatti a un dataset disponibile su Kaggle 'hard skills'.
{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=skills id="dettaglidataset" style="width: 80%; height: 30vh;" %}
<br>
<br>
<br>
<p>
Nel mare magnum degli annunci dell’universo tech rinvenibili su LinkedIn, ciò che emerge chiaramente è che un candidato, per essere interessante ed appetibile agli occhi di un recruiter, non deve solamente possedere le skills professionali (a titolo d’esempio, <b>saper programmare</b> utilizzando diversi linguaggi e conoscere le metodologie di <b>interrogazione dei dati</b>) ma anche, e soprattutto, deve esaltare la sua attitudine “umana”. Le soft skills, dati alla mano, infatti vincono la sfida contro la loro controparte “hard”. <br>
E così, il saper padroneggiare determinate situazioni diventa un requisito particolarmente ricercato nei candidati, ma non solo, gli esempi sono molteplici: la capacità di lavorare in team o quella di comprendere il business e l’attività che si hanno davanti sono quelle che anche Stefano Gatti ha definito le skill che fanno la differenza nell'ambito AI. 
</p>
<br>

<h2 id="la-foresta-di-requisiti">LA FORESTA DI REQUISITI</h2>
<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/simone.json"></vegachart></div>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Diagrammi a barre illustranti la distribuzione delle varie posizioni lavorative all’interno dei cluster.</p>
{% capture simone %}
L’analisi dei cluster generati sulla base delle descrizioni degli annunci di lavoro evidenzia come solamente il cluster 2,3 e 7 contengano una professione dominante, ma risultano essere cluster di dimensioni esigue e, quindi, il loro risultato non fortemente impattante. <br>
Questi cluster sono stati generati utilizzando l’algoritmo di clustering K-Means. Dopo aver applicato un adeguato preprocessing alle descrizioni degli annunci di lavoro, sono stati identificati 12 cluster distinti. Tuttavia, a parte i cluster menzionati in precedenza, questi cluster presentano una sovrapposizione a livello di competenze.

{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=simone id="simone" style="width: 80%; height: 30vh;" %}



<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/simone skills.json"></vegachart></div>
</div>

<br>
<br>
<br>

<h2 id="parte-giulio"> parte giulio</h2>
<style>
  .image {
    width: 150%;
    height: auto;
  }
</style>

<div style="width: 100%; display: flex; justify-content: center; align-items: center;">
  <div style="width: 120%; margin-left: 0%;">
    <div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt4_ClustSkills_v2.json"></vegachart></div>
    </div>
  </div>
</div>

{% capture giulio1 %}
I grafici mostrano l’andamento del tasso di crescita giornaliero di candidati rispetto ai singoli cluster individuati (sinistra) e rispetto alla loro capacità di identificarsi in un chiaro titolo (destra). <br>
Da entrambi si nota come i cluster non ben definiti siano in grado di attrarre maggiori candidati a parità di tempo di permanenza online dell’annuncio. 

{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=giulio1 id="giulio1" style="width: 80%; height: 30vh;" %}

<div style="width: 100%; display: flex; justify-content: center; align-items: center;">
  <div style="width: 120%; margin-left: 0%;">
    <div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt3FACOLTATIVO_Skills (1).json"></vegachart></div>
    </div>
  </div>
</div>

{% capture giulio2 %}
Il grafico mostra l’andamento del tasso di crescita giornaliero di candidati rispetto alla frequenza osservata negli annunci della singola skill. Si nota come ci sia una significativa relazione non lineare diretta tra la frequenza della skill e la capacità degli annunci in cui è stata inserita di attrarre candidati (la correlazione è anche stata misurata con indice di Spearman ed è significativa e si attesta su valori di 0.38). <br>
Si osserva anche che esistono alcune singole skill, poco frequenti, alle quali sono collegate buone performance di efficacia dell’annuncio. 

{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=giulio2 id="giulio2" style="width: 80%; height: 30vh;" %}




<div style="width: 100%; display: flex; justify-content: center; align-items: center;">
  <div style="width: 120%; margin-left: 0%;">
    <div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt2_PosterFullName_v4.json"></vegachart></div>
    </div>
  </div>
</div>


{% capture giulio3 %}
Il grafico sulla sinistra mostra l’andamento del numero di candidati medio al passare dei giorni di permanenza online dell’annuncio, nel caso in cui si sia presente o meno il nome del Gestore HR che seguirà il processo di recruiting. Si nota come migliorino le performance dell’annuncio se è presente il nome.<br>
Il grafico sulla destra invece mostra la distribuzione nel tempo degli annunci online suddivisi tra presenza e assenza del gestore HR nell’annuncio. Si osserva che per la maggior parte degli annunci si è misurata una breve permanenza online e che all’aumentare di questa diminuisce la proporzione di annunci aventi il nome del Gestore HR. Questo suggerisce, come anche visto per altri casi, che una caratteristica dell’annuncio in grado di attirare candidati permette una riduzione del tempo di permanenza online dell’annuncio.
{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=giulio3 id="giulio3" style="width: 80%; height: 30vh;" %}

<div style="width: 100%; display: flex; justify-content: center; align-items: center;">
  <div style="width: 120%; margin-left: 0%;">
    <div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt1_LocationType_v4.json"></vegachart></div>
    </div>
  </div>
</div>

{% capture giulio4 %}
Il grafico sulla sinistra mostra l’andamento del numero di candidati medio al passare dei giorni di permanenza online dell’annuncio, al variare della modalità lavorativa (Da remoto, Ibrido, In sede). Si nota come migliorino le performance dell’annuncio all’aumentare della possibilità di lavorare anche da remoto. <br>
Il grafico sulla destra invece mostra la distribuzione nel tempo degli annunci online tra le varie modalità lavorative. Come già osservato nel grafico precedente, si nota come all’aumentare della permanenza online diminuisce la proporzione di annunci aventi caratteristiche che aumentano più velocemente il numero di candidati. <br>

{% endcapture %}
{% include modal-component.html title="Dettagli del grafico" content=giulio4 id="giulio4" style="width: 80%; height: 30vh;" %}

<h2 id="to-hire-or-not-to"> to hire or not to hire</h2>
<script type="text/javascript" src="https://ssl.gstatic.com/trends_nrtr/3769_RC01/embed_loader.js"></script> <script type="text/javascript"> trends.embed.renderExploreWidget("TIMESERIES", {"comparisonItem":[{"keyword":"linkedin","geo":"IT","time":"today 12-m"}],"category":0,"property":""}, {"exploreQuery":"geo=IT&q=linkedin&hl=it&date=today 12-m","guestPath":"https://trends.google.it:443/trends/embed/"}); </script>
---
