# Huoltoneuvoja – Lapsen edun ja viranomaistoiminnan poikkihallinnollinen tietopankki vaikeissa huoltoriidoissa

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Oikeustila](https://img.shields.io/badge/Oikeustila-06.09.2026-blue.svg)](4.%20Lainsäädäntökartta.md)
[![Open Science](https://img.shields.io/badge/Open_Science-Data_&_Methods-green.svg)](research_data/)
[![Journal Draft](https://img.shields.io/badge/FinJeHeW-Manuscript_Ready-orange.svg)](finjehew_manuscript_draft.md)

> **Huoltoriidan olemassaolo ei laajenna viranomaisen toimivaltaa, mutta se ei myöskään poista viranomaisen omia lakisääteisiä tehtäviä.**

Tämä avoin repositorio sisältää laajan, autonomisilla tekoälyagenteilla ja oikeusdogmaattisella analyysilla kootun poikkihallinnollisen tutkimus- ja soveltamiskokonaisuuden. Hanke ratkaisee käytännön sosiaalityössä, kouluissa, varhaiskasvatuksessa ja tuomioistuimissa toistuvaa **monialaisen viranomaisloukun** ongelmaa, jossa lapsen lakisääteinen tuki tai asioiden selvittäminen halvaantuu vanhempien välisen konfliktin vuoksi.

---

## 📌 Sisältö ja pikaopas

1. [Miksi tämä projekti on olemassa?](#-miksi-tämä-projekti-on-olemassa)
2. [Kenelle aineisto on tarkoitettu?](#-kenelle-aineisto-on-tarkoitettu)
3. [Tietopankin rakenne ja luvut](#-tietopankin-rakenne-ja-luvut)
4. [Malliasiakirjat ja toimintakortit](#-malliasiakirjat-ja-toimintakortit)
5. [Säädösvalinta ja lainsäädännön ajallinen soveltaminen](#-säädösvalinta-ja-lainsäädännön-ajallinen-soveltaminen)
6. [Tekoälymenetelmä ja toistettavuus](#-tekoälymenetelmä-ja-toistettavuus)
7. [Akateeminen julkaisu ja viittaaminen](#-akateeminen-julkaisu-ja-viittaaminen)
8. [Vastuuvapauslauseke (Disclaimer)](#-vastuuvapauslauseke-disclaimer)
9. [Lisenssi](#-lisenssi)

---

## 🎯 Miksi tämä projekti on olemassa?

Vaativassa huolto- ja tapaamisriidassa vanhempien kertomukset ovat usein jyrkässä ristiriidassa. Tällöin viranomaiset ajautuvat helposti **toimivaltaparalyysiin**:
* **Koulu ja varhaiskasvatus** saattavat jättää lapsen oppimisen tuen tai koulupsykologin palvelut järjestämättä vedoten siihen, että huoltajat eivät pääse yhteisymmärrykseen tai että "asia on käräjäoikeudessa".
* **Lastensuojelu ja sosiaalihuolto** saattavat leimata yhteydenotot "pelkäksi huoltoriidaksi" ja jättää perheen palvelutarpeen arvioinnin tai lapsen henkilökohtaisen tapaamisen tekemättä (vastoin mm. eduskunnan oikeusasiamiehen ratkaisua EOAK/4063/2022).
* **Terveydenhuollossa** epäröidään hoidon aloittamista huoltajien erimielisyyden vuoksi, vaikka potilaslaki velvoittaa arvioimaan alaikäisen omaa päätöskykyä ja antamaan kiireellisen hoidon viipymättä.
* **Asiakirjoihin kirjataan** toisen vanhemman esittämiä väitteitä ja syytöksiä objektiivisina faktoina ilman tietolähteen merkintää, mikä rikkoo hallintolain puolueettomuusvaatimusta ja GDPR:n tietosuojavaatimuksia.

Tämä tietopankki jäsentää **kunkin viranomaisen itsenäiset toimivaltarajat, lakisääteisen ratkaisupakon, neutraalin kirjaamisen standardit sekä sovellettavat oikeussuojakeinot**.

---

## 👥 Kenelle aineisto on tarkoitettu?

| Kohderyhmä | Keskeinen hyöty ja luettavat osiot |
| :--- | :--- |
| **Sosiaalityöntekijät ja esihenkilöt** | • [Luku 7: Lastensuojelun ja sosiaalihuollon toimintapolku](7.%20Lastensuojelun%20ja%20sosiaalihuollon%20toimintapolku.md)<br>• [Luku 5: Viranomaisten vastuunjakotaulukko](5.%20Viranomaisten%20vastuunjakotaulukko.md)<br>• [Liite A: Viranomaisen tarkistuslista](research_data/liite_A_viranomaisen_tarkistuslista.md) |
| **Koulut ja varhaiskasvatus** | • [Luku 6: Päätösvallan matriisi koulua ja varhaiskasvatusta varten](6.%20Päätösvallan%20matriisi%20koulua%20ja%20varhaiskasvatusta%20varten.md)<br>• Selkeä rajaus: huoltajan kuuleminen ei tarkoita huoltajan veto-oikeutta opetuksen tuessa |
| **Huoltajat ja vanhemmat** | • [Liite B: Vanhemman toimintakortti](research_data/liite_B_vanhemman_toimintakortti.md)<br>• [Luku 11: Käytännön 30 päivän toimintasuunnitelma](11.%20Käytännön%2030%20päivän%20toimintasuunnitelma.md)<br>• [Valmiit malliasiakirjat (1–10)](12.%20Malliasiakirjat%20-%20osa%20I%20mallit%201-5.md) |
| **Juristit ja oikeusavustajat** | • [Luku 8: Oikeuskäytäntö](8.%20Oikeuskäytäntö.md) (mm. KKO:2025:65, KHO:2026:62)<br>• [Luku 10: Oikeussuojakeinot ja valitustiet](10.%20Oikeussuojakeinot.md)<br>• [Luku 4: Lainsäädäntökartta pykälätasolla](4.%20Lainsäädäntökartta.md) |
| **Tutkijat ja AI-kehittäjät** | • [FinJeHeW-tieteellinen käsikirjoitus](finjehew_manuscript_draft.md)<br>• Moniagenttisen normisystematisoinnin promptit, metodit ja arkkitehtuuri [research_data/](research_data/) |

---

## 📚 Tietopankin rakenne ja luvut

Koko aineisto on jaettu aihepiireittäin selkeisiin moduuleihin:

* **[00. Kokonaisuus ja sisällysluettelo](00_SISALLYSLUETTELO_JA_KOKONAISUUS.md)** – Koko raportin kartta ja lukujen tilanne.
* **[03. Käsitteet ja oikeuslähteiden painoarvo](3.%20Käsitteet%20ja%20oikeuslähteiden%20painoarvo.md)** – Oikeuslähdeoppi, normihierarkia ja vaikeiden termien ("vieraannuttaminen", "huoltokiusaaminen", "prosessiväkivalta") oikeudellinen arvio.
* **[04. Lainsäädäntökartta](4.%20Lainsäädäntökartta.md)** – Sovellettavat lait sektoreittain (siviili-, sosiaali-, opetus-, terveys- ja hallinto-oikeus).
* **[05. Viranomaisten vastuunjakotaulukko](5.%20Viranomaisten%20vastuunjakotaulukko.md)** – Toimivaltarajat: Käräjäoikeus vs. Lastensuojelu vs. Koulu vs. Terveydenhuolto.
* **[06. Päätösvallan matriisi koulua ja varhaiskasvatusta varten](6.%20Päätösvallan%20matriisi%20koulua%20ja%20varhaiskasvatusta%20varten.md)** – Milloin tarvitaan molempien huoltajien lupa ja milloin koulu tekee päätöksen itsenäisesti.
* **[07. Lastensuojelun ja sosiaalihuollon toimintapolku](7.%20Lastensuojelun%20ja%20sosiaalihuollon%20toimintapolku.md)** – Määräajat (7 arkipäivää, 3 kk), lapsen tapaaminen ja turvallisuusarvio.
* **[08. Oikeuskäytäntö](8.%20Oikeuskäytäntö.md)** – KKO:n ennakkoratkaisut (mm. KKO:2025:65), KHO:n ratkaisut (KHO:2026:62) ja EIT-ratkaisulinjat.
* **[09. Oikeudellisesti sallittu ja ongelmallinen viranomaistoiminta](9.%20Oikeudellisesti%20sallittu%20ja%20ongelmallinen%20viranomaistoiminta.md)** – Hallintolain hyvän hallinnon periaatteet vs. virkavirheet ja laiminlyönnit.
* **[10. Oikeussuojakeinot](10.%20Oikeussuojakeinot.md)** – Muutoksenhaku, oikaisuvaatimus, hallintovalitus, muistutus, kantelu ja vahingonkorvaus.
* **[11. Käytännön 30 päivän toimintasuunnitelma](11.%20Käytännön%2030%20päivän%20toimintasuunnitelma.md)** – Nelivaiheinen järjestelmällinen malli tilanteen vakauttamiseksi ja oikeusturvan varmistamiseksi.
* **[12. Malliasiakirjat (Osa I & Osa II)](12.%20Malliasiakirjat%20-%20osa%20I%20mallit%201-5.md)** – 10 käyttövalmista asiakirjapohjaa perusteluineen.
* **[16. Executive Summary](research_data/osa_16_executive_summary.md)** – Tiivistetty kokonaiskuva viranomaistoiminnan pelisäännöistä.
* **[20–24. Erillisteemat](20.%20Neutraalin%20kirjauksen%20malli.md)** – Neutraali kirjaaminen, avoimet oikeuskysymykset ja koottu lähdeluettelo.

---

## 📝 Malliasiakirjat ja toimintakortit

Repositorio sisältää 10 käyttövalmista malliasiakirjaa, joissa on valmiit pykäläviittaukset ja täyttöohjeet:

1. **Malli 1:** Pyyntö muutoksenhakukelpoisesta hallintopäätöksestä (palvelun epäämistilanne)
2. **Malli 2:** Julkisuuslain mukainen asiakirjapyyntö ja asianosaisjulkisuus
3. **Malli 3:** Virheellisen tai leimaavan kirjauksen oikaisu- ja täydennyspyyntö (GDPR 16 art. / asiakastietolaki)
4. **Malli 4:** Sosiaalihuollon muistutus (sosiaalihuollon asiakaslaki 23 §)
5. **Malli 5:** Hallintokantelu valvontaviranomaiselle (aluehallintovirasto / Valvira / LVV)
6. **Malli 6:** Esiopetuksen ja koulunkäynnin tukipäätöksen pyyntö
7. **Malli 7:** Ilmoitus tapaamisesteestä ja vaatimus korvaavista tapaamisista
8. **Malli 8:** Lapsen terveydenhuollon ja opiskeluhuollon selvityspyyntö
9. **Malli 9:** Pyyntö monialaisen asiantuntijaryhmän koollekutsumisesta
10. **Malli 10:** Vaatimus kiireellisen turvallisuusarvion tekemisestä

Lisäksi kansiosta `research_data/` löytyvät:
* **[Liite A: Viranomaisen tarkistuslista](research_data/liite_A_viranomaisen_tarkistuslista.md)**
* **[Liite B: Vanhemman toimintakortti](research_data/liite_B_vanhemman_toimintakortti.md)**
* **[Liite C: Päätös- ja määräaikataulukko](research_data/liite_C_paatos_ja_maaraaikataulukko.md)**
* **[Liite D: Tapahtuma-aikajanan pohja](research_data/liite_D_tapahtuma_aikajanan_pohja.md)**
* **[Liite E: Todisteiden ja tietolähteiden luokittelu](research_data/liite_E_todisteiden_ja_tietolahteiden_luokittelu.md)**

---

## ⚖️ Säädösvalinta ja lainsäädännön ajallinen soveltaminen

Tietopankin oikeudellinen pohja on koottu noudattaen tiukkaa tutkimusmetodologiaa:

1. **Säädösten valintaperusteet:**
   * **Toimivaltaperuste:** Säännökset, jotka määräävät viranomaiselle itsenäisen velvollisuuden selvittää ja ratkaista asia (non liquet -kielto).
   * **Erillisyyskriteeri:** Lapsen elatusapu, tapaamisoikeus, lastensuojelu ja vanhempien omaisuusositus ovat oikeudellisesti toisistaan erillisiä prosesseja.
   * **Tiedonhallintakriteeri:** Asiakastietolain (703/2023) ja GDPR:n tiedonsaanti- ja salassapitosäännökset monialaisessa yhteistyössä.
2. **Ajallinen ankkurointi ja intertemporaalioikeus:**
   * **Aikaleima:** Aineisto on ankkuroitu tarkasti syyskuuhun 2026 (Finlex säädöskokoelman numeroon 768/2026 asti).
   * **Siirtymäsäännökset:** Asiakastietolain (703/2023) vaiheittaiset Kanta-liittymiset (2024–2026), oppimisen tuen uudistuksen voimaantuloajat (1.8.2025 ja 1.8.2026) sekä elatuslain (1055/2025) voimaantulo 1.1.2026 on systematisoitu erikseen.
   * **Aineellinen vs. prosessuaalinen oikeus:** Viranomaisen toiminnan laillisuutta arvioidaan aina *tapahtumahetkellä* voimassa olleen lain nojalla, kun taas muutoksenhaku ja oikeussuojakeinot määräytyvät *ratkaisuhetken* mukaan.

---

## 🤖 Tekoälymenetelmä ja toistettavuus

Aineisto on luotu käyttäen autonomista moniagenttiarkkitehtuuria (yhteensä yli 6 tuntia itsenäistä agenttien suoritusaikaa). Agenttijärjestelmälle määriteltiin tiukat oikeusdogmaattiset säännöt hallusinaatioiden ehkäisemiseksi:
* Vaatimus ankkuroitua suoraan Finlexin ajantasaiseen säädöskokoelmaan pykälätasolla.
* Kielto käyttää ei-oikeudellisia leimaavia käsitteitä ratkaisuperusteina ilman konkreettisia tekoja ja lapsivaikutuksia.
* Ristiintarkistus ylimpien tuomioistuinten ja laillisuusvalvojien ennakkoratkaisuihin.

Metodologiaa, promptirakenteita ja järjestelmäarkkitehtuuria koskevat tiedostot ovat tutkittavissa kansiossa `research_data/` ja tiedostossa [2026-09-03_tutkimusprompt-chatgpt.md](2026-09-03_tutkimusprompt-chatgpt.md).

---

## 🎓 Akateeminen julkaisu ja viittaaminen

Hankkeesta on laadittu vertaisarvioitavan tiedelehden (*Finnish Journal of eHealth and eWelfare*, FinJeHeW) vaatimusten mukainen tieteellinen käsikirjoitus:
📄 **[finjehew_manuscript_draft.md](finjehew_manuscript_draft.md)**

### Viittausohje (Citation)

Jos hyödynnät tätä aineistoa tutkimuksessa, opinnäytteessä tai viranomaisohjeissa, viittaa repositorioon seuraavasti:

```bibtex
@misc{nurmela2026huoltoneuvoja,
  author       = {Nurmela, Pekka},
  title        = {Huoltoneuvoja: Monialaisen hyvinvointioikeuden ja lapsen edun poikkihallinnollinen systematisointi autonomisilla tekoälyagenteilla},
  year         = {2026},
  publisher    = {GitHub},
  journal      = {GitHub repository},
  howpublished = {\url{https://github.com/pnurmela/eroriita_huoltoneuvoja}}
}
```

Repositorio sisältää myös koneellisen [`CITATION.cff`](CITATION.cff) -tiedoston.

---

## ⚠️ Vastuuvapauslauseke (Disclaimer)

Tämä tietopankki ja sen sisältämät malliasiakirjat, toimintakortit ja taulukot ovat **tutkimuksellinen ja tiedonhallinnollinen systematisointi**, joka on koottu tekoälyavusteisesti ja toimitettu asiantuntijatyönä.

1. **Ei yksilöllistä oikeudellista neuvontaa:** Materiaali tarjoaa yleistä tietoa Suomen lainsäädännöstä ja viranomaismenettelyistä. Se ei korvaa asianajajan, julkisen oikeusavustajan tai toimivaltaisen viranomaisen antamaa tapauskohtaista oikeudellista tai sosiaalihuollon neuvontaa.
2. **Oikeustilan muutos:** Lainsäädäntö ja oikeuskäytäntö muuttuvat jatkuvasti. Aineisto on tarkistettu syyskuussa 2026 vallinneen oikeustilan mukaan. Käyttäjän tulee aina varmistaa sovellettavan pykälän ajantasaisuus Finlexistä.
3. **Päätöskohtaiset muutoksenhakuohjeet:** Yksittäisessä asiassa noudatetaan aina viranomaisen antamaa virallista valitus- tai oikaisuvaatimusosoitusta.

---

## 📄 Lisenssi

Tämän repositorion sisältö (tekstit, taulukot, analyysit ja malliasiakirjat) on julkaistu avoimella **Creative Commons Nimeä 4.0 Kansainvälinen (CC BY 4.0)** -lisenssillä.

Saat vapaasti jakaa, kopioida, muokata ja hyödyntää aineistoa missä tahansa välineessä myös kaupallisesti, kunhan mainitset alkuperäisen lähteen ja tekijän asianmukaisesti. Lisenssin täydellinen teksti löytyy tiedostosta [LICENSE](LICENSE).
