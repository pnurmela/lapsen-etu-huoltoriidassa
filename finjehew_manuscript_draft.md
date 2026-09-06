# Monialaisen hyvinvointi- ja lapsioikeuden systematisointi autonomisilla tekoälyagenteilla: Säädösten valintaperusteet, ajallinen soveltaminen ja tiedonhallinnan rajapinnat

**Synthesizing Multidisciplinary Welfare and Child Law Using Autonomous AI Agents: Statutory Selection Criteria, Intertemporal Validity, and Information Management Interfaces**

*Käsikirjoitusluonnos Finnish Journal of eHealth and eWelfare (FinJeHeW) -lehteen*
*Artikkelityyppi: Tieteellinen artikkeli / Katsaus (Scientific Article / Review)*

---

### Tekijätiedot ja affiliaatiot
**Kirjoittaja:** Pekka Nurmela ym. / Huoltoneuvoja-tutkimushanke  
**Affiliaatio:** Positive Productions / Itsenäinen tutkimusryhmä  
**Yhteystiedot:** pekka@positiveproductions.fi  
**Tutkimusajankohta:** Syyskuu 2026  

---

## Tiivistelmä

**Tavoite:** Tässä tutkimuksessa tarkastellaan autonomisten tekoälyagenttien hyödyntämistä monialaisen hyvinvointioikeuden, sosiaali- ja terveydenhuollon tiedonhallinnan sekä lapsioikeuden laajassa normisystematisoinnissa. Erityisenä tutkimuskohteena ovat menetelmät, joilla tekoälyjärjestelmä valitsee sovellettavat säädökset poikkihallinnollisissa konfliktitilanteissa (huoltoriidat, lastensuojelu, varhaiskasvatus ja perusopetus) sekä kykenee huomioimaan lainsäädännön ajallisen soveltamisen (intertemporaalioikeus, sote-uudistuksen siirtymäsäännökset ja asteittain voimaan tulevat lait).

**Aineisto ja menetelmät:** Aineistona käytettiin Suomen ajantasaista lainsäädäntöä (Finlex, syyskuu 2026), korkeimpien oikeuksien ennakkoratkaisuja, ylimpien laillisuusvalvojien (EOAK, OKV) ratkaisulinjauksia sekä Opetushallituksen ja THL:n velvoittavia normiperusteita. Moniagenttinen arkkitehtuuri suoritti kuuden tunnin itsenäisen laskenta-ajon, jossa normimassa jäsenneltiin toimivaltamatriiseiksi, tiedonhallintapoluiksi ja prosessikaavioiksi. Analyysimenetelmänä käytettiin oikeusdogmaattisen ja oikeusinformaatiotieteellisen analyysin synteesiä, jossa tekoälyn valintamekanismeja ja ajallista ankkurointia arvioitiin kriittisesti.

**Tulokset:** Agenttijärjestelmä valitsi tarkasteluun 18 keskeistä säädöstä viideltä eri hallinnonalalta. Säädösvalinta perustui funktionaaliseen toimivaltajaotteluun ja ratkaisupakkoon: säädöskenttä rajattiin niihin normeihin, jotka estävät viranomaisia ajautumasta toimivaltaparalyysiin vanhempien ristiriitaisten vaatimusten edessä. Tutkimus osoittaa, että tekoälyagentit kykenevät mallintamaan säädösten ajallista dynamiikkaa luotettavasti vain silloin, kun järjestelmään koodataan eksplisiittinen ajallisen ankkuroinnin arkkitehtuuri (cutoff-päiväys, säädöshistorian diff-analyysi sekä tapahtumahetken ja ratkaisuhetken erottaminen).

**Pohdinta ja johtopäätökset:** Autonomiset agentit voivat nopeuttaa merkittävästi sosiaali- ja terveydenhuollon tiedonhallinnan monialaisten rajapintojen mallinnusta. Suurimmat riskit liittyvät hallusinaatioiden sijaan ajallisen soveltamisen virheisiin, jos malli sekoittaa kumotun kunnallisen sääntelyn, voimassa olevan hyvinvointialuelainsäädännön sekä tulevat lakimuutokset. Tulokset tarjoavat suuntaviivoja eWelfare- ja eHealth-järjestelmien sääntelylogiikan kehittämiseen.

