# DOI-tunnisteiden käyttö Edition.fi-palvelussa

[Yleistä tietoa DOI-tunnisteiden käytöstä ja niitä koskevista sopimuksista löydät erillisestä ohjeesta](yleiset/doi.md). Tässä ohjeessa neuvotaan DOI-tunnisteiden käyttöä Edition.fi-palvelussa ja siinä käytössä olevassa Open Monograph Press -järjestelmässä (OMP).

## Julkaisijan sivuston asetukset

Vaadittavat asetukset koskevat kolmea kokonaisuutta:

1. Julkaisijan yleiset asetukset
3. Crossref-lisäosan asetukset
3. DOI-asetukset

### Julkaisijan yleiset asetukset

Kun uusi DOI-tunniste rekisteröidään, kirjaa koskeva metadata lähetetään tunnistetta hallinnoivalle taholle. Keskeinen osa tätä metadataa tulee julkaisijan yleisistä asetuksista.

Alla mainitut asetukset täytetään kaikilla käytössä olevilla kielillä.

**Settings > Press / Asetukset > Julkaisija**

* Julkaisijan nimi / Journal name
* Julkaisijan alkukirjaimet / Journal initials
* Julkaisijan nimi / Press Publisher Name (ONIX-tiedot, käytä pääasiallista kieliversiota)

**Settings > Press > Series / Asetukset > Julkaisija > Sarja**

* Valitse jokaisen lisätyn sarjan edestä sininen kolmio > Muokkaa ja lisää sarjan asetuksiin ISSN-tunnukset.

**Settings > Press > Contact / Asetukset > Julkaisija > Yhteystiedot**

* Pääasiallinen yhteyshenkilö (nimi ja sposti)
* Teknisen tuen yhteyshenkilö (nimi ja sposti)

**Settings => Workflow => Submission/ Asetukset => Työnkulku => Käsikirjoituksen vastaanotto**

* Kohdasta Submission Metadata / Käsikirjoituksen metatiedot valitse References / Lähdeviitteet (rasti kahteen kohtaan)
* Save / Tallenna

### CrossRef-lisäosan asetukset

CrossRef-lisäosan asetuksia varten tarvitaan TSV:ltä CrossRefin käyttäjätunnus ja salasana.

* Aktivoi Crossref-lisäosa kohdasta **Asetukset > Verkkosivusto > Lisäosat / Settings > Website / Plugins**
* Avaa asetukset kohdasta **Asetukset > Jakelu > DOIt > Rekisteröinti / Settings > Distribution > DOIs > Registration**
* Anna lomakkeeseen tallettajan nimi ja sähköposti sekä Crossrefin käyttäjätunnus ja salasana. Varmista ettei testirajapintaa koskeva asetus ole valittuna.
* Paina **Tallenna / Save**.

### DOI-asetukset

**Settings => Distribution => DOIs / Asetukset => Jakelu => DOIt**

* Aktivoi DOI-tunnuste käyttön sivulla näkyvästä valinnasta. Aktivoinnin jälkeen muut asetukset tulevat esille.
* Valitse kohteet, joille DOI-tunnisteet määritetään: **valitaan kirjat / books, jos haluaa myös luvuille DOI-tunnuksia, niin lisäksi luvut / chapters**
* **DOI Prefix** > _oma prefix_, joka on saatu TSV:ltä (esim. 10.1234)
* **DOI Suffix** > Käytä mukautettua rakennetta / Custom pattern
    * Käsikirjoitukset/Submissions: %p.%m
    * Luvut/Chapters: %p.%m.c%c
* Paina **Save/Tallenna**

## DOI-tunnisteiden lisääminen kirjoihin

Alla on kuvattu miten DOI-tunnus liitetään kirjan metadataan. Tämän lisäksi on aina hyvä huolehtia siitä, että tunnus liitetään myös kirjan kokotekstitiedoistoihin.

Kun yllä kuvatut asetukset ovat kunnossa, tapahtuu DOI-tunnisteen lisääminen tavallisesti käsikirjoituksen tuotantovaiheessa.

DOI-tunnuksia voi lisätä kohdasta **DOI-tunnukset / DOIs / DOIs**.

Valitse kirjat joille haluat lisätä DOI-tunnukset ja valitse **Massatoiminnot / Bulk Actions > Osoita DOI-tunnuksia / Assign DOIs**

### DOI-tunnisteen rekisteröinti

Rekisteröinti tapahtuu kohdasta **DOI-tunnukset / DOIs / DOIs** Avautuvalla sivulla näkyy listaus kaikista kirjoista sekä niiden DOI-tunnusten tila. 

Julkaistujen kirjojen DOI-tunnukset voi rekisteröidä painamalla **Talleta kaikki / Deposit All / Deponera Alla**. Ole kärsivällinen kun järjestelmä tekee tallennusta, siinä voi kulua pidempi aika. Järjestelmä ilmoittaa kun tallennus on valmis. Vaihtoehtoisesti voit saada virheilmoitukset, jossa kerrotaan mitä puutteita rekisteröitävän kirjan kuvailutiedoissa on.

## DOI-tunnisteet vanhoille kirjoille

Mikäli julkaisija haluaa hakea DOI-tunnisteita vanhoille kirjoille, tulee olla aina ensin yhteydessä sähköpostitse [tuki@tsv.fi](mailto:tuki@tsv.fi). Vanhojen kirjojen tunnisteita koskevista kustannuksista vastaa julkaisija itse.
