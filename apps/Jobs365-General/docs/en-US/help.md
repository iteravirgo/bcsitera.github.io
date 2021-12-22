# Jobs365 - General
Additions to Job module include follwoing functionalities:

  - [Archiving Jobs.](#archiving-jobs)
  - [Send Job budget to GL budget](#send-job-budget-to-gl-budget)
  - [Batch changing discount or markup on Job Planning Lines](#batch-changing-discount-or-markup-on-job-planning-lines)
  - [Batch replacing Item or GL account or Resource on Job Planning Lines](#batch-replacing-item-or-gl-account-or-resource-on-job-planning-lines)
  - [Batch updating unit cost and unit price on job planning lines based on relevant cards or pricelists](#batch-updating-unit-cost-and-unit-price-on-job-planning-lines-based-on-relevant-cards-or-pricelists)

## Archiving Jobs
Archiving job budget allows you to archive a jobs budget at certain time and compare it later to current budget.
### Setup
Open **Jobs Setup** and fill in relevant fields on **Archive Setup** tab.

<a href="https://apps.itera.ee/apps/Jobs365-General/docs/en-US/Jobs365ProSetupENG.png" target="_blank"><img src="Jobs365ProSetupENG.png" alt="Jobs Setup" width="600"/></a>

| Field | Explanation|
| --- | --- |
| ***Job Archive Nos.***| Võimaldab määrata projekti arhiivide numbriseeria.|
| ***Archive Quantity Unit of Measure***| Võimaldab määrata enimkasutatava mõõtühiku mille koguseid hakatakse kuvama Projekti ülesande ridadel veerus **Arhiveeritud eelarve kogus**.|
|***Show Archive Budget Quantity***| Võimladab määrata kas antud veergu kuvatakse Projekti ülesande ridadel.|
|***Show Archive Budget (Total Cost)*** | Võimladab määrata kas antud veergu kuvatakse Projekti ülesande ridadel.|
|***Show Archive Budget (Total Price)*** |Võimladab määrata kas antud veergu kuvatakse Projekti ülesande ridadel.|
|***Show Archived Billable (Total Price)***| Võimladab määrata kas antud veergu kuvatakse Projekti ülesande ridadel.|

### Usage
Open **Jobs list**, select relevant job and use button **Archive Budget** under Process tab. Insert **Version description** in the opening window for informational purposes and click **OK**:

<a href="https://apps.itera.ee/apps/Jobs365-General/docs/en-US/Jobs365ArhiveerimineENG.png" target="_blank"><img src="Jobs365ArhiveerimineENG.png" alt="Job Archiving" width="400"/></a>

Open **Job Card** and assign suitable archive version in **Initial Budget Version** field.
Open **Job Task Lines** (from Jobs List) and check **Archive..** columns. After changing budget/billable amounts the "archive" columns stay unchanged until you assign new archive version on **Job Card**.

<a href="https://apps.itera.ee/apps/Jobs365-General/docs/en-US/Jobs365ArhiveerimineProÜlReadENG.png" target="_blank"><img src="Jobs365ArhiveerimineProÜlReadENG.png" alt="Job Task Lines" width="700"/></a>

## Send Job budget to GL budget
Functionality allows you to send Job budgets (data from Job Planning Lines) to GL budget, so it would be easier to compare date in finance.

Go to **Jobs list** and use button **Send to G/L Budget** under Process tab.

Following view will be displayed:

<img src="JobToGLBudget.png" alt="JobToGLBudget" width="400"/>

| Field | Explanation|
| --- | --- |
| ***GL Budget name***| allows you to choose into which **GL Budget** you would like to send job data.|
| ***From Date*** and ***To Date***| allow you to filter which date range should be sent to **GL budget**. Filter will be applied to **Job Planning Lines** to be included.|
|***Line Type***| allows you to chosse which type of **Job Planning Lines** should be included.|
|***Include Cost Amounts*** and ***Include Price Amounts*** | allow you to choose if only costs should be sent to budget or only price amounts or both.
|***Default Gen. Business Posting Group*** | allows you to choose which **Gen. Business Posting Group** will be used for Item and Resource lines to find which Sales, Purchases or COGS account should be used.|
|***Include Budget Dimensions***| allows you to transfer dimension information from jobs to budget if some of the job dimensions match Budget dimensions.|

Additionally it is possible to use filter form **Job**, **Job Task** and **Job Planning Line** tables.

After pressing **OK** information from **Job Planning Lines** will be transferred to **GL Budget**.

# Jobs365 - General


## Batch changing discount or markup on Job Planning Lines
Functionality allows you to batch change markup or discount on **Job Planning Lines**.

Open **Job Task Lines** or **Job Planning Lines** and use button **Change markup/discount**.

Following view will be displayed:

<a href="https://apps.itera.ee/apps/Jobs365-General/docs/en-US/Jobs365MuudaJuurdeAllahindlustEE.png" target="_blank"><img src="Jobs365MuudaJuurdeAllahindlustEE.png" alt="Projekti plaanimisridadel allahindluste ja juurdehindluste massmuutmine" width="400"/></a>

| Field | Explanation|
| --- | --- |
| ***Job***| kuvatakse millise projekti ridu hakatakse muutma. Väli ei ole muudetav.|
| ***Markup %***| Võimaldab määrata juurdehindluse % ehk kui palju tuleks ühiku omahinnale müügihinna saamiseks juurde lisada. _Näide: Kui sisestada siia number 40 (ehk 40%) ning kui rea/ridade **Ühiku omahind** on 100 siis selle tulemsuena muudetakse rea/ridade **Müügihind** 140-ks (100*1,4)_.|
| ***Change Markup***| Võimaldab määrata kas antud käivitusega rakendatakse juurdehindluse muutmist või mitte.|
| ***Discount %***| Võimaldab määrata allahindluse % mida soovitakse real/ridadele rakendada. Peale käivitamist muudetakse kõikidel filtrisse jäävatel ridadel veergu **Rea hinnaalandi % (Allahindluse %)** ning arvutatakse vastavalt sellele ümber ka veerg **Rea summa**.|
| ***Change Discount***| Võimaldab määrata kas antud käivitusega rakendatakse allahindluse muutmist või mitte.|

Additionally it is possible to use filter form **Job Planning Line** table.

After pressing **OK** functionality will run with specified parameters.

## Batch replacing Item or GL account or Resource on Job Planning Lines
Functionality allows you to batch replace Itema, GL Account or Resource on **Job Planning Lines**.

Open **Job Planning Lines** and use button **Replace Iteam/Resource/GL Account**.

Following view will be displayed:

<a href="https://apps.itera.ee/apps/Jobs365-General/docs/en-US/Jobs365AsendaPRkontoRessurssKaupEE.png" target="_blank"><img src="Jobs365AsendaPRkontoRessurssKaupEE.png" alt="Projekti plaanimisridadel Kauba või PR konto või Ressursi massasendamine" width="400"/></a>

| Field | Explanation|
| --- | --- |
| ***Job***| kuvatakse millise projekti ridu hakatakse muutma. Väli ei ole muudetav.|
| ***Old Type to Change***| Võimaldab määrata millist liiki hakatakse asendama.|
| ***Old Item/Resource/GL Account to Change***| Võimaldab määrata millist kaupa, ressurssi või PR kontot soovitakse asendada. Valik sõltub sellest mis väärtus valiti väljale **Asendatav liik**.|
| ***New Type***| Võimaldab määrata millise liigiga hakatakse asendama.|
| ***New Item/Resource/GL Account***| Võimaldab määrata millise kauba, ressurssi või PR kontoga soovitakse asendada. Valik sõltub sellest mis väärtus valiti väljale **Uus liik**.|
| ***Maintain Unit Cost***| Võimaldab määrata kas asendamisel säilitatakse rea olemasoelv **Ühiku omahind** või uuendataske see vastavalt uuele kaubale või ressursile.|
| ***Maintain Unit Price***| Võimaldab määrata kas asendamisel säilitatakse rea olemasoelv **Müügihind** või uuendataske see vastavalt uuele kaubale või ressursile.|
| ***Update Description***| Võimaldab määrata kas asendamisel säilitatakse rea olemasoelv **Kirjaldus** või uuendataske see vastavalt uuele kaubale, ressursile või PR kontole.|

Additionally it is possible to use filter form **Job Planning Line** table.

After pressing **OK** functionality will run with specified parameters.

## Batch updating unit cost and unit price on job planning lines based on relevant cards or pricelists
Funktsionaalsus võimaldab kauba, PR konto või Ressursi asendamist mitmel projekti plaanimisreal korraga. 

Avage **Projekti ülesande read** või**Projekti plaanimisread** ning kasutage nuppu **Uuenda omahinnad/müügihinnad**.

Following view will be displayed:

<a href="https://apps.itera.ee/apps/Jobs365-General/docs/en-US/Jobs365UuendaMüügihinnadOmahinnadEE.png" target="_blank"><img src="Jobs365UuendaMüügihinnadOmahinnadEE.png" alt="Projekti plaanimisridadel ühiku omahindade ja müügihindade massuuendamine" width="400"/></a>

| Field | Explanation|
| --- | --- |
| ***Projekt***| kuvatakse millise projekti ridu hakatakse muutma. Väli ei ole muudetav.|
| ***Uuenda ühiku omahind***| Võimaldab määrata kas antud käivitusega rakendatakse ühiku omahinna uuendus või mitte.|
| ***Ühiku omahinna uuendamise alus***| Võimaldab määrata mille alusel ühiku omahinda uuendatakse. **_Ühiku omahind_** - Ühiku omahind uuendatakse kauba või ressursi kaardilt vastava välja alusel. **_Otsene kulu_** - Ühiku omahind uuendatakse kauba kaardilt (**Viimane otsene kulu**) või ressursi kaardilt () välja alusel. **_Ostuhinnakiri_** -  Ühiku omahind uuendatakse valitud **Ostuhinnakirja** alusel.|
| ***Ostuhinnakirja tähis***| Võimaldab määrata millise **Ostuhinnakirja** alusel Ühiku omahindu uuendatakse kui aluseks oli valitud **_Ostuhinnakiri_**.|
| ***Uuenda müügihind***| Võimaldab määrata kas antud käivitusega rakendatakse müügihinna uuendus või mitte.|
| ***Müügihinna uuendamise alus***| Võimaldab määrata mille alusel müügihinda uuendatakse. **_Ühiku hind_** - Ühiku hind uuendatakse kauba või ressursi kaardilt vastava välja alusel. **_Müügihinnakiri_** -  Ühiku hind uuendatakse valitud **Müügihinnakirja** alusel.|
| ***Müügihinnakirja tähis***| Võimaldab määrata millise **Müüghinnakirja** alusel Müügihindu (Ühiku hindu) uuendatakse kui aluseks oli valitud **_Müügihinnakiri_**.|

Additionally it is possible to use filter form **Job Planning Line** table.

After pressing **OK** functionality will run with specified parameters.