**Avainsanat (YSO/MeSH):** sosiaalioikeus, terveydenhuoltolaki, lapsen etu, tekoäly, tiedonhallinta, tietosuoja, intertemporaalioikeus

---

## Abstract

**Aims:** This study investigates the utilization of autonomous multi-agent artificial intelligence (AI) systems for large-scale legal synthesis and information architecture across multidisciplinary welfare law, healthcare information systems, and child protection. The study focuses specifically on two critical methodological aspects: (1) the criteria and logic by which autonomous agents identify and select relevant statutes across inter-administrative boundaries (custody disputes, social services, healthcare, and education), and (2) how AI systems account for intertemporal legal validity and multi-year statutory transitions (such as the health and social services reform and staggered legislation in Finland).

**Methods:** The primary data comprised the Finnish statutory corpus (Finlex up to September 2026), precedents of the Supreme Court and Supreme Administrative Court, ombudsman rulings (Parliamentary Ombudsman), and binding administrative regulations from the Finnish National Agency for Education (EDUFI) and the Finnish Institute for Health and Welfare (THL). A multi-agent framework executed a 6-hour computational reasoning run, structuring substantive law into jurisdiction matrices, data governance paths, and administrative workflows. The evaluation employed legal doctrinal analysis combined with health and welfare informatics methodologies.

**Results:** The multi-agent system identified and systematized 18 foundational statutes across five separate administrative sectors. Statutory selection was governed by a functional jurisdiction criterion: identifying norms that enforce an administrative obligation to decide (non liquet prohibition) irrespective of parental conflict. The results demonstrate that multi-agent LLM systems can reliably track temporal validity only when augmented with strict temporal anchoring protocols, distinguishing between *de lege lata*, transitional periods (e.g., Act 703/2023 on Social and Health Data), and pending legislative proposals (*de lege ferenda*).

**Conclusion:** Autonomous agents offer significant potential for synthesizing multi-professional eWelfare workflows and cross-sectoral documentation standards. However, safeguarding against temporal hallucinations requires specialized legal prompt architectures that enforce explicit temporal coordinates.

**Keywords:** social welfare law, health legislation, child welfare, artificial intelligence, information management, data protection, intertemporal law

---

## 1. Johdanto

Sosiaali- ja terveydenhuollon sekä perusopetuksen ja varhaiskasvatuksen monialainen yhdyspinta on yksi suomalaisen hyvinvointivaltion haastavimmista tiedonhallinnollisista ja oikeudellisista solmukohdista [1, 2]. Kun lapsiperheen tilanne kriisiytyy vaikeaksi huolto- ja tapaamisriidaksi, perhe asioi samanaikaisesti lukuisissa eri tietojärjestelmissä ja viranomaisprosesseissa: hyvinvointialueen perheoikeudellisissa palveluissa, lastensuojelussa, erikoissairaanhoidossa, perusterveydenhuollossa, varhaiskasvatuksessa, koulussa ja yleisissä tuomioistuimissa [3, 4].

Käytännön työssä tämä monitoimijaisuus johtaa toistuvasti ilmiöön, jota voidaan kutsua **toimivaltaparalyysiksi** tai **viranomaisloukuksi**:
* Koulu saattaa evätä tai lykätä oppilaan tarvitsemia tukitoimia odottaessaan käräjäoikeuden tulevaa huoltajuusratkaisua.
* Lastensuojelu saattaa kuitata perheen yhteydenotot "pelkkänä vanhempien keskinäisenä riitana" ja jättää lapsen oman palvelutarpeen arvioimatta.
* Terveydenhuollon ammattilaiset kokevat epävarmuutta siitä, milloin toisen huoltajan suostumus on hoidon ehdoton edellytys ja milloin alaikäisen oma päätöskyky tai potilaslain mukainen hoidon kiireellisyys syrjäyttää huoltajien erimielisyyden [5].
* Sosiaali- ja terveydenhuollon asiakastietolain (703/2023) ja EU:n yleisen tietosuoja-asetuksen (GDPR) soveltaminen aiheuttaa tilanteita, joissa toisen vanhemman oikeutta omiin ja lapsensa tietoihin rajoitetaan tai laajennetaan virheellisin perustein.

