# Päivämäärän ja ajan muotoilu

OJS- ja OMP-järjestelmien versio 3.4 tukee julkaisijoiden mahdollisuutta määrittää omat päivämäärien ja aikojen esitystavat.  
Asetukset löytyvät kohdasta **Asetukset > Verkkosivusto > Asetukset > Päivämäärä ja aika**.

Jokaiselle kielelle voidaan määrittää oma muotoilunsa. Julkaisija voi valita valmiin oletusasetuksen tai määrittää oman päivämäärä- ja aikamuodon. Omissa muodoissa käytetään PHP-ohjelmointikielen aikaleimaformaatteja, joiden kirjaimet kuvaavat päivämäärän ja kellonajan eri osia. 

Näitä kirjaimia yhdistelemällä saadaan haluttu päivämäärän ja/tai kellonajan muoto. Esimerkiksi `d.m.Y` tuottaa `21.04.2025`-muotoisen päivämäärän.  

Jos mukaan halutaan kiinteitä kirjaimia tai sanoja, niiden eteen täytyy lisätä kenoviivat (`\`). Esimerkiksi `d. F\t\a Y` tuottaa `21. huhtikuuta 2025` -muotoisen päivämäärän. Ilman `\t\a`-osaa tulos olisi `21. huhtikuu 2025`.


## PHP-päivämäärän ja -ajan muuttujat

| Merkki | Esimerkki (2025-04-07 09:05:03) | Selitys |
|---|---|---|
| `d` | 07 | Päivämäärä kahdella numerolla (01–31) |
| `j` | 7 | Päivämäärä ilman etunollaa |
| `m` | 04 | Kuukausi kahdella numerolla (01–12) |
| `n` | 4 | Kuukausi ilman etunollaa |
| `Y` | 2025 | Vuosi nelinumeroisena |
| `y` | 25 | Vuosi kahdella numerolla |
| `F` | huhtikuu / April | Kuukauden nimi (lokalisoitu) |
| `M` | huhti / Apr | Kuukauden nimen lyhennys (lokalisoitu) |
| `H` | 09 | Tunnit 24h muodossa (00–23) |
| `G` | 9 | Tunnit 24h muodossa ilman etunollaa |
| `h` | 09 | Tunnit 12h muodossa (01–12) |
| `g` | 9 | Tunnit 12h muodossa ilman etunollaa |
| `i` | 05 | Minuutit (00–59) |
| `A` | AM | Aikamerkintä isoilla kirjaimilla (AM/PM) |
| `a` | am | Aikamerkintä pienillä kirjaimilla (am/pm) |
| `l` | maanantai / Monday | Viikonpäivän nimi (lokalisoitu) |
| `D` | ma / Mon | Viikonpäivän lyhennys |


## Esimerkkejä 

Alla on esimerkkejä yleisistä päivämäärä- ja aikamuodoista eri kielillä.

### Suomi

| Tyyppi | PHP-kaava | Esimerkki |
|---|---|---|
| Päivämäärä (lyhyt) | `d.m.Y` | 21.10.2025 |
| Päivämäärä (pitkä, sisältää "ta") | `d. F\t\a Y` | 21. lokakuuta 2025 |
| Kellonaika (24h) | `H:i` | 14:05 |
| Kellonaika sekunneilla | `H:i:s` | 14:05:33 |
| Päivämäärä + aika (lyhyt) | `d.m.Y H:i` | 21.10.2025 14:05 |
| Päivämäärä + aika (teksti, sisältää "ta" ja "klo") | `d. F\t\a Y \k\l\o H.i` | 21. lokakuuta 2025 klo 14.05 |
| ISO (yleinen) | `Y-m-d` | 2025-10-21 |
| ISO + aika | `Y-m-d H:i` | 2025-10-21 14:05 |

---

### Ruotsi

| Tyyppi | PHP-kaava | Esimerkki |
|---|---|---|
| Päivämäärä (lyhyt) | `Y-m-d` | 2025-10-21 |
| Päivämäärä (pitkä) | `d F Y` | 21 oktober 2025 |
| Kellonaika (24h) | `H:i` | 14:05 |
| Kellonaika sekunneilla | `H:i:s` | 14:05:33 |
| Päivämäärä + aika (lyhyt) | `Y-m-d H:i` | 2025-10-21 14:05 |
| Päivämäärä + aika (teksti) | `Y-m-d \k\l\. H.i` | 2025-10-21 kl. 14.05 |

---

### Englanti (UK)

| Tyyppi | PHP-kaava | Esimerkki |
|---|---|---|
| Date (short) | `d/m/Y` | 21/10/2025 |
| Date (long) | `d F Y` | 21 October 2025 |
| Time (24h) | `H:i` | 14:05 |
| Time with seconds | `H:i:s` | 14:05:33 |
| Date + time (short) | `d/m/Y H:i` | 21/10/2025 14:05 |
| Date + time (long) | `d F Y \a\t H:i` | 21 October 2025 at 14:05 |
| ISO (common) | `Y-m-d` | 2025-10-21 |

---

### Englanti (US)

| Tyyppi | PHP-kaava | Esimerkki |
|---|---|---|
| Date (short) | `m/d/Y` | 10/21/2025 |
| Date (long) | `F j, Y` | October 21, 2025 |
| Time (12h) | `g:i A` | 2:05 PM |
| Time (12h, leading zero) | `h:i A` | 02:05 PM |
| Date + time (short, 12h) | `m/d/Y g:i A` | 10/21/2025 2:05 PM |
| Date + time (long, 12h) | `F j, Y \a\t g:i A` | October 21, 2025 at 2:05 PM |
| ISO (common) | `Y-m-d` | 2025-10-21 |


