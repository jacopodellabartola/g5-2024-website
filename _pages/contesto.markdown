---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title:  "Contesto"
subtitle: "Analisi descrittiva delle nostre variabili"
show_sidetoc: true
header_type: hero #base, post, hero,image, splash
#header_img: assets/images/bootstrap.jpg
header_title: "Linkedin e il nostro contesto"
vega: true
---

<style>

p {
    font-size: 15px; /* Modifica questo valore per adattarlo alle tue esigenze */
    line-height:1.5;
}


.justified {
    text-align: justify;
}
 .myImage {
    height: auto;
    margin-left: -10%;
  }

</style>

# Perché Linkedin?

<div style="display: flex;">
  <div style="flex: 100%;">
    <img src="{{site.baseurl}}/assets/images/output.png" alt="Descrizione dell'immagine" style="width:120%;" class="myImage">
  </div>
  <div style="flex: 50%;">

<div class="justified">
      <p><br><br><br>Per quanto riguarda la piattaforma scelta per raccogliere dati, non abbiamo avuto dubbi: Linkedin è stata la nostra prima scelta.<br>
    LinkedIn è un social network professionale, tra i più diffusi al mondo, ad oggi conta circa 830 milioni di utenti nel mondo, di cui oltre 16 milioni in Italia e oltre 58 milioni di aziende (LinkedIn, 2024).<br></p>
    </div>
  </div>
</div>
<div class="justified">
  <p>È il più utilizzato dalle aziende per trovare candidati, infatti lo scopo principale è quello di mettere in contatto i professionisti tra loro e creare nuove opportunità di lavoro. Rispetto alle altre piattaforme, Linkedin ci ha permesso di fare un’analisi più completa grazie alla presenza del numero di candidati e alle altre variabili che in altre piattaforme non sono disponibili.</p>
</div>
<br>
<h2>Panoramica dei dati ottenuti: la dimensione</h2>
<br>
<div class="justified">
<p>
Il periodo di osservazione è avvenuto tra il 02/05/2024 e il 06/06/2024. Durante questo periodo sono stati seguiti e raccolti i dati di circa 7000 annunci di lavoro unici presenti sulla piattaforma LinkedIn. 
Le caratteristiche principali di nostro interesse sono state sostanzialmente due: annunci di lavoro che fossero pubblicati da aziende in Italia e che al tempo stesso riguardassero posizioni lavorative in campo informatico, con particolare attenzione all’ambito Data / A.I..</p>
<br>
<div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo1_DistTotLavori_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati, normalizzata per 100 mila abitanti.</p>
<div class="justified">

<p>
La distribuzione geografica degli annunci di lavoro osservati risulta abbastanza sbilanciata: le prime 5 regioni per numero totale di annunci (Lombardia, Lazio, Piemonte, Veneto, Emilia-Romagna) costituiscono quasi l’80% dell’offerta di lavori osservata, con la Lombardia che da sola supera di poco il 40% dell’intero ammontare. Volendo normalizzare il numero di annunci per la popolazione in età lavorativa (24 - 65 anni), la regione italiana che offre più lavoro resta la Lombardia (poco più di 40 annunci per 100 mila lavoratori), seguita da Piemonte e Lazio (entrambe quasi a quota 23 annunci per 100 mila lavoratori). Ultimo posto di questa “classifica” spetta alla Basilicata, con meno di un annuncio di lavoro per 100mila abitanti in età compresa tra 24 e 65 anni.</p> </div>

<div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
  <div style="width: 120%; margin-left: -10%;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo2_DistTipoLavori_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati per posizione lavorativa, normalizzata per 100 mila abitanti.</p>
<div class="justified">
<p>
Ma quali sono le posizioni lavorative in ambito Data / A.I.. maggiormente ricercate negli annunci di lavoro? Dai dati raccolti nel periodo di osservazione e normalizzati per popolazione in età lavorativa si nota una marcata concentrazione di annunci in alcune regioni ma non per tutte le professionalità.
Più in dettaglio, per posizioni di data analysis e business intelligence la maggiore presenza di annunci si nota prevalentemente in regioni del centro-nord Italia, quali Lombardia, Veneto, Piemonte, Trentino-Alto Adige, Emilia-Romagna e Lazio.
Per le altre posizioni lavorative mostrate non si notano variazioni così marcate tra le regioni.
</p>
<div style="display: flex; justify-content: center; align-items: center; ">
  <div style="width: 120%; margin-left: -15%;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo3_DistTipoSede_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati per sede lavorativa, normalizzata per 100 mila abitanti.</p>