Tekoälyn ja suurten kielimallien (LLM) kehitys on avannut uusia mahdollisuuksia tiedonhallinnan ja laajan normimassan jäsentämiseen [6, 7]. FinJeHeW-lehdessä on hiljattain tarkasteltu tekoälysovelluksia sosiaalityössä ja todettu, että vaikka tekoäly voi automatisoida rutiineja ja koota hajanaista dataa, sen soveltaminen edellyttää vahvaa kriittistä arviointia ja ymmärrystä eettisistä sekä oikeudellisista reunaehdoista [6].

Tässä artikkelissa raportoidaan ja analysoidaan empiiristä tutkimusasetelmaa, jossa autonominen tekoälyagenttijärjestelmä suoritti kuuden tunnin laskenta-ajon aikana laajan, monialaisen hyvinvointioikeudellisen tutkielman systematisoinnin. Artikkelin erityisenä tavoitteena on vastata kahteen menetelmälliseen ydinkysymykseen, jotka ovat kriittisiä eHealth- ja eWelfare-tiedonhallinnan luotettavuudelle:
1. **Säädösten valintaperusteet:** Millä oikeudellisilla ja tiedonhallinnollisilla kriteereillä tekoälyjärjestelmä valitsee monialaisesta säädösmassasta relevantit normit, ja miten se erottaa toisistaan eri sektoreiden toimivaltarajat?
2. **Ajallisen soveltamisen hallinta (intertemporaalioikeus):** Miten tekoäly kykenee huomioimaan eri ajankohtina voimassa olevat säädökset, asteittain voimaan tulevat siirtymäsäännökset sekä historiallisten ja tulevien normien erot ilman ajallisia hallusinaatioita?

---

## 2. Aineisto ja menetelmät

### 2.1 Agenttijärjestelmän arkkitehtuuri ja suoritus

Tutkimuksessa hyödynnettiin moniagenttiarkkitehtuuria, joka toimi iteratiivisessa suunnittelu- ja tutkimustilassa (Planning Mode). Järjestelmä koostui koordinoivasta pääagentista, erikoistuneesta tiedonhaku- ja analyysiagentista sekä tiedostojärjestelmään integroituista validointityökaluista. Agenttien suoritusaika oli yhteensä 6 tuntia, jonka aikana järjestelmä suoritti kymmeniä rinnakkaisia hakuja, lainsäädäntötekstien ristiintaulukointeja sekä oikeuskäytännön vertailuja.

Aineistokokonaisuus kattaa 24 pääkappaletta, 10 malliasiakirjaa sekä useita toimintakortteja ja prosessiliitteitä, joiden kokonaislaajuus ylittää 150 000 sanaa.

### 2.2 Primääriaineisto ja normilähteet

Tutkimuksessa käytettiin seuraavia primäärilähteitä:
1. **Säädöskokoelma (Finlex):** Ajantasainen lainsäädäntö tarkasteluhetkellä (syyskuu 2026, säädöskokoelman numeroon 768/2026 saakka).
2. **Tuomioistuinratkaisut:** Korkeimman oikeuden ennakkopäätökset (erityisesti tuore KKO:2025:65 koskien lapsen kuulemista ja päätöksentekoa), Korkeimman hallinto-oikeuden vuosikirjapäätökset sekä Euroopan ihmisoikeustuomioistuimen (EIT) perhe-elämän suojaa (EIS 8 art.) koskeva oikeuskäytäntö.
3. **Laillisuusvalvontaratkaisut:** Eduskunnan oikeusasiamiehen (EOAK) ja Oikeuskanslerinviraston (OKV) ratkaisut, erityisesti EOAK/4063/2022, jossa määritellään viranomaisen aktiivinen toimintavelvollisuus huoltoriidasta riippumatta.
4. **Viranomaismääräykset:** Opetushallituksen velvoittavat määräykset (Esi- ja perusopetuksen opetussuunnitelman perusteet 2026, Varhaiskasvatussuunnitelman perusteet 2026) sekä THL:n ohjeistukset sosiaalihuollon asiakasasiakirjojen kirjaamisesta.

