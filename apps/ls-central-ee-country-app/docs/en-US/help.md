# LS Central Estonian Country App – User Guide.
**LS Central Estonian Country App** extends Dynamics 365 Business Central Estonian localization functionality related data fields and actions to LS Central pages (metadata cards/lists and documents).

## Setup
There is no special setup needed for LS Central Estonian Country App. Installation and configuration (according to User Guide links provided below) of the following Dynamics 365 Business Central Estonian localization apps is a prerequisite for using LS Central Estonian Country App:
* **Estonian Dynamics Partners Estonian Language (Estonia)** – Estonian translations for Business Central W1 version.<br> User Guide: [https://dynamicspartnersee.github.io/apps/estonian-language/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-language/docs/en-US/help)
* **Estonian Dynamics Partners Balance Statements** <br> User Guide: [https://dynamicspartnersee.github.io/apps/balance-statements/docs/en-US/app](https://dynamicspartnersee.github.io/apps/balance-statements/docs/en-US/app) 
* **Estonian Dynamics Partners Business Register localization for Estonia** <br> User Guide: [https://dynamicspartnersee.github.io/apps/estonian-business-register/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-business-register/docs/en-US/help)
* **Estonian Dynamics Partners Banking Formats localization for Estonia** <br> User Guide: [https://dynamicspartnersee.github.io/apps/estonian-banking-formats/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-banking-formats/docs/en-US/help)
* **Estonian Dynamics Partners Intrastat Reporting localization for Estonia** <br> User Guide: [https://dynamicspartnersee.github.io/apps/estonian-intrastat-reporting/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-intrastat-reporting/docs/en-US/help)
* **Estonian Dynamics Partners Package Excise localization for Estonia** <br> User Guide: [https://dynamicspartnersee.github.io/apps/estonian-package-excise/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-package-excise/docs/en-US/help)
* **Estonian Dynamics Partners Prepayment Management** <br> User Guide: [https://dynamicspartnersee.github.io/apps/prepayment-management/docs/en-US/help](https://dynamicspartnersee.github.io/apps/prepayment-management/docs/en-US/help)
* **Estonian Dynamics Partners VAT Reporting localization for Estonia** <br> User Guide: [https://dynamicspartnersee.github.io/apps/estonian-vat-reporting/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-vat-reporting/docs/en-US/help)

***Note!** All apps are installed and published as usual. The same counts for the process of removing apps.* 
<br><br>

### Technical detail about LS Central Estonian Country App
**BCS Itera_LSC Estonian Country App_xx.x.xxxxx.x.app** is a small app which adds Dynamics 365 Business Central Estonian localization functionality related data fields and actions to LS Central pages (metadata cards/lists and documents). It includes the following objects:

* **Pageextension 70404925 "BCS.LSC CustomerListExt"** extends **"LSC Retail Customer List"**
    *   Fields added: **BRQ Registration No.**
    *   Actions added: **BRQ Update Data from Business Register**
    *   **New > Sales Order** option replaced with **Retail Sales Order**, the action runs new document **LSC Retail Sales Order**
    *   **New Document > Sales Return Order** option replaced with **Retail Sales Return Order**, the action runs new document **LSC Retail Sales Return Order**

* **Pageextension 70404926 "BCS.LSC CustomerCardExt"** extends **"LSC Retail Customer Card"**
    *   Fields added: **SBS Balance Statement E-Mail**, **BRQ Registration No.**, **BNK Payment Reference No.**
    *   Actions added: **BRQ Query from Business Register**
    *   **New > Sales Order** option replaced with **Retail Sales Order**, the action runs new document **LSC Retail Sales Order**
    *   **New Document > Sales Return Order** option replaced with **Retail Sales Return Order**, the action runs new document **LSC Retail Sales Return Order**  

* **Pageextension 70404927 "BCS.LSC VendorListExt"** extends **"LSC Retail Vendor List"**
    *   Fields added: **BRQ Registration No.** 
    *   Actions added: **BRQ Update Data from Business Register**
    *   **New > Purchase Order** option replaced with **Retail Purchase Order**, the action runs new document **LSC Retail Purchase Order**
    *   **New Document > Purchase Return Order** option replaced with **Retail Purchase Return Order**, the action runs new document **LSC Retail Purchase Return Order**

* **Pageextension 70404928 "BCS.LSC VendorCardExt"** extends **"LSC Retail Vendor Card"**
    *   Fields added: **SBS Balance Statement E-Mail**, **BRQ Registration No.**, **BNK Payment Reference No.**
    *   Actions added: **BRQ Query from Business Register**
    *   **New > Purchase Order** option replaced with **Retail Purchase Order**, the action runs new document **LSC Retail Purchase Order**
    *   **New Document > Purchase Return Order** option replaced with **Retail Purchase Return Order**, the action runs new document **LSC Retail Purchase Return Order**

* **Pageextension 70404929 "BCS.LSC ItemCardExt"** extends **"LSC Retail Item Card"**
    *   Fields added: **PEX Package Excise Calculation**
    *   Actions added: **PEX Package Materials**

* **Pageextension 70404930 "BCS.LSC PostedSalesInvCardExt"** extends **"LSC Retail P. Sales Invoice"**
    *   Fields added: **BNK Payment Reference No.**

* **Pageextension 70404931 "BCS.LSC Sales Order"** extends **"LSC Retail Sales Order"**
    *   Fields added: **BNK Payment Reference No.**
    *   Actions added: **PPY Get Cust. Spec. Prepayment**
    *   **Navigate > Shipments** option opens **LSC Retail P. Sales Shipments** list
    *   **Navigate > Invoices** option opens **LSC Retail P. Sales Invoices** list

* **Pageextension 70404932 "BCS.LSC SalesHistSellToFb"** extends **"Sales Hist. Sell-to FactBox"**
    *   Tile **Ongoing Sales Orders** opens **LSC Retail Sales Order** list
    *   Tile **Ongoing Sales Return Orders** opens **LSC Retail Sales Ret.Order** list
    *   Tile **Posted Sales Shipments** opens **LSC Retail P. Sales Shipments** list
    *   Tile **Posted Sales Invoices** opens **LSC Retail P. Sales Invoices** list
    *   Tile **Posted Sales Return Receipts** opens **LSC Retail P. Ret.Receipt** list
    *   Tile **Posted Sales Credit Memos** opens **LSC Retail P. Sales Cr.M.** list

* **Pageextension 70404933 "BCS.LSC SalesHistBillToFb"** extends **"Sales Hist. Bill-to FactBox"**
    *   Tile **Orders** opens **LSC Retail Sales Order** list
    *   Tile **Return Orders** opens **LSC Retail Sales Ret.Order** list
    *   Tile **Posted Shipments** opens **LSC Retail P. Sales Shipments** list
    *   Tile **Posted Invoices** opens **LSC Retail P. Sales Invoices** list
    *   Tile **Post Return Receipts** opens **LSC Retail P. Ret.Receipt** list
    *   Tile **Post.Credit Memos** opens **LSC Retail P. Sales Cr.M.** list

* **Pageextension 70404934 "BCS.LSC Customer Stat.Factbox"** extends **"Customer Statistics FactBox"**
    *   **No.** opens **LSC Retail Customer Card**

* **Pageextension 70404935 "BCS.LSC Customer Det. Factbox"** extends **"Customer Details FactBox"**
    *   **No.** opens **LSC Retail Customer Card**

* **Pageextension 70404936 "BCS.LSC Vend. Hist.BuyFrom FB"** extends **"Vendor Hist. Buy-from FactBox"**
    *   Tile **Orders** opens **LSC Retail Purch.Ret.Order Lst**

* **Pageextension 70404937 "BCS.LSC Vend. Hist. PayTo FB"** extends **"Vendor Hist. Pay-to FactBox"**
    *   **No.** opens **LSC Retail Vendor Card**
    *   Tile **Orders** opens **LSC Retail Purch.Ret.Order Lst**

* **Pageextension 70404938 "BCS.LSC Purchase Line Factbox"** extends **"Purchase Line FactBox"**
    *   **No.** opens **LSC Retail Item Card**
   
* **Pageextension 70404939 "BCS.LSC Vendor Statistics FB"** extends **"Vendor Statistics FactBox"**
    *   **No.** opens **LSC Retail Vendor Card**

* **Pageextension 70404940 "BCS.LSC Vendor Details Factbox"** extends **"Vendor Details FactBox"**
    *   **No.** opens **LSC Retail Vendor Card**

* **Pageextension 70404941 "BCS.LSC Item Inventory FB"** extends **"LSC Item Inventory FactBox"**
    *   **No.** opens **LSC Retail Item Card**

* **Tableextension 70404925 "BCS.LSC Vat Entry"** extends **"VAT Entry"**
    *   Fields added: **CustLedg. Entry Descr.**
      
* **Codeunit 70404925 "BCS.LSC Management"** - used for setting up VAT reporting in **BCS Itera_LSC_EE_Country_App_xx.x.x.x.app**

* **Report 70404925 "BCS.LSC VAT Declar"** - used for VAT reporting in **BCS Itera_LSC_EE_Country_App_xx.x.x.x.app**

***Note!** The use of added fields and actions is described in user guides links specified above.*
<br><br>


### Contact Information
For more information and pricing please contact:  
[https://apps.itera.ee/docs/en-us/support](https://apps.itera.ee/docs/en-us/support)
