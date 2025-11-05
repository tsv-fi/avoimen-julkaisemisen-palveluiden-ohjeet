# DOI-tunnisteiden käyttö Journal.fi-palvelussa

[Yleistä tietoa DOI-tunnisteiden käytöstä ja niitä koskevista sopimuksista löydät erillisestä ohjeesta](yleiset/doi.md). Tässä ohjeessa neuvotaan DOI-tunnisteiden käyttöä Journal.fi-palvelussa ja siinä käytössä olevassa Open Journal Systems -järjestelmässä (OJS).

## Lehden asetukset

Vaadittavat asetukset koskevat kolmea kokonaisuutta:

1. Lehden yleiset asetukset
3. Crossref-lisäosan asetukset
3. DOI-asetukset

### Lehden yleiset asetukset

Kun uusi DOI-tunniste rekisteröidään, artikkelia koskeva metadata lähetetään tunnistetta hallinnoivalle taholle. Keskeinen osa tätä metadataa tulee lehden yleisistä asetuksista.

Alla mainitut asetukset täytetään kaikilla käytössä olevilla kielillä.

**Settings => Journal / Asetukset => Julkaisu / Inställningar => Tidskrift**

* Julkaisun nimi / Journal name
* Julkaisun alkukirjaimet / Journal initials
* Julkaisun lyhenne / Journal abbreviation
* Julkaisija / Publisher
* ISSN (yksi tai molemmat)

**Settings => Journal => Contact / Asetukset => Julkaisu => Yhteystiedot / Inställningar => Tidskrift => Kontakt**

* Pääasiallinen yhteyshenkilö (nimi ja sposti)
* Teknisen tuen yhteyshenkilö (nimi ja sposti)

**Settings => Workflow => Submission/ Asetukset => Työnkulku => Käsikirjoituksen vastaanotto / Inställningar => Arbetsflöde => Bidrag**

* Kohdasta Submission Metadata / Käsikirjoituksen metatiedot valitse References / Lähdeviitteet / Referenser (rasti kahteen kohtaan)
* Save / Tallenna / Spara

### CrossRef-lisäosan asetukset

CrossRef-lisäosan asetuksia varten tarvitaan TSV:ltä CrossRefin käyttäjätunnus ja salasana, ks. [DOI-tunnisteita koskeva yleinen ohjeistus](yleiset/doi.md).

* Aktivoi Crossref-lisäosa kohdasta **Asetukset > Verkkosivusto > Lisäosat / Settings > Website / Plugins**
* Avaa asetukset kohdasta **Asetukset > Jakelu > DOIt > Rekisteröinti / Settings > Distribution > DOIs > Registration**
* Anna lomakkeeseen tallettajan nimi ja sähköposti sekä Crossrefin käyttäjätunnus ja salasana. 
* Valitse lopuksi DOI-tunnisteiden automaattinen tallennus ja varmista, ettei testirajapinta ole valittuna. 
* Paina **Tallenna / Save**.

### DOI-asetukset

**Settings => Distribution => DOIs / Asetukset => Jakelu => DOIt**

* Aktivoi DOI-tunnuste käyttön sivulla näkyvästä valinnasta. Aktivoinnin jälkeen muut asetukset tulevat esille.
* Valitse kohteet, joille DOI-tunnisteet määritetään: **valitaan vain kohta Articles / Artikkelit / Artiklar**
* **Automaattinen DOI-tunnusten osoitus / Automatic DOI Assignment** Mikäli kaikille lehden sisällöille annetaan DOI, niin tästä asetuksesta voi valita joko teknisen toimituksen tai tuotannon, jolloin DOI luodaan sisällölle automaattisesti. **Huom!** Jos ette anna kaikille lehden sisällöille DOI-tunnusta, niin älkää käyttäkö automaattista DOI-tunnuksen luontia, vaan lisätkää DOIt halutuille artikkeleille manuaalisesti.
* **DOI Prefix** _oma prefix_, joka on saatu TSV:ltä (esim. 10.1234)
* **DOI Suffix** Käytä mukautettua rakennetta / Custom pattern
    * Käsikirjoitukset/Submissions: **%j.%a**
* Paina **Save/Tallenna**

## DOI-tunnisteiden lisääminen artikkeleihin

Alla on kuvattu miten DOI-tunnus liitetään artikkelin metadataan. Tämän lisäksi on aina hyvä huolehtia siitä, että tunnus liitetään myös artikkelin kokotekstitiedoistoihin.

Kun yllä kuvatut asetukset ovat kunnossa, tapahtuu DOI-tunnisteen lisääminen tavallisesti käsikirjoituksen tuotantovaiheessa.

DOI-tunnuksia voi lisätä kohdasta **DOI-tunnukset / DOIs / DOIs**.

Valitse artikkelit joille haluat lisätä DOI-tunnukset ja valitse **Massatoiminnot / Bulk Actions > Osoita DOI-tunnuksia / Assign DOIs**

### DOI-tunnisteen rekisteröinti

Mikäli CrossRef-lisäosan asetuksista on otettu käyttöön automaattinen rekisteröinti, OJS rekisteröi DOI-tunnisteet numeron julkaisun jälkeen 1-24 tunnin viiveellä.

Vaihtoehtoisesti tunnisteet voi rekisteröidä heti numeron julkaisun jälkeen manuaalisesti. Rekisteröinti tapahtuu kohdasta **DOI-tunnukset / DOIs / DOIs** Avautuvalla sivulla näkyy listaus kaikista artikkeleista sekä niiden DOI-tunnusten tila. 

Julkaistujen artikkeleiden DOI-tunnukset voi rekisteröidä painamalla **Talleta kaikki / Deposit All / Deponera Alla**. Ole kärsivällinen kun järjestelmä tekee tallennusta, siinä voi kulua pidempi aika. Järjestelmä ilmoittaa kun tallennus on valmis. Vaihtoehtoisesti voit saada virheilmoitukset, jossa kerrotaan mitä puutteita rekisteröitävän artikkelin kuvailutiedoissa on.


## DOI-tunnisteet vanhoille artikkeleille

Mikäli lehti haluaa hakea DOI-tunnisteita vanhoille artikkeleille ja on mukana TSV:n solmimassa sopimuksessa, tulee lehden olla aina ensin yhteydessä sähköpostitse [tuki@tsv.fi](mailto:tuki@tsv.fi). Vanhojen artikkeleiden tunnisteita koskevista kustannuksista vastaa lehti itse.