### 2.3 Analyysimenetelmä

Tutkimuksessa yhdistettiin lainopillinen (oikeusdogmaattinen) systematisointi ja tietojärjestelmätieteellinen informaatioarkkitehtuurin analyysi. Tekoälyagenttien suorittamaa päättelyä testattiin syöttämällä järjestelmälle monimutkaisia skenaarioita, joissa vanhempien intressit, lapsen edun arviointi ja viranomaisten tiedonsaantioikeudet olivat keskenään ristiriidassa.

---

## 3. Tulokset

### 3.1 Säädösten valintaperusteet monialaisessa kentässä

Agenttijärjestelmä valitsi tarkasteluun 18 ydinsäädöstä (Taulukko 1). Analyysi osoitti, että mielekäs ja hallusinaatiovapaa säädösvalinta ei voi perustua pelkkään avainsanahakuun (kuten "lapsi" tai "huolto"), sillä tällöin aineisto laajenee hallitsemattomasti toisarvoisiin vero-, vakuutus- ja etuusnormeihin.

Sen sijaan agenttijärjestelmän valintalogiikka strukturoitiin kolmen kriteerin perusteella:
1. **Toimivaltaperuste (Kompetenssikriteeri):** Säädökset, jotka määrittelevät viranomaisen *omatoimisen ja itsenäisen ratkaisu- ja selvittämisvelvollisuuden* (non liquet -kielto hallinto-oikeudessa).
2. **Substanssikohtainen erillisyyskriteeri:** Normit, jotka oikeudellisesti estävät eri asioiden sekoittamisen keskenään. Esimerkiksi lapsen elatus (laki 704/1975) ja lapsen tapaamisoikeus (laki 361/1983) ovat juridisesti täysin erillisiä: elatusavun maksamatta jättäminen ei oikeuta estämään tapaamisia, eikä tapaamisten katkeaminen oikeuta elatusmaksulakkoon.
3. **Tiedonhallinnan ja salassapidon poikkeuskriteeri:** Normit, jotka sääntelevät tiedon liikkumista sektoreiden välillä ilman huoltajan suostumusta (erityisesti Asiakastietolaki 703/2023, Sosiaalihuollon asiakaslaki 812/2000 ja Oppilas- ja opiskelijahuoltolaki 1287/2013).

**Taulukko 1. Tutkimukseen valitut keskeiset säädökset ja niiden valintaperusteet.**

