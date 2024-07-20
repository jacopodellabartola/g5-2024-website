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
    font-size: 15px; /* Modifica questo valore per adattarlo alle tue esigenze */
}
</style>

# INTRODUZIONE

<div class="justified">
<p>
“Nasci da ingegnere muori da deep learning engineer”… una parafrasi della celebre frase basterebbe forse a descrivere l’evoluzione, il cambiamento, la faglia che il terremoto AI ha prodotto sul mercato del lavoro lasciando da una parte, solo, il “buon vecchio ingegnere” e contrapponendo ad esso una serie di figure che lo vedono, di fatto, trasformato e reinventato in un più cool data scientist o data engineer solo per citare due dei suggerimenti di ricerca che accedendo a Linkedin è più facile trovare se si cerca banalmente il ruolo del buon vecchio ingegnere informatico.<br>
La ricerca del lavoro ha nuove keywords, il mercato del lavoro ha modificato le terminologie per lasciare forse inalterate le competenze, ha modificato il titolo lasciando forse inalterata la trama per rivendere al pubblico un libro già letto. Mascherando una job opportunity simile a quella di qualche anno fa, dietro un titolo imponente, un titolo che gonfia di orgoglio, perché diciamocelo alla domanda che lavoro fai “Artificial intelligent engineering” rende molto più di un banale “sviluppatore informatico”.<br>
Chiamatelo marketing, chiamatela strategia di recruiting, chiamatela stare al passo coi tempi, ma di fatto oggi l’evoluzione terminologica ha contribuito sensibilmente a rimappare una serie di ruoli un tempo ben definiti lasciando spazio, spesso, alla libera interpretazione della job opportunity, e cosi un’analista si vende per data scientist, uno sviluppatore per prompt engineer, perché cambiare pelle fa bene e rende sicuro più cool in una società troppo spesso fatta di “titoli”.<br>
</p>
</div>
<br>
<div>
<div class="container">
    <div class="row justify-content-center">
        <div class="col-lg-8">
            <blockquote style="font-size: 1.5em; font-weight: bold; font-style: italic; text-align: center;">
                Cosa spinge (o cosa attrae) l’individuo a candidarsi per un annuncio piuttosto che un altro?
            </blockquote>
        </div>
    </div>
</div>

</div>
<br>
<br>

<br>
# AI + H > AI or H

<div class="justified">
<p>
Partiamo proprio dalle sinergie, la sinergia creata dall’uomo più l’AI, sarà sicuramente superiore alla AI stessa o al singolo individuo quindi partiamo da una certezza la sinergia c’è e va sfruttata, la sinergia arricchisce e non sostituisce.<br>
E che la parte umana c'è e arricchisce è impossibile negarlo, soprattutto soffermandoci sulla quantità di hard e soft skill richieste ai candidati. Una vera e propria foresta di requisiti che confonde più che chiarire quali sono le aspettative dell'HR, dell'azienda e del datore di lavoro.<br>
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
Saltando da un annuncio all'altro dell'universo tech su Linkedin presto ci rendiamo che per essere un candidato interessante agli occhi di un recruiter non dobbiamo solamente saper programmare, conoscere le metodologie di interrogazione dei dati e tutta un'altra infinita serie di linguaggi di programmazione e conoscenze di backround,ma anche - e soprattutto- esaltare la nostra parte "umana" con le soft skill, che, come ci mostrano i dati, "vince" il braccio di ferro con la sua controparte "dura".<br> 
Se la capacità di prendersi le proprie responsabilità può spaventare nella vita di tutti i giorni, diventa un requisito che sembra particolarmente ricercato nei candidati. Ma non solo, la capacità di lavorare in team e di comunicazione e quella di capire il business che ho davanti sono quelle che Stefano Gatti- attualmente head of Data & Analytics a Nexi e scrittore del libro "La cultura del dato"- ha definito le skill che fanno la differenza nell'ambito AI e con le quali ci scontriamo analizzando gli innumerevoli job post della piattaforma. <br>
</p>
</div>
<br>

# "LA BOTTE PIENA E LA MOGLIE UBRIACA" 
<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/simone.json"></vegachart></div>
</div>
<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/simone2.json"></vegachart></div>
</div>

<div style="display: flex; justify-content: center; align-items: center;">
  <div style="flex: 1; max-width: 100%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/simone skills.json"></vegachart></div>
</div>

<br>
<br>
<br>


# PARTE GIULIO DA decidere nome

<style>
  .image {
    width: 150%;
    height: auto;
  }
</style>

<div style="width: 100%; display: flex; justify-content: center; align-items: center;">
  <div style="width: 120%; margin-left: 0%;">
    <div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt1_LocationType_V2.json"></vegachart></div>
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt2_PosterFullName_V2.json"></vegachart></div>
    </div>
  </div>
</div>



# TO HIRE OR NOT TO HIRE

<script type="text/javascript" src="https://ssl.gstatic.com/trends_nrtr/3769_RC01/embed_loader.js"></script> <script type="text/javascript"> trends.embed.renderExploreWidget("TIMESERIES", {"comparisonItem":[{"keyword":"linkedin","geo":"IT","time":"today 12-m"}],"category":0,"property":""}, {"exploreQuery":"geo=IT&q=linkedin&hl=it&date=today 12-m","guestPath":"https://trends.google.it:443/trends/embed/"}); </script>
---
