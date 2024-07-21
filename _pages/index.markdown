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

<div class="justified">
<p>
“Nasci ingegnere, muori data scientist”: potrebbe essere la didascalia che descrive la trasformazione che il mondo del lavoro ha subito con l’avvento, tra le altre cose, dell’intelligenza artificiale. Al buon vecchio “ingegnere”, adesso si contrappongono una vasta serie di figure che di fatti svecchiano o, meglio, tentano <b>di dare nuovo lustro o di rendere più cool, più catchy, più al passo coi tempi</b>, la stessa figura professionale. Adesso, infatti, tra i vari annunci di LinkedIn è facilissimo trovare gli internazionalissimi data scientist, data engineer, pronti per attirare lo sguardo di eventuali candidati e perfetti per riempire bocca e CV. <br>
Difatti, una job opportunity del tutto simile a quella di qualche anno fa, adesso si ammanta di nuovo splendore. Diciamocelo: alla domanda “Che lavoro fai?”, rispondere un “Artificial intelligence engineer” ha tutto un altro sapore rispetto a “sviluppatore informatico”. Leggere, infatti, “programmatore” in un annuncio di lavoro ha ormai un sapore retrò - come ci ha segnalato Gabriella Pepi, HR di DataPizza.<br>
Marketing? Strategia di recruiting? Evoluzione vera e propria? Possiamo dare a questo fenomeno molti nomi, ma ormai è innegabile che abbia contribuito sensibilmente a rimappare una serie di ruoli, un tempo ben definiti, lasciando spazio, adesso, ad una sempre più <b>selvaggia libera interpretazione della job opportunity</b>, sfrangiando spesso i confini. Così, l'analista si “vende” come data scientist, uno sviluppatore per data engineer perché cambiare pelle, agghindare ruolo e nome, “rende”, in termini di riuscita e di mera apparenza. <br>

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

<h2 id="la-botte-piena-e-la-moglie-ubriaca">"LA BOTTE PIENA E LA MOGLIE UBRIACA"</h2>
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
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt1_LocationType_V2.json"></vegachart></div>
      <div style="flex: 1; max-width: 180%;"><vegachart schema-url="{{site.baseurl}}/assets/charts/GiulioArt2_PosterFullName_V2.json"></vegachart></div>
    </div>
  </div>
</div>



<h2 id="to-hire-or-not-to"> to hire or not to hire</h2>
<script type="text/javascript" src="https://ssl.gstatic.com/trends_nrtr/3769_RC01/embed_loader.js"></script> <script type="text/javascript"> trends.embed.renderExploreWidget("TIMESERIES", {"comparisonItem":[{"keyword":"linkedin","geo":"IT","time":"today 12-m"}],"category":0,"property":""}, {"exploreQuery":"geo=IT&q=linkedin&hl=it&date=today 12-m","guestPath":"https://trends.google.it:443/trends/embed/"}); </script>
---
