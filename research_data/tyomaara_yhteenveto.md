# Agentillisen toiminnan työmäärä, suoritusaika ja käytetyt mallit

Tämä dokumentti sisältää yhteenvedon ja erittelyn `research_data`-kokonaisuuden tuottamiseen vaadittujen agentillisten toimintojen työmäärästä, suoritusajoista sekä käytetyistä tekoälymalleista ja -ympäristöistä.

> [!IMPORTANT]
> **HUOMIO MITTAUSPERUSTEESTA:**  
> Tässä dokumentissa ilmoitetut ajat kuvaavat **ainoastaan tekoälyn asiantuntija-agenttien aktiivista laskenta- ja prosessointiaikaa** (tekoälyagentillinen suoritusaika / computational test-time and inference compute).  
> Tutkimusta johtaneen ihmisen (ohjelmistoarkkitehti, lakiasiantuntijat) käyttämää aktiivista työaikaa – kuten kehotemuotoilua, vuorovaikutteista ohjausta, väliarviointeja ja juridista laadunvarmistusta – **ei mitattu tässä tutkimuksessa**.

---

## 1. Yhteenveto ja käytetty tekoälykokoonpano

Tutkimusprosessi toteutettiin kaksivaiheisena asiantuntijatyönkulkuna suoraan kehittyneissä generatiivisen tekoälyn tutkimus- ja asiantuntijaympäristöissä **ilman ohjelmallista sovellusrajapintaa (API)**:

1. **Vaihe 1: Primäärinen normilouhinta ja sisällöntuotanto (ChatGPT Deep Research / 5.6 Sol):**
   * **Ympäristö:** ChatGPT Deep Research -tutkimusagenttitila (vuorovaikutteinen moniagenttinen tutkimusympäristö).
   * **Taustamalli:** **5.6 Sol**
   * **Päättelytaso (Reasoning Effort):** **High / Max** (laajennettu test-time compute / syvä ketjupäättely, joka ohittaa Instant-oletusasetuksen).
   * **Tehtävä:** Autonominen säädösten (Finlex 3.9.2026 asti), oikeuskäytännön (KKO, KHO) ja viranomaisohjeiden (OPH, THL) louhinta, analyysi ja lukukohtainen raportointi.
   * **Ajoaika:** **~5 tuntia 59 minuuttia 19 sekuntia** (21 559 sekuntia).
   * **Tuotos:** 24 pääkappaletta, 10 malliasiakirjaa, laajuus yhteensä n. 150 000 sanaa.

2. **Vaihe 2: Datan järjestäminen, toimituksellinen työ ja akateeminen arviointi (Gemini 3.8 / Antigravity):**
   * **Ympäristö:** Antigravity-asiantuntijatyötila.
   * **Malli:** **Gemini 3.8**
   * **Tehtävä:** Lukujen vastaanotto, tiedostorakenteen ja informaatioarkkitehtuurin jäsennys, toimituksellinen laadunvarmistus, kriittinen akateeminen vertaisarviointisimulaatio (FinJeHeW-kriteerit) sekä IMRaD-tieteellisen käsikirjoituksen ja liiteaineistojen koostaminen.
   * **Aktiivinen laskenta-aika (lokitettu suoritusaika):** **~35 minuuttia 20 sekuntia** (2 120 sekuntia).

* **AI-agenttien kokonaissuoritusaika:** **6 tuntia 34 minuuttia 39 sekuntia** (yhteensä 23 679 sekuntia).

---

## 2. Erittely vaiheittain ja malleittain

