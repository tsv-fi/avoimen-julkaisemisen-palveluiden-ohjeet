# HTML-muotoisten artikkelien asettelu Journal.fi-julkaisuissa

Journal.fi:n käyttämä [Open Journal Systems](https://pkp.sfu.ca/ojs/) mahdollistaa HTML-muotoisten julkaisujen lisäämisen julkaisujen sivustoille. Käytännössä harva julkaisu kuitenkaan hyödyntää tätä mahdollisuutta. Käytännössä HTML-julkaisujen tukeminen vaati kolme asiaa:

1. Oikean lisäosan käyttämisen,
2. CSS-tyylitiedoston kirjoittamisen ja
3. julkaisujen oikean muotoilun.

## 1. Oikea lisäosa

Journal.fissä on tarjolla kaksi eri HTML-lisäosaa. Toinen on TSV:n ylläpitämä ja toimii paremmin useimmissa tapauksissa. Molemmat löytyvät oman julkaisun ylläpitosivulta seuraavasta polusta: **Asetukset => Verkkosivuston asetukset => Lisäosat**.

TSV:n ylläpitämä lisäosa on nimeltään **Vaihtoehtoinen HTML-artikkelin lisäosa**

Sen voi aktivoida laittamalla lisäosan kohdalla raksin ruutuun.

## 2. CSS-tyylitiedosto

HTML-lisäosa ottaa valmiin julkaisun tiedoston ja lataa sen verkkoselaimessa. Valitettavasti oletuksena siihen ei sisälly muotoiluja, joten lopputulos on yksi iso pötkö tekstiä. Jotta lopputulos on hieman luettavampi, järjestelmään täytyy ladata oma tyylitiedosto. Se onnistuu polusta: **Asetukset => Verkkosivuston asetukset => Lisäasetukset => Julkaisun tyylitiedosto**.

Tyylitiedosto täytyy olla valmiiksi kirjoitettu omaan CSS-tiedostoonsa ja se ladataan järjestelmään sellaisenaan.

[Voit ladata tämän perusasettelun sisältävän CSS-tiedoston](_assets/StyleSheet.css) ja muokata sitä vastaamaan paremmin omia tarpeitasi tai ladata sen sellaisenaan järjestelmään.

# 3. Julkaisujen oikea muotoilu

Lisäosan ja tyylitiedoston lisäksi tarvitaan vielä julkaistavat tekstit oikeassa muodossa.

Käytännössä kyseessä on hyvin yksinkertainen HTML-tiedosto, joka ladataan sellaisenaan Journal.fi-järjestelmään. Järjestelmä tekee siihen jotain muutoksia, kun se ladataan, joten lopputulos ei ihan vastaa alkuperäistä tiedostoa.

[Voit ladata valmiin esimerkkitiedoston](_assets/malli.html) ja katsoa, että julkaistavissa teksteissä on tarvittavat osiot. Käytännössä lopulliset julkaistavat tiedostot luodaan taitto-ohjelmassa samaan tapaan kuin julkaistavat PDF-tiedostot.
