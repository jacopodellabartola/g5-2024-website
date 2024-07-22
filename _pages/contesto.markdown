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
}
</style>

# Perché Linkedin?

  <div style="flex: 50%;">
    <div class="justified">
      <p><br><br><br>Per quanto riguarda la piattaforma scelta per raccogliere dati, non abbiamo avuto dubbi: Linkedin è stata la nostra prima scelta.<br>
    LinkedIn è un social network professionale, tra i più diffusi al mondo, ad oggi conta circa 830 milioni di utenti nel mondo, di cui oltre 16 milioni in Italia e oltre 58 milioni di aziende (LinkedIn, 2024). [grafico] <br></p>
    </div>
  </div>
</div>
<div class="justified">
  <p>È il più utilizzato dalle aziende per trovare candidati, infatti lo scopo principale è quello di mettere in contatto i professionisti tra loro e creare nuove opportunità di lavoro. Rispetto alle altre piattaforme, Linkedin ci ha permesso di fare un’analisi più completa grazie alla presenza del numero di candidati e alle altre variabili che in altre piattaforme non sono disponibili.</p>
</div>


<div style="display: flex; justify-content: center; align-items: center;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo1_DistTotLavori_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
<br>
<div style="display: flex; justify-content: center; align-items: center; ">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo2_DistTipoLavori_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
<br>
<div style="display: flex; justify-content: center; align-items: center; ">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo3_DistTipoSede_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>
<br>
<div style="display: flex; justify-content: center; align-items: center; ">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Jacopo4_DistDimAzienda_monochrome_NoContainer.json" style="width: 100%"></vegachart>
</div>

<br>

<div style="display: flex; justify-content: center; align-items: center;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Dona_chart_ore.json" style="width: 100%"></vegachart>
</div>


<div style="display: flex; justify-content: center; align-items: center;">
<vegachart schema-url="{{site.baseurl}}/assets/charts/Dona_chart_settimana.json" style="width: 100%"></vegachart>
</div>