<div class="justified">
<p>
Per quanto riguarda la distribuzione degli annunci di lavoro nei confronti della modalità di lavoro, i dati raccolti mostrano una maggioranza relativa di annunci di lavoro in modalità ibrida. Questa evidenza è stata riscontrata per molte regioni italiane: Lombardia, Piemonte, Emilia-Romagna, Valle d’Aosta, Liguria, Toscana, Lazio, Campania, Puglia, Calabria, Sicilia e Sardegna.
Per tutte le altre, i dati raccolti mostrano una maggioranza di annunci di lavoro in modalità in sede. Gli annunci di lavori che prevedono modalità da remoto sono i più rari in praticamente tutte le regioni.
</p>
<br>
<div style="display: flex; justify-content: center; align-items: center; ">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo4_DistDimAzienda_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati per dimensione aziendale, normalizzata per 100 mila abitanti.</p>
<div class="justified">
<p>
Infine, uno sguardo anche alle aziende che pubblicano gli annunci di lavoro su LinkedIn. Nel periodo di osservazione, i dati raccolti mostrano che gli annunci sono stati pubblicati prevalentemente da grandi imprese. Questo vale per tutte le regioni tranne la Basilicata.
</p>
<br>

<div style="display: flex; justify-content: center; align-items: center;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Dona_chart_ore.json" style="width: 100%"></vegachart>
</div>
<div class="justified">
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dictum, est eu accumsan suscipit, purus est elementum mauris, eu commodo ex mi a odio. Phasellus tempor neque id diam elementum aliquam. Morbi volutpat mollis odio, a consequat lorem tincidunt vitae. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed venenatis a nulla at bibendum. Etiam porta odio egestas nulla ornare maximus. Vestibulum vulputate ut ante non porta.

Sed ac fringilla leo, et mollis sapien. Mauris imperdiet, ante quis pellentesque venenatis, metus lacus aliquet tortor, ultrices sollicitudin lectus risus id neque. Integer faucibus, eros nec tincidunt blandit, massa nibh sollicitudin leo, ac consectetur sem odio a nibh. Etiam vulputate orci et libero vestibulum molestie. Maecenas aliquet condimentum lectus, ut placerat purus sagittis eu. Nulla feugiat eu tortor commodo dignissim. Donec erat ex, tempor quis mattis eu, imperdiet eu arcu. </p>
<div style="display: flex; justify-content: center; align-items: center;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Dona_chart_combinato_ore_giorno (1).json" style="width: 100%"></vegachart>
</div>

<div style="display: flex; justify-content: center; align-items: center;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Dona_chart_ore_annunci.json" style="width: 100%"></vegachart>
</div>

<div class="justified">
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dictum, est eu accumsan suscipit, purus est elementum mauris, eu commodo ex mi a odio. Phasellus tempor neque id diam elementum aliquam. Morbi volutpat mollis odio, a consequat lorem tincidunt vitae. Interdum et malesuada fames ac ante ipsum primis in faucibus. Sed venenatis a nulla at bibendum. Etiam porta odio egestas nulla ornare maximus. Vestibulum vulputate ut ante non porta.

Sed ac fringilla leo, et mollis sapien. Mauris imperdiet, ante quis pellentesque venenatis, metus lacus aliquet tortor, ultrices sollicitudin lectus risus id neque. Integer faucibus, eros nec tincidunt blandit, massa nibh sollicitudin leo, ac consectetur sem odio a nibh. Etiam vulputate orci et libero vestibulum molestie. Maecenas aliquet condimentum lectus, ut placerat purus sagittis eu. Nulla feugiat eu tortor commodo dignissim. Donec erat ex, tempor quis mattis eu, imperdiet eu arcu.
</p>