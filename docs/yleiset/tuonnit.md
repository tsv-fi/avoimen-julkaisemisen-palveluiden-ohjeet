# Vanhojen aineistojen tuonti

Vanhojen aineistojen tuontiin on kolme vaihtoehtoa.

1. **Pikajulkaisulisäosan käyttö**. Pikajulkaisulisäosalla voi ohittaa järjestelmän normaalin toimitusprosessin ja tuoda yksittäisiä artikkeleita yhtä lomaketta täyttämällä. Tämä vaihtoehto sopii parhaiten pienemmille määrille. Pikajulkaisulisäosan lomakkeen täyttöön kuluu aikaa noin 5 minuuttia per artikkeli.
2. **Excel-tuonti**. Toisena vaihtoehtona julkaisija voi tallentaa artikkeleita koskevat tiedot Excel-muotoon, jonka TSV muuntaa OJS-järjestelmän ymmärtämään XML-muotoon. Muuntotyö tehdään tuntityönä, jota koskeva veloitus kannattaa varmistaa etukäteen. TSV ei osallistu Excel-taulukon koostamiseen, mutta neuvoo sitä koskevassa työssä. Excel-tiedoston mukana pitää olla halutussa tiedostomuodossa tallennetut kokotekstitiedostot (tavallisesti pdf) ja niihin tulee viitata tiedostojen nimillä excel-taulukosta.
3. **Elektra-lehdet**. Mikäli lehteä on julkaistu aiemmin Elektra-tietokannassa, muista mainita asiasta, kun tiedustelet vanhojen numeroiden tuonnista. Osa artikkeleiden kuvailutiedoista on mahdollista saada esitäytettynä Elektran tiedoista, mutta myös tämä tuontitapa vaatii lehden toimituskunnan osallistumista kuvailutietojen täydentämiseen.


## Excel-tuonti