| Sektori | Säädös ja numero | Keskeinen soveltamisala | Valintaperuste ja tiedonhallinnollinen merkitys |
| :--- | :--- | :--- | :--- |
| **Perus- ja ihmisoikeudet** | Perustuslaki (731/1999)<br>YK:n lapsen oikeuksien sopimus (SopS 59–60/1991)<br>Istanbulin sopimus (SopS 52–53/2015) | PL 6, 7, 10, 19, 21 §<br>LOS 3, 12 art.<br>Istanbul 31, 48 art. | Kaikkien muiden lakien tulkintakehys; lapsen osallisuus ja suoja väkivallalta; turvallisuusarvioinnin ensisijaisuus suhteessa sovitteluun. |
| **Perhe- ja huolto-oikeus** | Laki lapsen huollosta ja tapaamisoikeudesta (361/1983)<br>Täytäntöönpanolaki (619/1996)<br>Laki lapsen elatuksesta (704/1975) | Huolto, asuminen, tapaaminen, valvotut vaihdot, elatusapu | Erottaa siviiliriidan sosiaalihuollosta; määrittelee yhteishuollon rajat; estää elatuksen ja tapaamisoikeuden kytkemisen toisiinsa. |
| **Sosiaalihuolto ja lastensuojelu** | Sosiaalihuoltolaki (1301/2014)<br>Lastensuojelulaki (417/2007)<br>Sosiaalihuollon asiakaslaki (812/2000)<br>Sote-järjestämislaki (612/2021) | Palvelutarpeen arviointi, lastensuojelutarpeen selvitys, hyvä kohtelu | Määrittää määräajat (7 arkipäivää / 3 kk); velvoittaa arvioimaan lapsen tuen tarpeen vanhempien riidasta riippumatta; ohjaa neutraalia kirjaamista. |
| **Varhaiskasvatus ja opetus** | Varhaiskasvatuslaki (540/2018)<br>Perusopetuslaki (628/1998)<br>Oppilas- ja opiskelijahuoltolaki (1287/2013) | Oppimisen ja kehityksen tuki, kouluympäristön turvallisuus, opiskeluhuolto | Osoittaa opetuksen järjestäjän itsenäisen päätösvallan tukipäätöksissä; erottaa huoltajan kuulemisen (ei veto-oikeutta) huoltajan suostumuksesta. |
| **Terveydenhuolto** | Terveydenhuoltolaki (1326/2010)<br>Potilaslaki (785/1992) | Hoitoon pääsy, alaikäisen päätöskyky, tiedonsaanti | Alaikäisen itsemääräämisoikeus ja kyky kieltää tietojen luovutus huoltajalle; kiireellisen hoidon toteutus ilman molempien huoltajien lupaa. |
| **Hallinto ja tiedonhallinta** | Hallintolaki (434/2003)<br>Julkisuuslaki (621/1999)<br>Asiakastietolaki (703/2023)<br>EU:n tietosuoja-asetus (2016/679) | Selvittämisvelvollisuus (31 §), asianosaisjulkisuus, salassapito | Viranomaisen puolueettomuus ja ratkaisupakko; estää toisen vanhemman väitteen kirjaamisen objektiivisena totuutena ilman lähdemerkintää. |

### 3.2 Ajallisen soveltamisen hallinta (Intertemporaalioikeus)

Oikeudellisen tiedonhallinnan ja tekoälyagenttien suurin haaste ei ole voimassa olevan lakitekstin löytäminen, vaan **lakien ajallisen sovellettavuuden (intertemporaalisuuden) hallinta**. Sosiaali- ja terveydenhuollon lainsäädäntö elää jatkuvassa muutoksessa, ja käytännön asiakastapauksissa arvioidaan usein vuosia sitten tapahtuneita tapahtumia tämän päivän oikeusvaikutuksilla.

Agenttitutkimuksessa kehitettiin ja validoitiin neliportainen malli ajallisen dynamiikan hallitsemiseksi:

#### 1. Ajallinen ankkurointi (Temporal Cut-off Date)
Järjestelmän kaikille päättelyketjuille asetettiin ehdoton nykyhetken aikaleima (tutkimuksessa 3.9.2026, Finlex säädösnumero 768/2026). Tämä esti mallia sekoittamasta eri vuosikymmenten säädöksiä toisiinsa ja pakotti mallin tarkistamaan kunkin säädöksen ajantasaisen voimaantulotiedon.

