#   Factoring Solution | User Manual
Factoring functionality enables to automate sales invoice transmissions to a factor and subsequently process factor payments incl. commissions and interests. Only factor Swedbank AS is supported.
### Main features :
*   Highly configurable setup of factoring agreements.
*   Generating a list of sales invoices according to Swebank file format.
*   Overview of transmitted/untransmitted receivables and payment status.
*   Recourse and non-recourse factoring agreements are supported. 
*   Assignment note on sales invoice in customers' language. 
*   Factor XML-fail import and automated generation of journal lines according to contract type, incl. 
    *   application of advance and payments under reserve.
    *   application of commission fees, VAT and interests.    
*   Customer or contract-based factoring limits. 
## Setup
To use the functionality, factoring agreement(s) must be created and editable fields be filled. Open **Factoring Agreements** and press button **+New**. 
|Field | Description|Editable / Informative| 
|---|---|---|
|No. **| Number of factoring agreements| Editable|
|Description|Description of the factoring agreement|Editable|
|Factoring Text on Invoice **|Assignment note|Editable|
|Add Factoring Text on posting |Function, that enables to add assignment note after sale invoice rows |Editable|
|Limit:|Limit of the factoring agreement|Editable|
|No. of customers|Number of customers linked with the factoring agreement|Informative|
|Customers Limits|Field displays total sum of the fields **Factoring Limit** from customer cards|Informative|
|No. of Untrasmitted Invoices|Numeral total of posted invoiced, that were not transmitted to factor|Informative|
|Untrasmitted Invoices Amount|Total sum of posted invoiced, that were not transmitted to factor|Informative|
|No. of Open Entries|Numeral total of posted sales invoices associated with factoring agreement|Informative|
|Factoring Type|Type of factoring agreement. Recourse and non-recourse factoring contracts are supported|Editable|
|Factoring Vendor No. *** |Assistive vendor. Short-term liability through Vendor entry is being created after receiving payments from factor|Editable|
|Factoring Customer No. ***|Assistive customer. Transmitted to factor sales invoices are transferred to this customer|Editable|
|Commission G/L Account No.|Account from the chart of accounts commission fees and VAT are being posted to|Editable| 
|Interest G/L Account No.|Account from the chart of accounts interests are posted to|Editable|
|Bank account|Bank account No associated with this factoring agreement|Editable|
|Transmissions Nos.|Code of a number series from number series list, that is used while creating transmission lines|Editable|\   

** Mandatory field  
*** Page **Standard text** codes allows to manage assignment notes text according to customer's Country/Region code. This allows to add text in different languages.  
**** Factoring Customer No. is compulsory in case of recourse factoring agreement and Factoring Vendor No. is compulsory in case of non-recourse factoring agreement. Both can be defined, but appropriate one will be used depending on factoring agreement type.
##  Factoring Agreements  
Page contains two buttons **Create Transmission** and **Transmissions** in menu section and table fields  
* **Create Transmission**  - action button, that initiates transmission process. Process results in creating transmission rows, which can be further processed.
* **Transmissions**- opens **Factoring Transmissions** page.   

|Field | Description|
| --- | --- |
|No.|Factoring agreement's number|
|Description|Description of the factoring agreement |
|No. of Customers| Numeral total of customers associated  with this factoring agreement|
|No. of Untrasmitted Invoices| Numeral total of posted invoices, that were not transmitted to factor|
|Untrasmitted invoices amount|Total sum of posted invoices that were not transmitted to the factor|
|No.of open entries|Number of transferred and unpaid invoices|
|Limit|Displays the **Limit** fields value from factoring agreement card page|

