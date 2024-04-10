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
* **Estonian Dynamics Partners Telema & Edisoft EDI** <br> User Guide: [https://dynamicspartnersee.github.io/apps/telema-edi/docs/en-US/help](https://dynamicspartnersee.github.io/apps/telema-edi/docs/en-US/help)
  
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
    *   Tab added: **BCS.LSC Telema EDI** with caption **Telema EDI** with fields added to this tab: **BCS.LSC Allow using Item No.**, **BCS.LSC Take Price from E-Order**, **BCS.LSC Require E-Receiving Advice**, **BCS.LSC Issue E-Order Response**, **BCS.LSC Issue E-Shipment**, **BCS.LSC Issue E-Invoice**, **BCS.LSC Price Round Prec on E-Inv**, **BCS.LSC DESADV Without Prices**, **BCS.LSC Send to Channel**, **BCS.LSC E-Doc. WebService AuthType**, **BCS.LSC E-Document Web Service URL**, **BCS.LSC E-Doc. Web Service User**, **BCS.LSC E-Doc. Web Service Key**, **BCS.LSC E-Doc. WebService Tenant**
      
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
    *  Tab added: **BCS.LSC Telema EDI** with caption **Telema EDI** with fields added to this tab: **BCS.LSC E-Ship. Creates Missing PO**, **BCS.LSC E-Inv Creates Miss. PO As**, **BCS.LSC Allow using Item No.**, **BCS.LSC Issue E-Receipt**, **BCS.LSC Send to Channel**, **BCS.LSC E-Doc. WebService AuthType**, **BCS.LSC E-Document Web Service URL**, **BCS.LSC E-Doc. Web Service User**, **BCS.LSC E-Doc. Web Service Key**, **BCS.LSC E-Doc. WebService Tenant**

* **Pageextension 70404929 "BCS.LSC ItemCardExt"** extends **"LSC Retail Item Card"**
    *   Fields added: **PEX Package Excise Calculation**
    *   Actions added: **PEX Package Materials**

* **Pageextension 70404930 "BCS.LSC PostedSalesInvCardExt"** extends **"LSC Retail P. Sales Invoice"**
    *   Fields added: **BNK Payment Reference No.**

* **Pageextension 70404931 "BCS.LSC Sales Order"** extends **"LSC Retail Sales Order"**
    *   Fields added: **BNK Payment Reference No.**, **BCS.LSC E-Receiving Advice Status**, **BCS.LSC Do Not Send as E-Document**
    *   Actions added: **PPY Get Cust. Spec. Prepayment**
    *   **Navigate > Shipments** option opens **LSC Retail P. Sales Shipments** list
    *   **Navigate > Invoices** option opens **LSC Retail P. Sales Invoices** list

* **Pageextension 70404932 "BCS.LSC SalesHistSellToFb"** extends **"Sales Hist. Sell-to FactBox"**
    *   Tile **Ongoing Sales Orders** opens **LSC Retail Sales Order List**
    *   Tile **Ongoing Sales Return Orders** opens **LSC Retail Sales Ret.Order Lst**
    *   Tile **Posted Sales Shipments** opens **LSC Retail P. Sales Shipments**
    *   Tile **Posted Sales Invoices** opens **LSC Retail P. Sales Invoices**
    *   Tile **Posted Sales Return Receipts** opens **LSC Retail P. Ret.Receipt List**
    *   Tile **Posted Sales Credit Memos** opens **LSC Retail P. Sales Cr.M. List**

* **Pageextension 70404933 "BCS.LSC SalesHistBillToFb"** extends **"Sales Hist. Bill-to FactBox"**
    *   Tile **Orders** opens **LSC Retail Sales Order List**
    *   Tile **Return Orders** opens **LSC Retail Sales Ret.Order Lst**
    *   Tile **Posted Shipments** opens **LSC Retail P. Sales Shipments**
    *   Tile **Posted Invoices** opens **LSC Retail P. Sales Invoices**
    *   Tile **Post Return Receipts** opens **LSC Retail P. Ret.Receipt List**
    *   Tile **Post.Credit Memos** opens **LSC Retail P. Sales Cr.M. List**

* **Pageextension 70404934 "BCS.LSC Customer Stat.Factbox"** extends **"Customer Statistics FactBox"**
    *   **No.** opens **LSC Retail Customer Card**

* **Pageextension 70404935 "BCS.LSC Customer Det. Factbox"** extends **"Customer Details FactBox"**
    *   **No.** opens **LSC Retail Customer Card**

* **Pageextension 70404936 "BCS.LSC Vend. Hist.BuyFrom FB"** extends **"Vendor Hist. Buy-from FactBox"**
    *   **No.** opens **LSC Retail Vendor Card**
    *   Tile **Orders** opens **LSC Retail Purch.Ret.Order Lst**
    *   Tile **Return Orders** opens **LSC Retail Purch.Ret.Order List**

* **Pageextension 70404937 "BCS.LSC Vend. Hist. PayTo FB"** extends **"Vendor Hist. Pay-to FactBox"**
    *   **No.** opens **LSC Retail Vendor Card**
    *   Tile **Orders** opens **LSC Retail Purch.Ret.Order Lst**
    *   Tile **Return Orders** opens **LSC Retail Purch.Ret.Order List**

* **Pageextension 70404938 "BCS.LSC Purchase Line Factbox"** extends **"Purchase Line FactBox"**
    *   **No.** opens **LSC Retail Item Card**
   
* **Pageextension 70404939 "BCS.LSC Vendor Statistics FB"** extends **"Vendor Statistics FactBox"**
    *   **No.** opens **LSC Retail Vendor Card**

* **Pageextension 70404940 "BCS.LSC Vendor Details Factbox"** extends **"Vendor Details FactBox"**
    *   **No.** opens **LSC Retail Vendor Card**

* **Pageextension 70404941 "BCS.LSC Item Inventory FB"** extends **"LSC Item Inventory FactBox"**
    *   **No.** opens **LSC Retail Item Card**
 
* **Pageextension 70404942 "BCS.LSC RetailSalesOrder List"** extends **"LSC Retail Sales Order List"**
    *   Fields added: **BCS.LSC E-Order No.**, **BCS.LSC E-Receiving Advice Status**

* **Pageextension 70404943 "BCS.LSC RetailSalesOrderSubp"** extends **"LSC Retail Sales Order Subpage"**
    *   Fields added: **BCS.LSC E-Rec. Adv. Quantity**, **BCS.LSC E-Rec Adv Price incl Disc**

* **Pageextension 70404944 "BCS.LSC RetailPurch.OrderStore"** extends **"LSC Retail Purch. Order Store"**
    *   Factbox added: **BCS.LSC PO E-Documents FactBox**

* **Pageextension 70404945 "BCS.LSC Retail Purchase Order"** extends **"LSC Retail Purchase Order"**
    *   Factbox added: **BCS.LSC PO E-Documents FactBox**

* **Pageextension 70404946 "BCS.LSC Outbound E-Documents"** extends **"TED Outbound E-Documents"**
    *   Actions added: **BCS.LSC Create POS E-Sales Transaction**

* **Pageextension 70404947 "BCS.LSC Retail P.SalesInvoices"** extends **"LSC Retail P. Sales Invoices"**
    *   Fields added: **BCS.LSC EDI Status**

* **Pageextension 70404948 "BCS.LSC RetailP.SalesShipments"** extends **"LSC Retail P. Sales Shipments"**
    *   Fields added: **BCS.LSC EDI Status**

* **Pageextension 70404949 "BCS.LSC RetailP.SalesCr.M.List"** extends **"LSC Retail P. Sales Cr.M. List"**
    *   Fields added: **BCS.LSC EDI Status**

* **Pageextension 70404950 "BCS.LSC StoreP.PurchRecpt.List"** extends **"LSC Store P. Purchase Rec.List"**
    *   Fields added: **BCS.LSC EDI Status**

* **Pageextension 70404951 "BCS.LSC Transaction Card"** extends **"LSC Transaction Card"**
    *   Fields added: **BCS.LSC Payment Reference No.**
    
* **Pageextension 70404952 "BCS.LSC Transaction Register"** extends **"LSC Transaction Register"**
    *   Fields added: **BCS.LSC EDI Status**
  
* **Tableextension 70404925 "BCS.LSC Vat Entry"** extends **"VAT Entry"**
    *   Fields added: **CustLedg. Entry Descr.**

* **Tableextension 70404926 "BCS.LSC Transaction Header"** extends **"LSC Transaction Header"**
    *   Fields added: **BCS.LSC Payment Reference No.**, **BCS.LSC EDI Status**, **BCS.LSC EDI Status Error**
      
* **Codeunit 70404925 "BCS.LSC Management"** - used for open pages and lists in **LSC Retail** pages and lists view, also new documents after converting or posting in **LSC Retail Document** page. Also used for **Telema E-document** sending/receiving process, **item recognizing by Barcode** as the first option and **recognizing the LSC POS Transactions** as invoices needs to be send as **Telema E-Document**.
    *   In **Sales Quote** document action **Sales-Quote to Order** opens created order in **LSC Retail Sales Order** document
    *   In **LSC Retail Sales Order** document after action **Post** Business Central offers to open Posted Sales Invoice, if choose YES, it opens this posted invoice in **LSC Retail P. Sales Invoice** document  

* **Codeunit 70404926 "BCS.LSC VAT Return Management"** - used for VAT reporting in **BCS Itera_LSC_EE_Country_App_xx.x.x.x.app**
    *   Supports use the **POS Receipt no** from **Transaction Register** that it arrives to **Cust. Ledger Enrty** and **VAT Ledger Entry** tables and shown as **Invoice No.** to **KMD VAT Report INF Line**

* **Codeunit 70404927 "BCS.LSC Single Instance Mgt."**

* **Reportextension 70404925 "BCS.LSC Create Outbound EDocs"** extends **"TED Create Outbound EDocuments"** - used for creating outbound E-Documents from BCS.LSC Transaction Header.
    
* **Enumextension 70404925 "BCS.LSC Outbound Document Type"** extends **"TED Outbound Document Type"**
    *   Value added: **BCS.LSC EDI Status**
  
***Note!** The use of added fields and actions is described in user guides links specified above.*
<br><br>


### Contact Information
For more information and pricing please contact:  
[https://apps.itera.ee/docs/en-us/support](https://apps.itera.ee/docs/en-us/support)