#### 2. Voimassaolon tilaluokittelu
Jokainen oikeusnormi ja pykälä luokiteltiin neljään toisensa poissulkevaan tilaan:
* **A. Voimassa oleva oikeus (*de lege lata*):** Säädökset, joita sovelletaan tarkasteluhetkellä (esim. Lapsenhuoltolaki 361/1983 sellaisena kuin se on muutettuna vuoden 2019 uudistuksella ja vuoden 2023 hyvinvointialuemuutoksilla lailla 626/2022).
* **B. Hyväksytty, vaiheittain voimaan tuleva sääntely (Siirtymäsäännökset):** Erityisen kriittinen sosiaali- ja terveydenhuollon asiakastietolaissa (703/2023), jonka velvoitteet Kanta-liittymisistä, tahdonilmaisujen tallentamisesta ja sosiaalihuollon rekisterinkäytöstä astuvat voimaan porrastetusti vuosina 2024, 2025 ja 2026. Samoin perusopetuksen oppimisen tuen uudistus astui voimaan pääosin 1.8.2025, mutta varhennetun oppivelvollisuuden osalta vasta 1.8.2026.
* **C. Hyväksytty tuleva laki:** Säädökset, jotka on julkaistu säädöskokoelmassa mutta joiden voimaantulopäivä on tulevaisuudessa (esim. oppivelvollisuuslain 5 §:n muutos lailla 711/2026, joka tulee voimaan vasta 1.1.2027).
* **D. Vireillä olevat uudistukset (*de lege ferenda*):** Hallituksen esitykset ja komiteamietinnöt, joilla ei ole oikeudellista velvoittavuutta ja jotka agentti eristi ehdottomasti sovellettavasta normimassasta.

#### 3. Tapahtumahetken oikeus vs. ratkaisuhetken oikeus
Erityisesti valvonta- ja kanteluasioissa (EOAK, Valvira, aluehallintovirastot) tekoälyagentille ohjelmoitiin sääntö, jonka mukaan *viranomaisen toiminnan lainmukaisuutta arvioidaan tapahtumahetkellä voimassa olleen lain mukaan, mutta prosessuaalisia oikeussuojakeinoja käytetään ratkaisuhetken mukaan*. Esimerkiksi ennen 1.1.2023 tehtyjä kuntien sosiaalityöntekijöiden toimia ei voitu arvioida hyvinvointialueita koskevan järjestämislain (612/2021) nojalla, vaikka kanteluratkaisu annettaisiin vuonna 2026.

---

## 4. Pohdinta

### 4.1 Tekoälyagenttien luotettavuus ja "ajalliset hallusinaatiot"

Kielimallit ovat tunnetusti alttiita anakronismeille ja ajallisille harhoille. Tyypillisessä arkkitehtuurissa malli saattaa yhdistää sujuvasti 1980-luvun lapsenhuoltolain alkuperäisiä säännöksiä, vuoden 2014 sosiaalihuoltolain pykäliä ja vuoden 2026 Opetushallituksen määräyksiä tiedostamatta, että käsitteet (kuten "kunnallinen sosiaalilautakunta" vs. "hyvinvointialueen toimivaltainen viranhaltija") ovat muuttuneet.

Tässä tutkimuksessa tehty 6 tunnin agenttiajo osoitti, että autonominen päättely saadaan tieteellisesti ja ammatillisesti luotettavaksi vain, jos järjestelmää ei päästetä tekemään yleistä vapaata synteesiä ilman normihierarkkista ja ajallista ankkurointia. Kun säädöksille rakennettiin tiukka metatietorakenne (voimaantulo, kumoamiset, siirtymäajat), agentti kykeni tunnistamaan hienovaraisia poikkeuksia, kuten sen, että lapsen elatuksesta annetun lain uudistus (1055/2025) toi 1.1.2026 alkaen hyvinvointialueille uuden velvollisuuden selvittää elatusavun muuttamista Kelan ilmoitusten perusteella.

Erityisen merkittävänä empiirisenä löydöksenä tutkimus paljasti **viranomaisohjeistuksen laahaamisen suhteessa lainsäädäntöön (guidance vs. statute lag)**: Esimerkiksi syyskuussa 2026 Opetushallituksen (OPH) virallisilla verkkosivuilla neuvottiin edelleen kansalaisia hakemaan oikaisua varhaiskasvatuksen tukipäätöksiin Aluehallintovirastolta (AVI), vaikka laki Lupa- ja valvontavirastosta (530/2025) siirsi tehtävän uudelle valtakunnalliselle Lupa- ja valvontavirastolle (LVV) jo 1.1.2026 alkaen ja lakkautti AVIt. Mikäli tekoälyjärjestelmä tekisi tiedonhakua vain pintapuolisella verkkosivuhalulla (perinteinen RAG ilman normihierarkiaa), se antaisi kansalaiselle vanhentuneen viranomaisosoitteen ja vaarantaisi tiukan määräajan (perusopetuksessa 14 päivää, varhaiskasvatuksessa 30 päivää). Oikeudellinen tekoäly vaatii siten aina primäärisen normipohjan toissijaisen informaatio-ohjauksen edelle.