## Factoring Transmissions page
Page displays transmissions to factor, it contains two action buttons **Transfer to Journal** and **Export to File** and table fields.  
* **Transfer to Journal**- a transmission row must be chosen before clicking **Transfer to Journal**. Journal and journal worksheet names are asked after pressing **Transfer to Journal** button. As a result of this action General Journal lines are created and ready for posting. After posting  customer's invoice is marked as paid and Factoring Customer ledger entry is created. Transferred receivable consists of copied information about the invoice number, sum, payments terms ets. 
* **Export to File** - action generates file in Excel according to Swedbank AS format terms. Excel file must be submitted to factor manually in accordance with contracted conditions.  

Factoring Transmissions page fields
|Field | Description|
| --- | --- |
|No.|Number of transmission from number series|
|Transmission Date|Data when transmission was created|
|No. of Invoice|Number of transmitted invoices|
|Invoices Amount|Sum of transmitted invoices|
|No.of open entries|Number of unpaid invoices|
|No.of factoring agreement|Factoring agreement number the invoices are associated with|
## Use
*   **Setup factoring agreement**  
To use the factoring functionality user must create new factoring agreement. Open **Factoring Agreements** and press button **+New** and fill all editable fields. 
*   **Adding factoring agreement to a customer card**\
    Connection between factoring agreement and customers generates by filling Factoring Agreement No. field  on customers card. In the same place customer limit can be settled. Total amount of limits from all customer cards are displayed summarily at factoring agreement page.  
    NB! While creating sales invoice or sales order use can pick up any factoring agreement from the factoring agreements list. 
    
*   **Creating an export file to factor**\
This stage is described in **Export to File** section. 
*   **Closing sales invoice and transferring accounts receivables to Factoring customer**
Action can be performed in case of recourse factoring agreement only and is described in **Transfer to Journal** section. 

*   **Importing XML data file**\
XML is generated each time factor makes payment. This XML file can be downloaded and then imported to Business Central. To import file open  **Cash Receipt Journal** and click **Factoring Import** under Process section. Factoring agreement number is requested firstly and the XML data file location. Journal lines are generated automatically in accordance with factoring agreement setup.

### Here is an overview how cash receipt lines are created after XML file import.

**Advanced payment receipt under non-recourse factoring agreement** 
|Journal line | Debit/Credit| Description|
| --- | --- |--- |
|Factoring Customer|Credit|Factoring Customer No. field value from Factoring agreement page|
|Bank Account|Debit|Bank account from Factoring agreement page|
|Commission|Debit| Commission G/L account No. field value from Factoring agreement page|
|Commission VAT|Debit|Commission G/L account No. field value from Factoring agreement page|

**Reserve payment receipt under non-recourse factoring agreement**
|Journal line  | Debit/Credit|Description|
| --- | --- |--- |
|Factoring Customer|Credit|Factoring Customer No. field value from Factoring agreement page|
|Bank account|Debit|Bank account from Factoring agreement page|
|Interest|Debit|Interest G/L account no. field value from Factoring agreement page|

**Advanced payment receipt under recourse factoring agreement** 
|Journal line  | Debit/Credit| Description|
| --- | --- |--- |
|Factoring Vendor Entry|Credit| Factoring Vendor from Factoring agreement page|
|Bank Account|Debit|Bank account from Factoring agreement page|
|Commission |Debit|Commission G/L Account No. field value from Factoring agreement page|
|Commission VAT|Debit|Commission G/L Account No. field value from Factoring agreement page|

**Reserve payment receipt under recourse factoring agreement**   
|Journal line| Debit/Credit| Description|
| --- | --- |--- |
|Factoring Vendor Entry|Debit| Factoring Vendor from Factoring agreement page |
|Bank Account|Debit|Bank account from Factoring agreement page|
|Interest |Debit|Interest G/L from Factoring agreement page|
|Transferred invoice|Credit|Total of transferred invoice under recourse contract*| 
*NB! After reserve payment is received, Factoring Vendor Entries are applied to Transferred invoice, thus remaining amount of short-term liability and receivable equals to zero.

---
For more information, please contact:  
[https://www.itera.ee](https://www.itera.ee)