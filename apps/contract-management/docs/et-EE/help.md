# Lepingute haldus
Lepingute funktsionaalsus võimaldab BC-s järgmist:

- Müügi- ja ostulepingute haldus
- Müügipäise ja müügiridade summade jälgimist lepingu numbri alusel
- Ostupäise ja osturidade summade jälgimist lepingu numbri alusel
- Lepingute tugi projekti kaardil projekti müügiarvet loomiseks
- Partneri ja lepingute tugi projekti plaanimisridadel planeerimise eesmärgil 
- Vaikedimensioonide kasutamine lepingtel
- Lepingu arvelduse ridade loomine
- Perioodiliste müügiarvete loomine lepingu arvelduse ridade alusel

## Sisukord
  - [Seadistamine](#seadistamine)
    - [Lepingu kategooriad](#lepingu-kategooriad)
  - [Kasutamine](#kasutamine)
    - [Lepingu loomine](#lepingu-loomine)
    - [Lepingu kasutamine ostu- ja müügidokumentidel](#lepingu-kasutamine-ostu--ja-müügidokumentidel)
    - [Lepingu täituvuse jälgimine](#lepingu-täituvuse-jälgimine)
    - [Lepingute kasutamine projektides](#lepingute-kasutamine-projektides)
  - [Arveldamine](#arveldamine)
    - [Lepingu arvelduse ridade loomine](#lepingu-arvelduse-ridade-loomine)
    - [Loo lepingu müügiarved](#loo-lepingu-müügiarved)

## Seadistamine
Funktsionaalsuse kasutamiseks tuleb **Lepingute seadistuses** seadistada järgmised väljad:

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManSetupEE.png" target="_blank"><img src="ContManSetupEE.png" alt="Lepingute Seadistus" width="800"/></a>

| Väli | Selgitus |
| --- | --- | 
| **_Lepingute numbrid_** | Antud väljal määratakse ära lepingute numbriseeria. Väärtus on valitav **Numbriseeriate** loendist.|
| **_Lepingu täitmise kontod_** | Tuleb ära määrata PR kontode filter mille pealt hakatakse lugema lepingu täitmist. Näiteks tulu ja kulukontod, kuhu tekib lepingu kandeid. Kindlast võiks välja jätta käibemaksu ja reskontroga seotud kontod. Võib sisestada konkreetsed kontod ja/või kontode vahemiku (näiteks vahemik 30000..90000).|
|**_Transfer Contract No to Job Sales Header_** |Enables transferring Contract No. from Job Card to new Job Invoice Header.
|**_Default Contract Type_**|Specifies default Contract Type for new contracts.
|**_Def. Contract Category Sales_**|Specifies default Contract Category for sales contracts.
|**_Def. ContractCategory Purchase_**|Specifies default Contract Category for purchase contracts.

_Billing related setup_

|Field|Explanation|
|---|---| 
|**_Show Billing Information_**|Enables Billing Information tab on sales contracts.
|**_Create Contract Invoice Lines Date Formula_**|Specifies default date formula for Next Billing Date in Create Contract Invoice Lines (CM).
|**_Create Sales Invoices Date Formula_**|Specifies default date formula for Posting Date in Create Sales Invoices (CM).

----

### Lepingu kategooriad

Contract categories allow you to define different type of categories in order to divide your contracts into different groups.

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManContCategoriesEE.png" target="_blank"><img src="ContManContCategoriesEE.png" alt="Lepingu kategooriad" width="800"/></a>

|Field| Explanation|
|---|---| 
| **_Contract Category Code_** | Specifies a category code for the contract.|
| **_Contract Category Description_** | Decription to define which contracts are categorized to this category|
|**_Sales, Purchase, Other_**| Sales should be marked if category should be availabele on sales contracts (Type **Sales**), Purchase should be marked if category should be availabele on purchase contracts (Type **Purchase**), Other should be marked if category should be availabele other contracts (Type **Other**).
|**_No. of Sales Contracts_** and **_No. of Purchase contracts_**| Shows number of Sales/Purchase contracts in that category.|

_Billing related category setup_

|Field|Explanation|
|---|---| 
| **_Def. InvoicingFrequency Option_** | Specifies default Invoicing Frequency Option for contracts in this category.|
| **_Invoicing Frequency"_** | Specifies default Invoicing Frequency for contracts in this category.|
| **_Default Type_** | Specifies default Type for contract lines for contracts in this category.|
| **_Default No._** | Specifies default No. for contract lines for contracts in this category.|

---
 
## Kasutamine
### Lepingu loomine

Lepingute lahenduse puhul on võimalik hallata nii ostu-, müügi- kui ka muid lepinguid. Uue lepingu sisestamiseks tuleb avada **Lepingud** ning luua uus kirje kasutades nuppu **+Uus**.

Avaneval lepingu kaardil on võimalik täita järgenvad väljad:

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManContractCardEE.png" target="_blank"><img src="ContManContractCardEE.png" alt="Lepingu kaart" width="800"/></a>

| Väli | Selgitus |
| --- | --- | 
| Lepingu nr.* | Täitub automaatselt vastavalt **Lepingute seadistuses** määratud numbriseeriale.|
| Nimetus ja Kirjeldus** | Lepingu nimetuse ja lühikirjelduse sisestamiseks.|
| Partneri nr.* | Võimaldab määrata lepingu osapoole, valik toimub **Kontaktide loendist**. Kui kontakt on seotud ka mõne **Kliendi** või **Hankijaga** siis kuvatakse vastavad andmed väljadel _Kliendi nr ja nimi_ ning _Hankija nr ja nimi_. |
| Lepingu tüüp* | Määratakse ära kas tegemist on ostu, müügi või mõne muu lepinguga. Valik määrab ühtlasi ära ka selle kas leping on valitav ostuarvele (**Ost**) või müügiarvele (**Müük**).|
|Pealepingu nr. | Võimaldab lepingute grupeerimist ühise tunnuse (pealepingu) alla, väljalt avaneb valik **Lepingute loendisse**. Vaikimisi täidetakse lepingu enda numbriga.|
|Välise lepingu nr. | Võimaldab sisestada partneripoolse lepingu numbri.|
| Algus- ja Lõpukuupäev** | Määratakse ära mis on lepingu kehtivusaeg. Väli on informatiivse tähendusega|
| Summa** | Võimaldab määrata lepingu summa, mille alusel hakatakse kuvama ka lepingu jääki.|
| Summa KM-ga | Võimaldab sisestada lepingu summa koos käibemaksuga.|
| Maksetingimused | Võimaldab määrata lepingus kokkulepitud maksetingimused. Value will be transferred to Sales/Purchase header after chosing contract in document header.|
|Salesperson/Purchaser Code| Specifies a code for the salesperson/purchaser who is responsible for the contract. Value will be transferred to Sales/Purchase header after chosing contract in document header.
| Lukus | Võimaldab lepingu märkida lukus olevaks. Lepingut ei kuvata enam lepingu valiku juures ost- ja müügidokumentidel ega projektide valikutes.|

*_Väljad mis tuleb kndlasti täita_
**_Väljad mis on soovituslikud täita_

Vahekaardil **Seosed** kuvatavad väljad (Kliendi nr. ja nimi ning Hankija nr. ja nimi) täituvad automaatselt peale partneri valimist. Väljad täituvad ainult juhul kui partneriks valitud **Kontakt** on seotud kliendi ja/või hankijaga. Kui seos luuakse hiljem, siis tuleb lepingu päises kasutada tegevust **Uuenda kliendi/hankija seos**, mis uuendab Kontaktiga (Partneri nr.) seotud Kliendi ja Hankija seosed ka lepingul.
 
### Lepingu kasutamine ostu- ja müügidokumentidel
Müügi- ja ostudokumentidel on võimalus valida päisesse väljale **_Lepingu number_** sobiv leping **Lepingute loendist**. Kui dokumendi päisesse on lepingu number valitud siis lisatakse see automaatselt ka igale dokumendi reale. Dokumendi ridadel on võimalik lepingu numbrit muuta. 


#### _Tähtis_
---
_Dokumentidele valitavate lepingute valik on piiratud järgnevate tunnuste alusel:_
- _Lepingu liigiga ehk müügidokumentidele saab valida lepinguid liigiga **_Müük_** ja ostudokumentidele liigiga **_Ost_**._
- _Ostja või müüja numbriga ehk müügidokumentidel **_Ostja-kliendi number_** ning ostudokumentidel **_Müüja-Hankija number_**._
- _Valikust jäävad välja ka **_Lukus_** lepingud._

_Kui tingimustele vastavat lepingut siiski valikus ei kuvata võib asi olla selles, et lepingul on uuendamata Kliendi/Hankija seos. Uuendamiseks tuleb **Lepingu kaardil** vajutada nuppu **Uuenda kliendi/hankija seos**, mis uuendab **Kontaktiga** (Partneri nr.) seotud **Kliendi** ja **Hankija** väärtused lepingul._

---

Dokumendi konteerimisel kantakse lepingu number edasi konteeritud dokumentidele, pearaamatusse, kliendi- ja hankijareskontrosse ning projektiandmiku kannetesse. 


#### _Tähtis_

--- 
_Arvestama peab sellega, et kliendi- ja hankijareskontrosse liigub lepingu number mis on valitud dokumendi päisesse. Kui ridadel on kasutatud ka teisi lepingu numbreid siis need liiguvad edasi vastavatele tulu ja kulukannetele._

---

### Lepingu täituvuse jälgimine

Lepingu täituvust ning jääki on võimalik jälgida **Lepingute loendist** või **Lepingu kaardilt** järgnevatelt väljadelt:

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManCompletionTrackingEE.png" target="_blank"><img src="ContManCompletionTrackingEE.png" alt="Lepingu täituvuse jälgimine" width="1000"/></a>

- Täitmine (KV) - kuvab lepinguga seotud summasid **Pearaamatu kannete alusel**. Kannetele on summa arvutamiseks rakendatud **Lepingute seadistuses** määratud filtrit.
- Jääk (KV) - kuvab lepingu jääki mis leitakse väljade **_Summa_** ja **_Täitmine (KV)_** alusel

Lisaks on nii loendist kui kaardilt võimalik avada ka seotud **Pearaamatu kanded** kasutades selleks nuppu **Täitmise kanded**.
 

### Lepingute kasutamine projektides
Lepinguid on võimalik kasutada ka projektimoodulis nii **Projekti kaardil** kui ka **Projekti plaanimisridadel**.


**Projekti kaardile** on võimalik sisestada projektiga seotud müügileping. 

Lepingu valimisel rakenduvad järgnevad filtrid:
- Lepingu liik ehk projektile saab valida lepinguid liigiga **_Müük_**.
- Klient ehk projektile saab valida lepinguid mis on seotud projektil märgitud **_Maksja-kliendi nr._**-ga.
- Valikust jäävad välja ka **_Lukus_** lepingud.

Projekti müügiarve loomisel kantakse leping üle ka loodavale **Müügiarvele**.

**Projekti plaanimisridadele** on võimalik sisestada **_Partneri nr._** ning temaga seotud ostu- või müügileping. See võimaldab jälgida seda kas näiteks allhanke puhul on partneriga juba leping sõlmitud või mitte ning hiljem jälgida ka lepingu täituvust.

Lepingu valimisel rakenduvad järgnevad filtrid:
- Partner ehk projekti plaanimisreale saab valida lepinguid mis on seotud projekti plaanimisreale märgitud **_Partneri nr._**-ga.
- Valikust jäävad välja ka **_Lukus_** lepingud.

---

## Arveldamine

You can enter billing information on contract card and then fill in contract lines. After that billing lines can be created, in order to check possible deviations and to have a longer view, and finally sales documents can be created.

#### _Important_

--- 
_**Billing Information** tab becomes visible only if it is allowed in **Contract Setup** and on contracts of type **Sales**! **Contract Lines** tab becomes visible after billing information date related fields are filled in and **Add Contract Lines** has been clicked!_

---

On **Billing Information** tab you can fill following fields:

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManBillingInfoEE.png" target="_blank"><img src="ContManBillingInfoEE.png" alt="Arvelduse info" width="1000"/></a>

|Field|Explanation|
|---|---| 
| **_Bill-to Customer No._** | Specifies Bill-To Customer. If not filled in Customer default value will be used on invoice creation.|
| **_Ship-to Code_** | Specifies Ship-To Code. If not filled in Customer default value will be used on invoice creation.|
| **_Invoicing Frequency Option_** | Specifies default Invoicing Frequency Option for lines.|
| **_Invoicing Frequency_** | Specifies default Invoicing Frequency for lines. By default field is not visible.|
| **_Billing Start Date_** | Specifies default Billing Start Date for lines.|
| **_End Date First Period_** | Specifies default End Date of the first billing period for lines. For an example this field allows to play with the length of the first period in order to adjust future periods to fit into full months.|
| **_Billing End Date_** | Specifies default Billing End Date for lines.|
| **_Add Contract Lines_** | Enables **Contract Lines** and inserts first contract line with default values from **Contract Category** and **Billing Information** tab.|

On **Contract Lines** tab you can fill following fields:

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManContLinesEE.png" target="_blank"><img src="ContManContLinesEE.png" alt="Lepingu read" width="800"/></a>

|Field|Explanation|
|---|---| 
| **_Type_** | Allows to specify type. Default value will be taken from **Contract Category**.|
| **_No._** | Allows to specify No. to be billed. First line default value will be taken from **Contract Category**|
| **_Description_** | Allows to specify line description.|
| **_Quantity_** | Allows to specify quantity to be billed.|
| **_Unit of Measure Code_** | Allows to specify unit of measure to be billed. Field is not visible by default.|
| **_Unit Price Excl. VAT_** | Allows to specify line unit price to be billed.|
| **_Line Amount Excl. VAT_** | Displays calculated line amount. Field is not editable.|
| **_Valid_** | Allows to specify if line is valid or not. Default value is Valid.|
| **_Add Period Text_** | Allows to specify if new text line with period information will be added after this line when creating invoice information.|
| **_Invoicing Frequency Option_** | Specifies billing period/frequency for current line. Default value will be taken from **Billing Information** tab.|
| **_Billing Start Date_** | Allows to specify Billing Start Date for current line.|
| **_End Date First Period_** | Allows to specify End Date First Period for current line. Default value will be taken from **Billing Information** tab.|
| **_Next Billing Date_** | Displays **Nexte Billing Date** (next period start date) for current line after [Create Contract Invoice Lines](#create-contract-invoice-lines) has been run|
| **_Billing End Date_** | Allows to specify Billing End Date for current line.. Default value will be taken from **Billing Information** tab.|

Contract line based sales orders/invoices creation consists of two steps.

### Lepingu arvelduse ridade loomine
First step is to create **Contract Invoice Lines**.

Open **Contracts List** or **Contract Card** and use action **Create Contract Invoice Lines (CM)**.
Following window will be opened:

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManCreateContInvLinesEE.png" target="_blank"><img src="ContManCreateContInvLinesEE.png" alt="Lepingu arvelduse ridade loomine" width="500"/></a>

Fill in **Next Billing Date**, this date will be an end date for a range that will be applied to **Valid** contract lines. It will be applied to **Next Invoicing Date** or to **Billing Start Date** (if the other is empty) and **Contract Invoice Lines** will be created for each **Contract Line** that meets the filtering criteria. 
* By default it is filled with Today + date formula from **_Create Contract Invoice Lines Date Formula_** in **Contract Setup**.
* Additonal filters can be applied from **Contracts** or **Contract Lines**.
* If clicked from **Contract Card** then **_Contrat No_** filter will be entered automatically. 

Press **OK**.

Use action **Contract Invoice Lines** from **Contract Card** to open list. Check if lines were created and if they look OK for creating invoices/orders. _List is not editable_.

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManContInvLinesEE.png" target="_blank"><img src="ContManContInvLinesEE.png" alt="Lepingu arvelduse read" width="800"/></a>

Some of the fields need no explanation. Other will be explained below.

|Field|Explanation|
|---|---| 
| **_Posting Date_** | By default **Period Start Date**.|
| **_Period Start Date_** and **_Period End Date_**  | Are reflecting the actual billing period|
| **_Status_** | Shows status of current line. **New** - First status for alla created lines. Also line gets this status back when it is removed from order/invoice. or removed . **Order** - **Sales Order** has been created from that line. **Invoice** - **Sales Invoice** has been created from that line. **Posted** - involved sales order/invoice has been posted. **Canceled** - line has been canceled by using action **Cancel**, only **New** lines can be canceled.|
| **_Document No._** | Shows document number of the involved document (order, invoice, posted invoice).|

---

### Loo lepingu müügiarved
Teien samm on **Müügitellimuste** või **Müügiarvete** loomine.

Open **Contracts List** or **Contract Card** and use action **Create Sales Invoices (CM)**.
Following window will be opened:

<a href="https://apps.itera.ee/apps/contract-management/docs/et-EE/ContManCreateSalesInvEE.png" target="_blank"><img src="ContManCreateSalesInvEE.png" alt="Lepingu müügiarvete loomine" width="500"/></a>

Fill in **Posting Date**, this date will be an end date for a range that will be applied to **Contract Invocie Lines**. It will be applied to **Posting Date** and **Sales Invoices/Orders** will be created for contract invoice lines that meet the filtering criteria and combined according to **Create Invoices By**.
* By default it is filled with Today + date formula from **_Create Sales Invoices Date Formula_** in **Contract Setup**.
* Additonal filters can be applied from **Contracts** or **Contract Invoice Lines**.
* If clicked from **Contract Card** then **_Contrat No_** filter will be entered automatically. 

|Field|Explanation|
|---|---| 
| **_Replace Posting Date_** | Allows to replace invoice/order **Posting Date**. Otherwise Posting Date will be taken from Contract Invoice Line. |
| **_Create Invoices By_** | Allows to select how the lines should be grouped among documents. **Contract** - one invoice/order for each contract. Only lines from one contract will be included in one invoice/order. **Customer** - one invoice/order per customer. Lines from different contracts that have the same customer will be included in one invoice/order. **Main Contract** - one invoice/order per main contract. Lines from different contracts that have the same main contract will be included in one invoice/order.|
| **_Create as Invocie or Order_** | Allows to select which type of sales docuemnts should be created: **Invoices** (default) or **Orders**.|

Press **OK**.

---

Täpsema info saamiseks, palun võtke ühendust BCS Itera AS-ga:  
https://www.itera.ee
