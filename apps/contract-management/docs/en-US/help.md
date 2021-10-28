# Contract Management
Contract management functionality in BC enables the following:

- Management of sales and purchase contracts
- Tracking of sales header and sales line amounts by contract number
- Tracking of purchase header and purchase line amounts by contract number
- Contract support on Job card for creating job sales invoices
- Partner and contract support on job planning lines for planning purposes
- Use default dimensions on contracts.

## Table of Contents
  - [Settings](#settings)
    - [Contract Categories](#contract-categories)
  - [Use](#use)
    - [Contract management](#Contract-management)
    - [Using contracts on purchase and sales documents](#Using-contracts-on-purchase-and-sales-documents)
    - [Contract completion tracking](#Contract-completion-tracking)

## Settings
To use the functionality, **Contract Setup** must be opened and following fields filled:

<img src="ContManSetupENG.png" alt="ContManContSetup" width="1000"/>

|Field|Explanation|
|---|---| 
| **_Contract numbers_** | For defining contract number series. Value can be chosen from **No. Series List**.|
| **_Contract Usage Accounts_** | Allows to define a GL accounts filter for contract usage calculation. For an example income and expense accounts on which you expect transaction related to contracts. It is advisable to exclude VAT, payables and receivables accounts. You can define specific accounts and/or an accounts range (for an example range 30000..90000).|
|**_Transfer Contract No to Job Sales Header_** |Enables transferring Contract No. from Job Card to new Job Invoice Header.

### Contract Categories

Contract categories allow you to define different type of categories in order to divide your contracts into different groups.

<img src="ContManContCategoriesENG.png" alt="ContManContCategories" width="1000"/>

|Field| Explanation|
|---|---| 
| **_Contract Category Code_** | Specifies a category code for the contract.|
| **_Contract Category Description_** | Decription to define which contracts are categorized to this category|
|**_Sales, Purchase, Other_**| Sales should be marked if category should be availabele on sales contracts (Type **Sales**), Purchase should be marked if category should be availabele on purchase contracts (Type **Purchase**), Other should be marked if category should be availabele other contracts (Type **Other**).
|**_No. of Sales Contracts_** and **_No. of Purchase contracts_**| Shows number of Sales/Purchase contracts in that category.|

 
## Use
### Contract management

With contract management it is possible to manage purchase, sales and other contracts. For creating a new contract you must open **Contracts** and use button **+New** in order to create a new entry.

An empty **Contract card** opens where you can fill the following fields:

<img src="ContManContractCardENG.png" alt="ContManContractCard" width="1000"/>

|Field| Explanation|
|---|---| 
| Contract No.* | Is filled automatically according to defined Number Series from **Contract Setup**.
| Name and Description** | For entering contract and short description.
| Partner No.* | Allows to choose contract partner from **Contact list**. If contact is related to a **Customer** or **Vendor** then related information will be displayed on **Relations** tab  on fields _Customer No. and Name_ and _Vendor No. and Name_. 
| Contract Type* | Defines if it is a purchase, sales or other type of contract. Option also defines if that contract can be chosen to Purchase document (**Purchase**) or to Sales document (**Sales**).
|Main Contract No. | Allows to group contracts under a common value (Main Contract), that can be chosen from **Contract List** filtered by field **Main Contract**. Default value is contract's own number.
|Main Contract| Allows that contract to be chosen as main contract.
|External Contract No. | Allows to enter partners contract number.
| Start and End Dates** | Allows to define validity dates of the contract. Field is informative.
| Amount** | Allows to enter contract amount, this amount is base for calculating the reminder of the contract.
| Amount Incl. VAT | Allows to enter contract amount including VAT.
| Payment Terms | Allows to define agreed payment terms. Value will be transferred to Sales/Purchase header after chosing contract in document header.
|Salesperson/Purchaser Code| Specifies a code for the salesperson/purchaser who is responsible for the contract. Value will be transferred to Sales/Purchase header after chosing contract in document header.
| Blocked | Allows to mark contract as Blocked. Contract will no longer be displayed in drop down list on purchase and sales documents, job and job planning lines.

*_Fields that must be filled_
**_Fields that are advisable to fill_

Fields displayed on fast tab **Relations** (Customer No. and Name, Vendor No. and Name) are filled automatically after partner selection. Fields will only be filled if the selected **Contact** is related to **Customer** and/or **Vendor**. If the relation will be created later, then contract must be updated manually by pressing button **Update Customer/Vendor link** on contract card. This updates Contact's relations with Customer and Vendor on contract.
 
### Using contracts on purchase and sales documents
On sales and purchase document headers you can select appropriate contract from **Contract List** in the field **_Contract No._**. If contract has been selected in the header then it will be automatically transferred to lines. It is possible to change contract number on lines. 


#### _Important_
---
_Selection of contracts that can be chosen to document is limited with the following:_
- _Contract type - on sales documents you can select contracts with the type of **_Sales_** and on purchase documents with the type of **_Purchase_**._
- _Buyer or Seller number - sales documents **_Sell-To Customer No._** and purchase documents **_Buy-From Vendor No._**._
- _**Blocked** contracts will be left out._

_If there is no contract in the selection that meets the requirement, then it might be due to Customer/Vendor relations that have not been updated on contract card. In order to update the relations button **_Update Customer/Vendor link_** must be pressed on related contract card.This updates Contact's relations with Customer and Vendor on contract_.

---

Contract number will be transferred to posted documents, **General Ledger Entries**, customer and vendor ledgers and **Job Ledger Entries** after posting. 


#### _Important_

--- 
_It must be taken into account that document header contract number will be transferred to customer and vendor ledgers. If different contract have been used on lines then those will be transferred to related income and expenses accounts._

---

### Contract completion tracking

You can track the completion and reminder of the contract from the **Contract List** or **Contract Card** by checking following fields:

<img src="ContManCompletionTrackingENG.png" alt="ContManCompletionTracking" width="1000"/>

- **Completion (LCY)** - displays contract related amounts from **General Ledger Entries**. Account filter from the **Contract Setup** has been applied to entries.
- **Reminder (LCY)** - displays contract remaining amount that is calculated on the basis of fields **_Amount_** and **_Completion (LCY)_**.

Additionally it is possible to open list of related **General Ledger Entries** by using **Completion entries** button in contract list or on contract card.
 

### Using contracts in Jobs
It is possible to use contract in Job module on **Job Card** and in **Job Planning Lines**.

**Job Card** - it is possible to enter related sales contract to a job by selecting appropriate contract from **Contract List** in the field **_Contract No._**  

Selection of contracts that can be chosen to job is limited with the following:
- Contract Type - contracts with type **Sales** can be used for jobs.
- Customer - contracts that are related to **_Bill-To Customer No._** from job card can be used.
- **Blocked** contracts will be left out.

Contract will be transferred to **Sales Invoice** when creating an invoice for a job by using action **_Create Job Sales Invoice_**.

**Job Planning Lines** - it is possible to enter **_Partner No._** and related **_Contract No._** to job planning lines. That allows track, for an example, if you already have a contract with subcontractor or no for a specific task. Later it will help to track completion..

Selection of contracts that can be chosen to job planning line is limited with the following:
- Partner - contracts that are related to selected **_Partner No._** can be used.
- **Blocked** contracts will be left out.

---

For more information please contact BCS Itera AS:  
https://www.itera.ee
