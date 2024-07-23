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


# Perché Linkedin?

<div style="display: flex;">
  <div style="flex: 100%;">
    <img src="{{site.baseurl}}/assets/images/output.png" alt="Descrizione dell'immagine" style="width:120%;" class="myImage">
  </div>
  <div style="flex: 50%;">

      <p><br><br><br>Per quanto riguarda la piattaforma scelta per raccogliere dati, non abbiamo avuto dubbi: Linkedin è stata la nostra prima scelta.<br>
    LinkedIn è un social network professionale, tra i più diffusi al mondo, ad oggi conta circa 830 milioni di utenti nel mondo, di cui oltre 16 milioni in Italia e oltre 58 milioni di aziende (LinkedIn, 2024).<br></p>

  </div>
</div>

  <p>È il più utilizzato dalle aziende per trovare candidati, infatti lo scopo principale è quello di mettere in contatto i professionisti tra loro e creare nuove opportunità di lavoro. Rispetto alle altre piattaforme, Linkedin ci ha permesso di fare un’analisi più completa grazie alla presenza del numero di candidati e alle altre variabili che in altre piattaforme non sono disponibili.</p>

<br>
<h2>Panoramica dei dati ottenuti: la dimensione spaziale</h2>
<br>

<p>
Il periodo di osservazione è avvenuto tra il 02/05/2024 e il 06/06/2024. Durante questo periodo sono stati seguiti e raccolti i dati di circa 7000 annunci di lavoro unici presenti sulla piattaforma LinkedIn. 
Le caratteristiche principali di nostro interesse sono state sostanzialmente due: annunci di lavoro che fossero pubblicati da aziende in Italia e che al tempo stesso riguardassero posizioni lavorative in campo informatico, con particolare attenzione all’ambito Data / A.I..</p>
<br>
<center><h5>Distribuzione regionale degli annunci di lavoro osservati</h5></center>
<div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo1_DistTotLavori_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati, normalizzata per 100 mila abitanti.</p>
<div class="justified">

<p>
La distribuzione geografica degli annunci di lavoro osservati risulta abbastanza sbilanciata: le prime 5 regioni per numero totale di annunci (Lombardia, Lazio, Piemonte, Veneto, Emilia-Romagna) costituiscono quasi l’80% dell’offerta di lavori osservata, con la Lombardia che da sola supera di poco il 40% dell’intero ammontare. Volendo normalizzare il numero di annunci per la popolazione in età lavorativa (24 - 65 anni), la regione italiana che offre più lavoro resta la Lombardia (poco più di 40 annunci per 100 mila lavoratori), seguita da Piemonte e Lazio (entrambe quasi a quota 23 annunci per 100 mila lavoratori). Ultimo posto di questa “classifica” spetta alla Basilicata, con meno di un annuncio di lavoro per 100mila abitanti in età compresa tra 24 e 65 anni.</p> </div>
<br>
<center><h5>Distribuzione regionale degli annunci di lavoro per posizione lavorativa</h5></center>
<div style="display: flex; justify-content: center; align-items: center; flex-direction: column;">
  <div style="width: 120%; margin-left: -10%;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo2_DistTipoLavori_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati per posizione lavorativa, normalizzata per 100 mila abitanti.</p>

<p>
Ma quali sono le posizioni lavorative in ambito Data / A.I.. maggiormente ricercate negli annunci di lavoro? Dai dati raccolti nel periodo di osservazione e normalizzati per popolazione in età lavorativa si nota una marcata concentrazione di annunci in alcune regioni ma non per tutte le professionalità.
Più in dettaglio, per posizioni di data analysis e business intelligence la maggiore presenza di annunci si nota prevalentemente in regioni del centro-nord Italia, quali Lombardia, Veneto, Piemonte, Trentino-Alto Adige, Emilia-Romagna e Lazio.
Per le altre posizioni lavorative mostrate non si notano variazioni così marcate tra le regioni.
</p>
<br>
<center><h5>Distribuzione regionale degli annunci di lavoro per modalità lavorativa</h5></center>
<div style="display: flex; justify-content: center; align-items: center; ">
  <div style="width: 120%; margin-left: -15%;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo3_DistTipoSede_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati per sede lavorativa, normalizzata per 100 mila abitanti.</p>

<p>
Per quanto riguarda la distribuzione degli annunci di lavoro nei confronti della modalità di lavoro, i dati raccolti mostrano una maggioranza relativa di annunci di lavoro in modalità ibrida. Questa evidenza è stata riscontrata per molte regioni italiane: Lombardia, Piemonte, Emilia-Romagna, Valle d’Aosta, Liguria, Toscana, Lazio, Campania, Puglia, Calabria, Sicilia e Sardegna.
Per tutte le altre, i dati raccolti mostrano una maggioranza di annunci di lavoro in modalità in sede. Gli annunci di lavori che prevedono modalità da remoto sono i più rari in praticamente tutte le regioni.
</p>
<br>
<center><h5>Distribuzione regionale degli annunci di lavoro per dimensione aziendale</h5></center>
<div style="display: flex; justify-content: center; align-items: center; ">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo4_DistDimAzienda_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione per regioni italiane degli annunci di lavoro osservati per dimensione aziendale, normalizzata per 100 mila abitanti.</p>

<p>
Infine, uno sguardo anche alle aziende che pubblicano gli annunci di lavoro su LinkedIn. Nel periodo di osservazione, i dati raccolti mostrano che gli annunci sono stati pubblicati prevalentemente da grandi imprese. Questo vale per tutte le regioni tranne la Basilicata.
</p>
<br>

<h2>Panoramica dei dati ottenuti: la dimensione temporale</h2>
<br>

<div style="display: flex; justify-content: center; align-items: center; height: 100vh;">
    <vegachart schema-url="{{site.baseurl}}/assets/charts/Dona_combined_chart_ore_giorno.json" style="width: 100%"></vegachart>
</div>


<p style="font-size: 0.9em; background-color: white; color: grey; padding: 10px;">Distribuzione degli annunci di lavoro per fascia oraria e per giorno della settimana.</p>



<p>
Ma quando vengono pubblicati gli annunci di lavoro? <br>
Analizzando i dati raccolti si osserva che l’orario lavorativo è il momento in cui vengono maggiormente pubblicati gli annunci di lavoro, infatti le percentuali variano dal 15% al 19% tra le 10:00 e le 17:00. Diversamente, fuori dall’orario di lavoro, la quota di annunci scende al 5,5% tra le 8:00 e le 9:00 e all’11% circa tra le 18:00 e le 19:00,  mentre non raggiunge il 4% per le restanti fasce orarie.<br>
Per quanto riguarda i giorni della settimana, gli annunci vengono pubblicati maggiormente dal lunedì e venerdì, con percentuali che oscillano tra il 18% e il 20%. 
Nonostante le quote trascurabili, anche il sabato e la domenica vi è la pubblicazione degli annunci di lavoro (3,1% e 1,8% rispettivamente). 

</p>