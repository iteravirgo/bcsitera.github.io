# Kuluaruanded
Kuluaruannete lahendus BC-s võimaldab järgmist:

- Kulu- ja lähetusaruannete haldust (sh kinnitusringid ja päevarahad)
- Kuludokumentide haldust (erinevate valuutadega)
- Kuludokumentide digitaalset arhiivi
- Ühendust digiteerimise partneriga <a href="https://costpocket.com/et" target="_blank">CostPocket.com</a>

## Seadistamine
Lahenduse kasutamiseks tuleb esmalt avada **Kuluaruannete seadistus** ning täita järgmised väljad:

|Väli|Selgitus|
|---|---| 
| Kuluaruannete numbrid | Määramaks kuluaruannete numbriseeria. Väärtuse saab valida **Numbriseeriate loendist**.|
| Kuludokumentide numbrid | Määramaks kuludokumentide numbriseeria. Väärtuse saab valida **Numbriseeriate loendist**.|
| Hankija registreerimisnumbri väli | Lahendus kasutab Hankija registreerimisnumbrit tuvastamaks kulu hankijat. Kuivõrd erinevate maade lokalisatsioonid kasutavad selleks erinevaid väljasid, siis oleme teinud selle väärtuse valitavaks. **Valik on soovitatav, kuid mitte kohustuslik**. Eesti lokalisatsiooni äppidena kasutamise korral peaks valik olema 24007770|
| Päevarahade vaikimisi konto nr. | Määramaks vaike PR kontot, kuhu konteeritakse Päevarahade summa. Väärtuse saab valida **PR Kontode loendist**.|

Kõik kuludokumendid konteeritakse läbi peažurnaali ning kasutaja saab selleks **määrata kasutatava Žurnaalimalli ning Žurnaali töölehe**. Lahenduse installeerimise käigus luuakse selleks Peažurnaali tööleht nimega APP-EXPREP.

Kasutamaks digiteerimise partneri **CostPocket** pakutavat funktsionaalsust, tuleb algatada ühenduse loomine nupust **Registreerimine**. CostPocketis registreerimise aknas Sisestatud kasutajast saab lahenduse peakasutaja, kellele CostPocket saadab e-postiga juhised, kust saada ning kuidas kasutada CostPocketi äppi. Peale edukat registreerimist luuakse ühendus CostPocketiga. (Registreerimist tuleb teha vaid korra).    

**Automaatseks kuluaruannete/dokumentide importimiseks** kasutatakse tööjärjekorra kannet, mida saab vaadata/luua Toimingud sektsioonis asuva **nupuga "Tööjärjekorra kanded"**. Kui tööjärjekorra kanne ei ole loodud, siis nimetatud nupule vajutades see luuakse. *Tööjärjekorra kannet kuludokumentide importimiseks on vaja ainult juhul, kui aruandeta dokumendid on lubatud.*    

Ettemääratud kulu liikidele saab kasutaja vastendada vaike kulukontod. Seda saab seadistada lehel **Kulu liigid**. Dokumentide importimisel CostPocketist, kui hankija tuvastatakse (Reg.nr või VAT nr. alusel), määrab süsteem kuludokumentidele vaike kulukontod vastavalt kuludokumendi kulu liigile.

**Kuluaruande kinnitamine** ning selle seadistamine on analoogne Ostuarve kinnitusringile (vt <a href="https://docs.microsoft.com/en-us/dynamics365/business-central/walkthrough-setting-up-and-using-a-purchase-approval-workflow/" target="_blank">Setting Up and Using a Purchase Approval Workflow</a>.)
Lehel Töövood tuleb vajutada nupule "Uus töövoog mallist" ning valida **Expense Report Approval Workflow**. 
Kui töövoog on määratud Lubatud staatusesse, siis õnnestub kuluaruande konteerimine ainult peale kinnitusringi läbimist (staatuseks saab Vabastatud).    

Teavitamaks raamatupidajat värskelt imporditud kuluaruannetest, tuleks kasutada töövoo malli **Expense Report New Entry Notification Workflow**.    

**Lahendus on mõeldud kasutamiseks järgmise loogika kohaselt:**  
Kasutaja(d) kasutavad igapäevaselt/iganädalaselt CostPocketi äppi, pildistades kuludokumente ning lisades neid kuluaruandele. Raamatupidaja toimetab BC-s CostPocketist tulnud kuluaruannete ning seotud kuludokumentidega (kontrollib konteeringud, saadab kinnitusringile ning konteerib).
*Erandjuhtudel, kui ei plaanita kuluaruandeid kasutada, võib märkida **Luba aruandeta dokumente**, mis muudab võimalikuks aruandeta kuludokumentide käsitlemise.*

## Kasutamine
### Kuluaruanded

**Käsitsi** kuluaruanne luuakse üldjuhul peale käsitsi üksikute kuludokumentide loomist. Kasutaja saab lisada dokumente aruandele nupust **Lisa aruandele dokumendid**.