| Vaihe / Tehtävä | Suoritusympäristö ja Malli | Minuutit | Sekunnit | Kesto sekunteina | Kesto (selkokielinen) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Raportin jatko** | ChatGPT Deep Research (5.6 Sol, Max effort) | 67 | 34 | 4 054 | 1 h 07 min 34 s |
| *(Nimeämätön vaihe)* | ChatGPT Deep Research (5.6 Sol, Max effort) | 1 | 35 | 95 | 1 min 35 s |
| **Suunnitelma** | ChatGPT Deep Research (5.6 Sol, Max effort) | 4 | 5 | 245 | 4 min 05 s |
| **Luku 3** | ChatGPT Deep Research (5.6 Sol, Max effort) | 39 | 57 | 2 397 | 39 min 57 s |
| **Luku 4** | ChatGPT Deep Research (5.6 Sol, Max effort) | 52 | 40 | 3 160 | 52 min 40 s |
| **Luku 5** | ChatGPT Deep Research (5.6 Sol, Max effort) | 29 | 27 | 1 767 | 29 min 27 s |
| **Luku 6** | ChatGPT Deep Research (5.6 Sol, Max effort) | 26 | 28 | 1 588 | 26 min 28 s |
| **Luku 7** | ChatGPT Deep Research (5.6 Sol, Max effort) | 27 | 53 | 1 673 | 27 min 53 s |
| **Luku 8** | ChatGPT Deep Research (5.6 Sol, Max effort) | 44 | 18 | 2 658 | 44 min 18 s |
| **Luku 9** | ChatGPT Deep Research (5.6 Sol, Max effort) | 15 | 2 | 902 | 15 min 02 s |
| **Luku 10** | ChatGPT Deep Research (5.6 Sol, Max effort) | 23 | 25 | 1 405 | 23 min 25 s |
| **Luku 11** | ChatGPT Deep Research (5.6 Sol, Max effort) | 13 | 53 | 833 | 13 min 53 s |
| **Luku 12** | ChatGPT Deep Research (5.6 Sol, Max effort) | 10 | 11 | 611 | 10 min 11 s |
| **Luku 13** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 23 | 23 | 23 s |
| **Luku 14** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 27 | 27 | 27 s |
| **Luku 15** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 29 | 29 | 29 s |
| **Luku 16** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 15 | 15 | 15 s |
| **Luku 17** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 17 | 17 | 17 s |
| **Liite A** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 20 | 20 | 20 s |
| **Liite B** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 20 | 20 | 20 s |
| **Liite C** | ChatGPT Deep Research (5.6 Sol, Max effort) | 0 | 20 | 20 | 20 s |
| **Antigravity: executive, työtila ja arviointi** | Gemini 3.8 (Antigravity) | 15 | 20 | 920 | 15 min 20 s |
| **Antigravity: lukujen vastaanotto ja järjestely** | Gemini 3.8 (Antigravity) | 20 | 0 | 1 200 | 20 min 00 s |
| **YHTEENSÄ** | **Kaksivaiheinen työnkulku (5.6 Sol + Gemini 3.8)** | **389** | **639** | **23 679** | **6 h 34 min 39 s** |

---

## 3. Huomioita työmäärän ja suorituskyvyn jakautumisesta

1. **Työläimmät osuudet (ChatGPT Deep Research / 5.6 Sol):**
   - *Raportin jatko* (1 h 7 min 34 s)
   - *Luku 4: Toimivaltaperiaatteet ja normihierarkia* (52 min 40 s)
   - *Luku 8: Oikeuskäytäntö ja soveltamiskäytäntö* (44 min 18 s)
   - *Luku 3: Käsitteet ja oikeuslähteet* (39 min 57 s)
   - *Luku 5 & 7: Vastuunjako ja sosiaalihuolto* (~28–29 min)
   *Perustelu:* Nämä osiot vaativat laajinta itsenäistä verkkohakua Finlex-tietokantaan, ristiintaulukointia useiden ministeriöiden hallinnonalojen välillä sekä useita sisäisiä iteraatioita ristiriitaisten normien yhteensovittamiseksi.

2. **Kevyet osiot:**
   - Luvut 13–17 sekä liitteet A–C veivät kukin vain 15–29 sekuntia, sillä kyse oli aiemmin muodostettujen periaatteiden tiivistämisestä tarkistuslistoiksi ja valmiiksi jäsennellyiksi yhteenvedoiksi.

3. **Toimituksellinen työ ja akateeminen arviointi (Gemini 3.8):**
   - Antigravity-työtilassa Gemini 3.8:lla suoritettu lukujen vastaanotto, tiedostojen strukturointi, taulukoiden luominen, FinJeHeW-vaatimusten mukainen vertaisarviointi ja akateemisen käsikirjoituksen koostaminen veivät **35 minuuttia ja 20 sekuntia**.
   - Tämä mitattu suoritus kertyi kahdesta aktiivisesta istunnosta (ensimmäinen yhtenäinen 222 askeleen tiedostokäsittelyjakso ja sitä seurannut tieteellisten tarkennusten ja laadunvarmistusten ajo).
   - Mallin korkea kontekstikapasiteetti mahdollisti 150 000 sanan normiaineiston nopean käsittelyn ilman laadun heikkenemistä.
