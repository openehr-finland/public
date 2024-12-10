# openEHR Finlandin dokumentaatio ja tukimateriaalit (TRIAL)

> **STATUS:** TRIAL

OpenEHR Finland on aloittanut toimintansa kesäkuussa 2022 ja se toimii HL7 Finlandin alatyöryhmänä. Toiminnan tarkoituksena on edistää semanttista yhteentoimivuutta, tiedon hyödynnettävyyttä, yhteistyöstä sekä tietämyksen kehittymistä openEHR:stä. OpenEHR Finlandin manifestin voit lukea [täältä](https://www.hl7.fi/openehr-alatyoryhma/manifesti-2022-openehr-finland/). 

Tämän osion tarkoituksena on koota yhteen erilaiset ohjeet, hyvät käytännöt sekä soveltamisoppaat liittyen openEHR mallinnustyöhön Suomessa.
Materiaalien tarkoituksena on ohjata toteutettavaa mallinnus työtä sekä openEHR:n hyödyntämistä suomessa yhtenäiseen suuntaan.

## Hallintamalli ja hyödynnettävät työkalut

OpenEHR Finlandin toiminnassa sovelletaan HL7 Finlandin määrittämiä hallintakäytäntöjä tuotosten kommentoimisessa sekä hyväksynnässä ([HL7 Finland Lausuntokierrosten ja äänestysten säännöt v1.0](https://www.hl7.fi/wp-content/uploads/HL7_Finland_lausunto_ja_%C3%A4%C3%A4nestyskierrosten_s%C3%A4%C3%A4nn%C3%B6t_v100_20140512.doc)). Poikkeuksena yhdistyksen säännönmukaisiin käytäntöihin openEHR Finlandin tuotokset katselmoidaan ja kommentoidaa ennen varsinaisia kommentointi ja äänestyskierroksia Suomen openEHR yhteisön toimesta, jotta mallinnosten kliininen valididius pystytään varmistamaan ja informoimaan käsittelyyn.

### Etenemiskaavio
| Vaihe | Kuvaus | Kesto |
| --- | --- | --- |
| Työstäminen | Mallinnus tai määrittelytyön toteutus | Tarpeen mukainen aika |
| Kliininen validointi | Tuotos käydään läpi tarkoituksen mukaisten sote-ammattihenkilöiden kanssa, jotta tuotoksen kliininen pätevyys voidaan varmistaa | 1-2vko |
| Kommentointi | Kommentointi / Lausuntokierroksen toteutus yhdistyksen sääntöjen mukaisesti | 4vko |
| Standardiluonnoksen alustava äänestys | Ensimmäisen äänestyskierroksen toteutus yhdistyksen sääntöjen mukaisesti | 2vko |
| Korjaustarpeista äänestäminen (tarvittaessa) | Edellisessä vaiheessa esiin tulleista korjaustarpeista sekä muutosehdotuksista äänestäminen yhdistyksen sääntöjen mukaisesti | 1vko |
| Standardin hyväksyntä HL7 hallituksessa | Hyväksytty tuotos vahvistetaan hallituksen kokouksessa | Äänestystä seuraava hallituksen kokous |

### Mallinnustyö ja käytettävät työkalut

openEHR Finlandin mallinnustyössä käytetään Archetype Designeria arkkityyppien ja templaattien kehittämiseen ja muokkaamiseen, ja GitHubia niiden (sekä muiden yhteisten resurssien) säilytykseen, ylläpitoon ja hallinnoimiseen. Kaikkien mallintajien tulee luoda omat  Archetype Designer ja GitHub-tilit, jotka liitetään openEHR Finlandin etätietovarastoihin, niin että kaikilla on pääsy samoihin tietomalleihin ja tiedostoihin.


| Työkalu | Kuvaus | Ohjeet ja lisätiedot |
| --- | --- | --- |
| GitHub | GitHubia käytetään on openEHR Finlandin tuotosten sekä dokumentaation hallintaan. GitHubissa on käytössä kolme repositoriota; openehr-finland: Kaikki muokkauksessa olevat templaatit ja niissä käytetyt arkkityypit sekä muu tekninen aineisto, documentation: Käytetään erilaisen dokumentaation, hyvien käytäntöjen ja aineistojen sekä soveltamisoppaiden tuottamiseen, public: käytetään valmiiden aineistojen julkaisuun sekä kommentointikierrosten toteutusta varten | - https://github.com/openehr-finland<br/>- [Rekisteröitymisohje](https://github.com/openehr-finland/public/blob/main/documentation/guides/openEHR-Finland_GitHub_ohje_v1.pdf) |
| Archetype Designer | Archetype Designer on Betterin kehittämä arkkityyppien ja templaattien suunnittelu- ja muokkaustyökalu. openEHR International ylläpitää siitä ilmaista kopiota, mikä on mallinnusyhteisön yleisessä käytössä. Lista muista vastaavista työkaluista löytyy osoitteesta: https://openehr.org/products_tools/modelling_tools/. | - https://tools.openehr.org/designer/#/<br/> - [Rekisteröitymisohje](https://github.com/openehr-finland/public/blob/main/documentation/guides/openEHR-Finland_AD_ohje_v1.pdf)<br/> - [Ohje Archetype Designerin ja GitHubin linkittämisestä](https://github.com/openehr-finland/public/blob/main/documentation/guides/openEHR-Finland_AD-GitHub-linkitys_ohje_v1.pdf) |
| Clinical Knowledge Manager (CKM) | Yksi openEHR-mallinnuksen tärkeimmistä työkaluista on Clinical Knowledge Manager (CKM) - eli Ocean Health Systemsin ylläpitämä verkkopohjainen yhteistyötila ja tietomalliarkisto. Sitä käytetään kansainvälisten arkkityyppien kehittämiseen, ylläpitoon ja hallinnointiin. CKM:ään voi rekisteröityä ilmaiseksi kuka tahansa openEHR-tietomalleista kiinnostunut henkilö. Rekisteröityneet käyttäjät voivat osallistua arkkityyppien kehittämiseen ja julkaisuun arvioijina, kääntäjinä tai Editoreina. Osallistuminen CKM:ään tehdään vapaaehtoiselta pohjalta, ja kaikki CKM:n tietomallit ovat avointa lähdekoodia ja vapaasti käytettävissä Creative Commons-lisenssin alla.<br/>CKM mahdollistaa kansainvälisten arkkityyppien avoimen arvioinnin ja kommentoinnin asiantuntijoiden johdolla ennen niiden virallista julkaisua. Sen kautta voidaan lähettää kutsuja arviointikierroksille, koota ja järjestää arviointikierroksilta saatua palautetta, sekä vastata kaikkiin kommentteihin ja ehdotuksiin julkisesti.<br/>Myös kaikki julkaistujen arkkityyppien muutokset tehdään CKM:n avulla ja ovat avoimesti nähtävissä arkkityyppihistoriatoiminnon kautta. Muutospyyntöjä voivat tehdä kaikki CKM:n rekisteröityneet käyttäjät, ja Clinical Knowledge Administratorit (CKA), jotka vastaavat CKM:n ylläpidosta ja hallinnoimisesta, päättävät toteutetaanko vai hylätäänkö ne. Kaikki muutospyynnöt ja CKA:n kommentit näkyvät myös muille rekisteröityneille käyttäjille. | - https://ckm.openehr.org/ckm/<br/>- [CKM yleisohje](https://github.com/openehr-finland/documentation/blob/main/guides/CKM-yleisohjeet_v1.pdf)<br/>- [Suomennosten kommentointi CKM:ssä](https://github.com/openehr-finland/public/blob/main/documentation/guides/openEHR-CKM-suomennosten-kommentointi.pdf) |
| X-Mind | X-Mind on ajatuskarttojen laadintaan käytettävä ilmainen ohjelmisto, jota hyödynnetään tietomallien jäsentämisen tukena mallinnustyön alkuvaiheessa. Työkalulla on muunmuassa helppo toteuttaa CGEM jäsennyksiä, joiden avulla käyttötapaus voidaan purkaa openEHR templaattien ja arkkityyppien hahmottamiseksi. | - https://xmind.app/ |

# openEHR Finland documentation

OpenEHR Finland has started its operations in June 2022 and it works as a sub-working group of HL7 Finland. The purpose of the activity is to promote semantic interoperability, the usability of information, cooperation and the development of knowledge about openEHR. You can read OpenEHR Finland's manifesto [here](https://github.com/openehr-finland/public/blob/main/documentation/manifest.md).

The purpose of this repository is to bring together various instructions, good practices and implementation guides related to the work of openEHR Finland. The purpose of the materials is to guide the modeling work to be implemented and the utilization of openEHR in Finland in a unified direction.