Vanhojen numeroiden tuonti on lisäpalvelu, josta TSV veloittaa [avoimen julkaisemisen palveluita koskevan hinnastonsa mukaisen maksun](https://tsv.fi/fi/palvelut/avoimen-julkaisemisen-palvelut/hinnasto). Julkaisijan vastuulla tuonneissa on kuvailutietojen koostaminen ja aineistojen toimittaminen digitoidussa muodossa. TSV:n vastuulla on julkaisijan toimittamien aineistojen ja kuvailutietojen muuntaminen julkaisujärjestelmän ymmärtämään muotoon ja testituontien teko. TSV:n työpanos on tavallisesti 4-5 tunnin luokkaa.

Tuonti etenee seuraavasti:

1. Ottakaa yhteyttä TSV:hen ja ilmoittakaa, että haluatte julkaista palvelussa vanhoja aineistoja ([tuki@tsv.fi](mailto:tuki@tsv.fi)).
2. Muodostakaa julkaisijan tarpeisiin sopiva excel-taulukko alla olevien ohjeiden mukaisesti ja varmistakaa TSV:ltä, että siinä on kaikki tarvittava täyttämällä kuvailutiedot muutamien sisältöjen osalta ja lähettämällä taulukko tarkistettavaksi ([tuki@tsv.fi](mailto:tuki@tsv.fi)).
3. Kun taulukon rakenne on kunnossa, täyttäkää excel-taulukko ja lähettäkää se tämän jälkeen yhdessä kokotekstitiedostojen kanssa TSV:lle. Tallentakaa kokotekstitiedostot kaikki yhteen hakemistoon, ei siis jaettuna alahakemistoihin. Tiedostot voi toimittaa TSV:lle esimerkiksi jakamalla ne OneDriven tai Google Driven kaltaisten palveluiden kautta.
4. TSV tarkistaa taulukon tiedot ja pyytää tarvittaessa korjauksia
5. Kun excel-tiedosto on kunnossa, TSV muuntaa sen XML-muotoon ja tekee koesiirron testialustalle. Toimituskunnan jäsenet tarkistavat tässä vaiheessa, että tiedot ovat siirtyneet oikein. Mahdolliset korjaukset tehdään aina Excel-taulukkoon, jonka uusi versio toimitetaan sitten TSV:lle, eli älä tee korjauksia suoraan testialustalle siirrettyihin sisältöihin. 
6. Tarkistuksen jälkeen tehdään siirto varsinaiseen tuotantopalveluun ja TSV veloittaa siirrosta.


## Excel-taulukon rakenne Journal.fi-palvelua käyttäville julkaisijoille

Alla olevan kuvauksen mukaisesti tuotetun esimerkkitiedoston voi ladata lisäosan Github-sivuilta:

* [Yksinkertainen mallitiedosto](https://github.com/ajnyga/tsvConverter/raw/master/exampleMinimal.xlsx)
* [Monimutkainen mallitiedosto](https://github.com/ajnyga/tsvConverter/raw/master/exampleAdvanced.xlsx)

Myös ohjeistus löytyy englanniksi lisäosan Github-sivulta: [ajnyga/tsvConverter: Excel to OJS3 XML conversion tool](https://github.com/ajnyga/tsvConverter/blob/master/README.md)

**Huom!** Älä käytä esimerkiksi artikkelin otsikossa tai kirjoittajan nimessä pelkkiä ISOJA KIRJAIMIA. Pakolliset kentät merkitty tähdellä.


### Artikkelin tiedot

``prefix``
otsikon alkuun tuleva “The”, “A” jne.

``title`` *
artikkelin otsikko 

``subtitle``
artikkelin alaotsikko 

``abstract``
artikkelin abstrakti

``keywords``
asiasanat, esim. sana1; sana2; sana3

``sponsors``
rahoittajat, esim. rahoittaja1; rahoittaja2; rahoittaja3

``language`` *
mikäli artikkeleita on useilla eri kielillä, voidaan yksittäisen artikkelin antaa tähän sarakkeeseen. Esimerkiksi en, fi, sv, de, fr

``articleCopyrightYear``
tekijänoikeuden vuosi, yleensä sama kuin julkaisuvuosi	

``articleCopyrightHolder``
tekijän tai muun tekijänoikeuksien haltijan nimi

``articleLicenseUrl``
annetaan lisenssin koko url, esimerkiksi _http://creativecommons.org/licenses/by/4.0	_

``doi``
artikkelin DOI-tunnus esimerkiksi _10.1234/art.182_


### Numeron tiedot

``issueDatepublished`` *
numeron julkaisupäivä (muodossa vvvv-kk-pp)

``issueVolume`` *				

``issueNumber`` *			

``issueYear`` *				

``issueTitle``
Numeron otsikko, jos sellainen on erikseen

``sectionTitle`` *
osaston nimi, esim, “Artikkelit” [voi olla jo OJS:ssä]

``sectionAbbrev`` *
osaston lyhenne, esim “ART”

``pages``
esim. 10-25

``seq`` *
juokseva numerointin numeron sisällä, jolla määritellään artikkeleiden järjestys sisällysluettelossa. Numeron ensimmäinen artikkelin on siis aina 1.

### Kertaantuvat kentät

Kertaantuvia kenttiä ovat kirjoittajia ja kokotekstejä koskevat kentät. Jokaisessa artikkelissa pitää olla vähintää yksi kirjoittaja ja yksi tiedosto. Mikäli jossain tuotavassa artikkelissa on esimerkiksi kolme kirjoittajaa, lisätään alla kuvattuja kenttien kokonaisuuksia kolmet niin, että nimen perässä oleva numero vaihtuu.

``authorFirstname1`` *

``authorMiddlename1``

``authorLastname1`` *

``authorEmail1``

``authorAffiliation1``

``authorBio1``

``authorOrcid1``

``file1`` *
filename.pdf _ei ääkkösiä eikä välilyöntejä tiedostonimeen! Tämä nimi viittaa kokotekstitiedostoon, joka lähetetään excel-taulukon mukana.

``fileLabel1`` *
yleensä “PDF, liitetiedostojen yhteydessä esim. “Kuva 1”

``fileGenre1`` *
yleensä “Article Text”

``fileLocale``
fi, en, us

### Tietojen tuonti useammalla kielellä

Mikäli lehdessä on artikkeleita useilla eri kielillä, anna yksittäisen artikkelin kielikoodi yllä mainittuun language-sarakkeeseen. Tällöin esimerkiksi annetun artikkelin otsikko tulee täsmätä annetun kielen kanssa.

Mikäli yksittäisen artikkelin kohdalla halutaan antaa metadataa useilla eri kielillä, esimerkiksi englanninkielinen abstrakti, lisää tauluun abstraktia varten ylimääräinen sarake muodossa lokalisaatio:sarakkeen_nimi. Eli jos suomenkielisiin artikkeleihin on lisätty englanninkielinen abstrakti, se tallennetaan sarakkeeseen **en:abstract**.

#### Lokalisaatioiden tunnisteet

fi - suomi

en - englanti

sv - ruotsi

fr - ranska

de - saksa
