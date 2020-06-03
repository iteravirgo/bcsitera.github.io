# Smart Warehouse – Kasutusjuhend

Smart Warehouse lahendus võimaldab alljärgnevat:
- Paberivabad laotegevused
- Vigade tekkimise tõenäosuse vähenemine
- Lao protsesside kiirenemine
- Business Centrali ja Smart Warehouse omavaheline automaatne infovahetus
- Veoringide määramise funktsionaalsus
- Aluste ja kastide arvestus kauba vastuvõtul
- Aegumiskuupäeva määramine kaubale
- Komplekteerimise järjekorra seadistamise võimalus
- Aluste kleepsude ja aluste kleepsude saadetistele printimise võimalus
- Kauba eluea seadistamise võimalus
- Smart Warehouse programmist on laotöötajal võimalik näha kauba laoseisu koos aegumiskuupäevadega
- Paberivaba inventuur

## Sisukord
  - [Seadistused](#seadistused)
  - [Äpi seadistamine](#äpi-seadistamine)
  - [Kasutamine](#kasutamine)
  - [Ostutellimuse toimingud Business Centralis](#ostutellimuse-toimingud-business-centralis)
  - [Ostutellimuse toimingud Smart Warehouse programmis](#ostutellimuse-toimingud-smart-warehouse-programmis)
  - [Ostutellimuse kontrollimine Business Centralis ja arveks konteerimine](#ostutellimuse-kontrollimine-business-centralis-ja-arveks-konteerimine)
  - [Müügitellimuse toimingud Business Centralis](#müügitellimuse-toimingud-business-centralis)
  - [Müügitellimuse toimingud Smart Warehouse programmis](#müügitellimuse-toimingud-smart-warehouse-programmis)
  - [Müügitellimuse kontrollimine Business Centralis ja arveks konteerimine](#müügitellimuse-kontrollimine-business-centralis-ja-arveks-konteerimine)
  - [Aluse sisu kontrollimine](#aluse-sisu-kontrollimine)

<br/>

## Seadistused

Esmalt kontrolli, kas oled alla laadinud “ **Smart Warehouse** ” äpi. Kui see puudub võta ühendust BCS Iteraga. 

### Äpi seadistamine

Ava **Installeerimine**.
**Aktiveeri veebiteenus** ning seejärel vajuta **Edasi**.

![BCSetup](BCSetup.png)

Järgmiseks juhendatakse kasutajat leidma Smart Warehouse veebiteenus. Siin vajuta **Jah**.

![BCSetup2](BCSetup2.png)

Järgmiseks juhendatakse kasutajat leidma Smart Warehouse veebiteenus. Siin vajuta **Jah**.
Veebiteenuse leiad teenuste loendist ülevalt poolt.

![BCSetup3](BCSetup3.png)

Sulge antud leht!
Kopeeri endale tuleviku tarvis **Tahvli rakenduse URL** ja liigu **Edasi**.

![BCSetup4](BCSetup4.png)

|Väli|Kasutamine|
|-|-|
|Töökorralduste funktsionaalsuse kasutamine|Võimaldab vaadata töökorraldusi.|
|Laolähetuse funktsionaalsuse kasutamine|Võimaldab vaata ja luua laolähetusi.|
|Laotarne funktsionaalsuse kasutamine|Võimaldab kasutajal luua laotarnet.|
|Laotegevuste funktsionaalsuse kasutamine|Võimaldab vaadata ja luua laotegevusi.|

![BCSetup5](BCSetup5.png)

Kui kasutajal on vaja kõiki neid funktsionaalsusi kasutada aktiveeri need ning liigu Edasi.

![BCSetup6](BCSetup6.png)

Võimaldab automaatse Kaubakategooria valimist aktiveerimisel, mis saadab töökorralduse automaatselt tahvlisse. Soovi korral aktiveerige ning vajutage **Edasi**.
Kui aktiveerisite eelneva avaneb Business Centralisse seadistatud **Kaubakategooriate leht**:

![BCSetup7](BCSetup7.png)

Valige sealt endale soovitud kategooria ning pange linnuke kasti **Automaatne töökorraldus**. Sulgege leht. 
Järgmiseks valige Taara üld, toote konteeringu rühm:

![BCSetup8](BCSetup8.png)

Antud seadistus võimaldab taara ridade kaasamist Töökorralduse lõpetamisel. Vajadusel seadistage endale sobiv.
Minge **Edasi**.

|Väli|Kasutamine|
|-|-|
|Töötaja kontrollimise tõenäosuse %|Saab määrata kasutaja eksimuste tõenäosust tellimuste kokkupanemisel. Kasti numbrit kirjutades määratakse kasutajale nn supervisor, kes vastavalt seatud protsendile pisteliselt tema komplekteeritud kauba üle kontrollib|
|Kontrollitavate klientide valimine|Aktiveerimine võimaldab järgmist valikut muuta(Kontrollitavate klientide valimine käsitsi või filtreid kasutades).|
|Kontrollitavate klientide  valimine käsitsi või filtreid kasutades|Eelnev seadistus peab olema aktiveeritud, seejärel saab kasutaja otsustada, millise valiku järgi kontrollitavaid kliente valitakse.|

![BCSetup9](BCSetup9.png)

Minge **Edasi**.
Järgnevalt saab kasutaja aktiveerida endale soovitud automaattööd.

![BCSetup10](BCSetup10.png)

Vajutades **Edasi**, kuvatakse kõigi automaattööde kohta eraldi aknad algus/lõpu aegade ning sageduse seadistamiseks näiteks:

![BCSetup11](BCSetup11.png)

Liikuge **Edasi**.
Seadistuste viimases aknas on võimalik aktiveerida õiguste uuendamist, avada seadete akent ning tööjärjekorra kandeid. Kui soovitud read on aktiveeritud **Lõpetage** installeerimine.

![BCSetup12](BCSetup12.png)

Järgnevalt lehelt on võimalik endale Smart Warehouse rakendus alla laadida:

![BCSetup13](BCSetup13.png)

Pakkige fail lahti ning avage fail **SmartWarehouse Setup.exe**:

![SWSetup](SWSetup.png)

|Väli|Kasutamine|
|-|-|
|URL|Sinna kopeeri eelnevalt kopeeritud link.|
|Autentimine|Windows/Nav Kasutaja|
|Kasutaja nimi|Vastavalt eelnevalt tehtud valikule, kas Window või Business Central Kasutaja|
|Parool|Vastavalt eelnevalt tehtud valikule kas Window või Business Central parool|

![SWSetup1](SWSetup1.png)

Seejärel testi ühendust:

![SWSetup2](SWSetup2.png)

Kui kõik õnnestus annab server vastuse:

![SWSetup3](SWSetup3.png)

Mine tagasi **Business Centralisse**.
Seadista **Mõõtühikud**. Nendele mõõtühikutele, mida on vaja kasutada Smart Warehouse programmis lisa linnuke kasti **Kaaluühik**.

![BCUnitSetup](BCUnitSetup.png)

Järgmiseks mine lehele **Laotöötajad**.
Lisa sinna kõik töötajad, kes hakkavad programmi kasutama ning juurde vali ladu ehk **Asukoha tähis**. Kasti **Vaikimisi** lisa linnukesed nende töötajate asukohtadele, mis mida soovid määrata töötajale vaikimisi. 

![BCEmployeeSetup](BCEmployeeSetup.png)

## Kasutamine

### Ostutellimuse toimingud Business Centralis

Avage ostutellimused ning looge uus ostutellimus.
Kohustuslikud väljad **Hankija nimi**, **Hankija arve nr**, **Auto nr.**

![BCPurchOrder](BCPurchOrder.png)

Ridadele lisa kaup, koos **Asukoha tähise** ja **Kogusega**.

![BCPurchOrder2](BCPurchOrder2.png)

Eelnev info on vaja lisada, sest seda kuvatakse laotöötajale Smart Warehouse programmis.
Järgnevalt vajuta **Toimingud** -> **Vabasta** -> **Täida algselt tellitud kogus**.
Toimingu järgselt täitus ridadel **Algselt tellitud kogus**.

![BCPurchOrder3](BCPurchOrder3.png)

Vabasta tellimus!
Viimaks vajuta **Toimingud** -> **Ladu** -> **Loo Laotarne**.

![BCPurchOrderLaotarne](BCPurchOrderLaotarne.png)

### Ostutellimuse toimingud Smart Warehouse programmis

Ava **SmartWarehouse.exe.**

![SWProgramFind](SWProgramFind.png)

Logi sisse eelnevalt seadistatud Kasutajanime ja Parooliga:

![SWLoging](SWLoging.png)

Seejärel avaneb tegevuste loend:

![SWMenu](SWMenu.png)

Ostutellimuse puhul lõime Business Centralis **Laotarne**, seega avame **Laotarne** lehe.
Alljärgnev valik annab võimaluse laotarne leidmiseks **Kuupäeva**, **Hankija**, **Auto**, **Kauba järgi**.

![SWLaotarneMenüü](SWLaotarneMenüü.png)

Valides Auto, kuvatakse laotöötajale kõik ostutellimused, millel oli auto väli täidetud:

![SWLaotarneAuto](SWLaotarneAuto.png)

Vajuta **auto nr** väljal ning töötajale avaneb ostutellimuse read. 

![SWLaotarneList](SWLaotarneList.png)

|Väli|Kasutamine|
|-|-|
|Kood|Business Centralist tulev kauba kood. Pole muudetav.|
|LTAR000015 JB-007|Laotarne peal olevad tooted. Pole muudetav|
|Tellitud kogus|Ostutellimusel märgitud tellitud kogus. Pole muudetav|
|Ühik|Kaubale määratud ühik. Pole muudetav.|
|Kogus|Vajutades väljale, on võimalik sisestada tegelik kogus.|
|Praagi %|Vajutades väljale, saab määrata praagi %.|
|Partii|Kui tootele on määratud partii, saab selle sisestada.|
|Alus|Vaikimisi Business Centralist. Pole muudetav.|
|Valmis|Kui rida on kontrollitud vajuta Valmis ja toote kontrollimine on automaatselt kinnitatud. |

Osade toodete puhul on vaja täita väljad :

![SWLaotarneList2](SWLaotarneList2.png)

|Väli|Kasutamine|
|-|-|
|Aluse KG|Kui Business Centralis seadistatud tuleb automaatselt, aga saab muuta.|
|Kast KG|Kui Business Centralis seadistatud tuleb automaatselt, aga saab muuta.|
|Kaste|Kui Business Centralis seadistatud tuleb automaatselt, aga saab muuta.|
|Bruto KG|Kui Business Centralis seadistatud tuleb automaatselt, aga saab muuta.|
|Neto KG|Kui Business Centralis seadistatud tuleb automaatselt, aga saab muuta.|
|Praagi %|Vajutades väljale, saab määrata praagi %.|
|Partii|Siin lehel ei saa määrata, määratakse eelmisel lehel.|
|Valmis|Kui kõik vajalik info on seadistatud vajuta Valmis kasti linnuke.|

Vajutades nupule **Trüki silt**, on võimalik välja printida valitud tootele aluse silti.

![SWSilt](SWSilt.png)

Kui tooted on laos kontrollitud vajuta nupule **Tagasi**.

![SWLaotarneList3](SWLaotarneList3.png)

Seejärel saab valida, kas kinnitada rida, kinnitaja ja ava ladustamise või mitte kinnitada.

![SWLaotarneKinnitus](SWLaotarneKinnitus.png)

Vajutades **Jah, ava ladustamised** avaneb leht ladustusleht, kus saab sisestada kauba soovitud asukoha:

![SWLadustamine](SWLadustamine.png)

Kui soovitud asukoht on sisestatud ja kaup paigutatud tee linnukesed kasti **Valmis**. 
Ladustamine on registreeritud ning võid minna tagasi algusesse.

### Ostutellimuse kontrollimine Business Centralis ja arveks konteerimine

Ava eelnevate tegevuste jaoks loodud ostutellimus.
Tellimuse ridadel vajutades **Rida** -> **Kaubajälgimise read**, kuvatakse detailne info kauba kohta näiteks Smart Warehouses sisestatud **Kehtivuse lõpp**:

![BCKaubajälgimine](BCKaubajälgimine.png)

Lisaks saab kaubale juurde määrata:

![BCKaubajälgimine2](BCKaubajälgimine2.png)

Tellimuse ridadel vajutades **Rida** -> **Kaalumise read** kuvatakse kasutajale **Konteeritud lao kaalumise ridu**:

![BCKaalumisread](BCKaalumisread.png)

Kui kõik soovitud info on tellimusel olemas **Konteeri** dokument.

### Müügitellimuse toimingud Business Centralis

Loo uus müügitellimus.
Müügitellimuse osas **Üldine** saad sisestada laole info väljale **Töö kirjeldus**:

![BCOstutell](BCOstutell.png)

Osas SmartWarehouse saad sisestada järgneva info:

|Väli|Kasutamine|
|-|-|
|Noppimise seisund|Noppimine/Valmis|
|Veoring|Eelseadistatud veoringi valik.|
|Veoringi tarne algus|Veoringi tarne algusaeg.|
|Veoringi tarne lõpp|Veoringi tarne lõppaeg.|
|Järjekord veoringis|Mitmes on tellimus valitud veoringil.|
|Lähetuskuupäev|Lähetuskuupäeva määrang|
|Töörühm|Laotöötajaid on võimalik klientidega siduda|

![BCOstutell2](BCOstutell2.png)

Ridadel saad sisestada lisainformatsiooni komplekteerijale:

![BCOstutell3](BCOstutell3.png)

Kui müügitellimusel on kõik vajalikud read lisatud **Vabasta** dokument.

Seejärel ava **Tööjärjekorra kanded**.
Käivita automaatöö : 
- Käivitatava objekti ID - 70466728
- Parameetrijada: CREATESALESSHIPMENTS

Antud automaatöö loob lao lähetuse ning varude noppimise, mille read ilmuvad seejärel kättesaadavaks Smart Warehouse programmis.

### Müügitellimuse toimingud Smart Warehouse programmis

Ava **Smart Warehouse** programm.

Programmis ava leht **Laosisesed tegevused**.

![SWMenüü_laotegevused](SWMenüü_laotegevused.png)

Seejärel ava leht **Noppimine**.

![SWNoppimine](SWNoppimine.png)

Avaneb noppeleht:

![SWNoppeleht](SWNoppeleht.png)

Kus kuvatakse infot müügitellimuse väljalt **Töö Kirjeldus**, **Veoringi**, **Laolähetuse numbrit** ning laotöötajale olulist info kauba kohta, näiteks **Asukoht**, **Kogus**.

Lisaks on võimalik alusele välja printida silti. Seal kuvatakse tellimuse saaja aadresse, tellimuse numbrit, kauba saatjat, veoringi, lähetuse ja- tarnekuupäeva.

Kui nope on valmis pane linnuke kasti **Valmis**.
Seejärel avaneb leht, mis juhendab töötajat kuhu tuleb suunata nopitud kaup. Lisaks saab vajadusel sisestada **Aluse KG**, **Kasti KG**, **Kastide arvu** ning selle järgi arvutatakse välja **Bruto KG** ja **Neto KG**.

![SWNoppeleht2](SWNoppeleht2.png)

Pane linnuke kasti **Valmis**.
Nope on seejärel registreeritud ja liigu tagasi **Algusesse**.
Vajuta nupule **Laolähetus**.

![SWLähetus](SWLähetus.png)

Avaneb nopitud laolähetuste loend.

![SWLähetus2](SWLähetus2.png)

Vajutades Autode määramine, saad täpsustada kaupa vedava auto numbri. 
Vajuta laolähetuse reale ning kinnita veelkord kogused ning seejärel saad dokumendi märkida **Valmis**.

![SWLähetus3](SWLähetus3.png)

Smart Warehouse programmi tegevused on laotöötaja poolt lõpetatud ning võib minna tagasi **Algusesse**.

### Müügitellimuse kontrollimine Business Centralis ja arveks konteerimine

Ava Business Central ja kontrolli muutuseid müügitellimusel. Ridadel on kogused uuendatud.

![BCMüügitelliKontroll](BCMüügitelliKontroll.png)

Seejärel saab arve ära konteerida.

### Aluse sisu kontrollimine

Ava Smart warehouse programmist leht **Kaubakontroll**.
Kliki real kood ning sisesta kauba number, mille aluse sisu soovid kontrollida ning seejärel vajuta klaviatuuril **Enter**. Avaneb kauba aluse sisu info:

![SWAlus1](SWAlus1.png)

Kui kaubale on määratud partii ja säilivus, siis vajutades kauba reale kuvatakse seda infot.

![SWAlus2](SWAlus2.png)

Kui soovitud info on üle kontrollitud vajuta nuppu **Tühjenda**.

Lisainformatsiooni saamiseks palun võta ühendust BCS Itera AS:
[https://www.itera.ee](https://www.itera.ee)