Kuluaruanded *(staatusega Valmis)* imporditakse CostPocketist, kui kasutaja vajutab nuppu **Too aruanded CostPocketist** või kui käivitub vastav tööjärjekorra töö *(Käivitatava objekti liik on Aruanne ning ID 24008101)*.  Koos kuluaruandega imporditakse BC-sse ka kõik vastava kuluaruandega seotud kuludokumendid.    

Kuluaruande kaardil näeb kasutaja kõikide seotud dokumentide summat kohalikus valuutas väljal Summa KM-ta (KV).    

Kasutaja saab muuta välja **Esitaja nr.** väärtus, valides Töötajate loendist teise väärtuse. Väärtuse valimisel küsib süsteem kinnitust, kirjutamaks üle kõikide seotud kuludokumentide esitajad.    

Konteerimaks kuluaruannet peab kasutaja määrama kuupäeva väljale **Konteerimiskuupäev**, mis määratakse ka kõikidele seotud dokumentidele.    

Kasutaja saab kuluaruandel muuta **Päevarahade summat** ning konteerimiseks kasutatavat Päevarahade konto numbrit.    

Kasutaja saab avada seotud kuludokumentide loetelu, vajutades väljal **Dokumentide arv** olevale numbrile.    

Kuluaruandele määratavad **Dimensioonid** kanduvad edasi ka kõikidele seotud dokumentidele (kui kasutaja vastava valiku kinnitab). Esitajast töötaja küljes olevad vaikedimensioonid lisatakse samuti automaatselt kõikidele seotud dokumentidele.    

**Kinnitamise protsess** vastab tavapärasele BC kinnitamise loogikale (vt <a href="https://docs.microsoft.com/en-US/dynamics365/business-central/across-how-use-approval-workflows/" target="_blank">Use Approval Workflows</a>).    

**Konteeri** tähendab, et nii päevarahad, kui kõik kuluaruandega seotud kuludokumendid konteeritakse ühe korraga koos. *Dokumendid konteeritakse kõik eraldi.*  

Konteeritud kuluaruanded leiab **Konteeritud kuluaruanded** arhiivist.

### Kuludokumendid

Käsitsi kuludokumendi loomine on võimalik ning sarnaneb ostuarve loomisele.

**Hankija ning Esitaja peab olema** kuludokumendil määratud.  Kuludokumentide importimisel CostPocketist otsitakse Hankija reg. nr. ja/või Hankija KM reg. nr. väärtuse alusel Hankijate registrist hankijat. Analoogselt otsitakse töötajate registrist (välja Ettevõtte e-post alusel) kuludokumendi esitajat, väljal Esitaja e-post oleva väärtuse alusel.
Kasutaja võib luua mitme reaga arve, kasutades erinevaid konteeringurühmasid (KM korrektseks haldamiseks).    

**Dimensioonid** saab lisada nii päisele kui ridadele (analoogselt ostuarvetele).    

Kõiki enamlevinuid pildifaile (nt .png .jpg .jpeg) saab lisada **pildimanustena**. Lisaks saab dokumendimanustena lisada kõiksugu faile (nt digiallkirjastatud dokumente).   

Kuludokumendi **Makse tüüp** saab olla kas Makstud eraisikuna või Makstud e/v vahenditest, sõltuvalt tehingu finantseerijast.    

Tehingu kurssi saab muuta läbi **Valuutakordaja** välja.    

Kasutaja saab töödelda kuludokumente nii läbi kaardi, kui kuludokumentide loendi *(peamiselt määramaks Hankijat/Esitajat/Kulukontot)*.
Kui kuludokumendi päises valitakse Kulukonto, siis kasutajalt küsitakse kinnitust Kas soovite uuendada ridu, mis määrab kõikidele dokumendi ridadele uue kulukonto.    

Kasutaja võib kontrollida dokumendi konteerimise tulemust nupust **Konteeringu eelvaade**.  
Lahendus teeb Hankija alla hankijaandmiku kanded ning Töötaja alla töötajaandmiku kanded *(kui esitaja on tasunud kuludokumendi eest).*

Dokumendid konteeritakse üldjuhul Kuluaruandelt.
*Erandjuhul, kui on lubatud aruandeta kuludokumendid, saab CostPocketist importida üksikuid kuludokumente nupust **Too dokumendid CostPocketist** ning sellisel juhul saab üksikut kuludokumenti ka konteerida.*

Konteeritud kuludokumendid leiab **Konteeritud kuludokumendid** arhiivist.    

Ekslikult konteeritud kuludokumendi tühistamiseks tuleb valida vastav pearaamatu kanne ning vajutada nupule **Pööra tehing ümber...**, mille tulemusena loob süsteem vastupidise kande (algse kandega tehakse identne kanne ainult vastupidise märgiga Summa veerus), jättes samaks nii dokumendi numbri kui konteerimiskuupäeva. Peale kande ümberpööramist saab kasutaja luua peažurnaalist õige kande.

---

Täpsema info saamiseks, palun võtke ühendust BCS Itera AS-ga:
<a href="https://www.itera.ee/" target="_blank">www.itera.ee</a>