Vastaavasti tuomioistuinlinjausten ajallinen dynamiikka osoittautui kriittiseksi: ratkaisussa **KKO:2025:17** vahvistettiin (äänin 3–2), että nuoren mielipiteenmuodostuksen itsenäistyminen estää vetoamasta yli kolme vuotta vanhaan kuulemiseen huoltohakemuksen nopeuttamiseksi, kun taas ratkaisu **KHO:2026:62** osoitti, että 12 vuotta täyttäneen lapsen lakisääteistä itsenäistä puhevaltaa ei voida pelastaa toisen osapuolen (kuten sijaisvanhemman) tekemällä valituksella, ellei lapsen omaa puhevaltaa ole käytetty ajallaan.

### 4.2 Merkitys eWelfare- ja eHealth-tiedonhallinnalle

Tutkimuksen tuloksilla on suoraa annettavaa sosiaali- ja terveydenhuollon tiedonhallinnan kehittäjille. Sosiaali- ja terveydenhuollon asiakastietolaki (703/2023) korostaa tietojen käsittelyn käyttötarkoitussidonnaisuutta ja oikeusperustetta. Kun huoltoriidassa olevien vanhempien tietoja kirjataan Kanta-palveluihin ja hyvinvointialueen asiakastietojärjestelmiin, kirjaamisen neutraalisuus ja tietolähteen eksplisiittinen erottaminen ovat avainasemassa:
* Työntekijän oma havainto, lapsen oma kertomus ja toisen vanhemman esittämä väite on pidettävä tietokantarakenteessa toisistaan erillään.
* Toisen vanhemman esittämää syytöstä (esim. "isä vieraannuttaa" tai "äiti pahoinpitelee") ei saa kirjata diagnoosiksi tai objektiiviseksi tosiasiaksi ilman viranomaisen omaa tutkintaa.
* Lapsen itsemääräämisoikeus ja kyky kieltää tietojensa luovutus huoltajalle (potilaslaki 9 §, asiakastietolaki 53 §) edellyttää tietojärjestelmiltä kykyä suojata alaikäisen tietoja dynaamisesti tapauskohtaisen päätöskyvyn arvioinnin perusteella.

### 4.3 Tutkimuksen rajoitteet

Tutkimus perustui simuloidun agenttijärjestelmän suorittamaan normianalyysiin ja oikeuslähteiden systematisointiin. Vaikka normipohja kattoi säädöskokoelman kattavasti, tutkimuksessa ei käsitelty elävää potilas- tai asiakasdataa, eikä mallia integroitu suoraan hyvinvointialueiden tuotantotietojärjestelmiin. Jatkotutkimuksessa olisi arvioitava, miten vastaava agenttiavusteinen säädösmallinnus toimii reaaliaikaisena päätöksenteon tukijärjestelmänä sosiaalityöntekijöiden ja opiskeluhuollon kuraattorien arjessa.

---

## 5. Johtopäätökset

Autonomiset tekoälyagentit voivat toimia tehokkaana työkaluna monialaisen hyvinvointioikeuden ja sosiaali- ja terveydenhuollon tiedonhallinnan systematisoinnissa. Keskeiset löydökset ovat:
1. **Säädösvalinta vaatii toimivalta- ja ratkaisupakkokriteerejä:** Tekoäly ei voi seuloa monialaista säädöskenttää avainsanapohjaisesti, vaan sen on nojattava hallintolain mukaiseen selvittämisvelvollisuuteen ja sektorikohtaisiin itsenäisiin toimivaltoihin.
2. **Ajallinen ankkurointi on laadun elinehto:** Ilman selkeää intertemporaalista arkkitehtuuria tekoäly tuottaa anakronistisia tulkintoja, joissa vanha kuntapohjainen sääntely ja uusimmat sote-normit sekoittuvat.
3. **Monialainen kirjaaminen ratkaisee oikeusturvan:** Tekoälyn jäsentämä säädöskartta osoittaa, että vaikeassa perhekonfliktissa lapsen edun toteutuminen nojaa tietolähteiden erotteluun ja kirjaamisen puolueettomuuteen digitaalisissa asiakastietojärjestelmissä.

---

## Sidonnaisuudet ja eettiset lausunnot (Conflict of Interest)

Kirjoittajat ilmoittavat, että tutkimukseen ei liity taloudellisia tai henkilökohtaisia sidonnaisuuksia, jotka olisivat voineet vaikuttaa tutkimuksen tuloksiin tai puolueettomuuteen. Tutkimus on suoritettu noudattaen Tutkimuseettisen neuvottelukunnan (TENK) hyvän tieteellisen käytännön periaatteita. Tekoälyä on käytetty aineiston analyysin ja systematisoinnin apuvälineenä artikkelissa kuvatun menetelmän mukaisesti; ihmistutkijat kantavat täyden vastuun tekstin sisällöstä, lähteistä ja johtopäätöksistä.

---

## Lähteet (References)

[1] Salovaara S, Mykkänen J, von Gerich H. Sosiaali- ja terveydenhuollon tiedonhallinta systeemisenä kokonaisuutena. Finnish Journal of eHealth and eWelfare. 2026;18(2):92–95.  
[2] Virtanen A, Jokinen E. Sosiaalihuollon asiakastietovarannon käyttöönotto – pistemäisestä informaatio-ohjauksesta monitoimijaiseen dialogiin. Finnish Journal of eHealth and eWelfare. 2026;18(2):236–239.  
[3] Salovaara S, Brusila E, Harrikari T. Social network analysis in child protection information management research: A scoping review. Finnish Journal of eHealth and eWelfare. 2026;18(2):186–200.  
[4] Ikonen J, Kinnunen UM, Liljamo P, Kuusisto H, Vehko T. Multidisciplinary documentation as a tool on shared knowledge creation – registered nurses’ view. Finnish Journal of eHealth and eWelfare. 2026;18(2):159–174.  
[5] Kuusisto H, Saranto K, Huhtala H, Keränen T. Interpretations and views of hospital specialists and residents on the decision-making process, documentation, and education of the Do Not Attempt Resuscitation (DNAR) order. Finnish Journal of eHealth and eWelfare. 2026;18(2):201–212.  
[6] Salovaara S, Outila M, Heilala V, Hautala S. Artificial intelligence in social work: A rapid review. Finnish Journal of eHealth and eWelfare. 2026;18(2):115–131.  
[7] Miettinen J, Sund R. From register data to useful information: Framework for automating real-world evidence reporting. Finnish Journal of eHealth and eWelfare. 2026;18(2):213–224.  
[8] Suomen perustuslaki 731/1999. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/1999/19990731  
[9] Laki lapsen huollosta ja tapaamisoikeudesta 361/1983. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/1983/19830361  
[10] Laki sosiaali- ja terveydenhuollon asiakastietojen käsittelystä 703/2023. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/2023/20230703  
[11] Sosiaalihuoltolaki 1301/2014. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/2014/20141301  
[12] Lastensuojelulaki 417/2007. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/2007/20070417  
[13] Perusopetuslaki 628/1998. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/1998/19980628  
[14] Varhaiskasvatuslaki 540/2018. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/2018/20180540  
[15] Hallintolaki 434/2003. Finlex. Saatavilla: https://www.finlex.fi/fi/laki/ajantasa/2003/20030434  
[16] Eduskunnan oikeusasiamies. Ratkaisu EOAK/4063/2022: Lastensuojelun ohjeistus ja yhteistyö vaikeissa huoltoriidoissa. 2022.  
[17] Korkein oikeus. Ennakkopäätös KKO:2025:65: Lapsen kuuleminen ja huoltoratkaisu. 2025.  
