# LS Central Estonian Country App – User Guide
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
**BCS Itera_LSC_EE_Country_App_xx.x.x.x.app** is a small app which adds Dynamics 365 Business Central Estonian localization functionality related data fields and actions to LS Central pages (metadata cards/lists and documents). It includes the following objects:

* **Pageextension 81100 "BCS.LSC CustomerListExt"** extends **"LSC Retail Customer List"**
    *   Fields added: **Registration No.**
    *   Actions added: **Update Data from Business Register**

* **Pageextension 81101 "BCS.LSC CustomerCardExt"** extends **"LSC Retail Customer Card"**
    *   Fields added: **Balance Statement E-Mail**, **Registration No.**, **Payment Reference No.**
    *   Actions added: **Query from Business Register**

* **Pageextension 81102 "BCS.LSC VendorListExt"** extends **"LSC Retail Vendor List"**
    *   Fields added: **Registration No.** 
    *   Actions added: **Update Data from Business Register** 

* **Pageextension 81103 "BCS.LSC VendorCardExt"** extends **"LSC Retail Vendor Card"**
    *   Fields added: **Balance Statement E-Mail**, Registration No.**, **Payment Reference No.**
    *   Actions added: **Query from Business Register**

* **Pageextension 81104 "BCS.LSC ItemCardExt"** extends **"LSC Retail Item Card"**
    *   Fields added: **Package Excise Calculation**
    *   Actions added: **Package Materials**

* **Pageextension 81105 "BCS.LSC PostedSalesInvCardExt"** extends **"LSC Retail P. Sales Invoice"**
    *   Fields added: **Payment Reference No.**

* **Pageextension 81106 "BCS.LSR Sales Order"** extends **"LSC Retail Sales Order"**
    *   Fields added: **Payment Reference No.**
    *   Actions added: **Get Cust. Spec. Prepayment**

* **Codeunit 81100 "BCS.LSR Management"** - used for setting up VAT reporting in **BCS Itera_LSC_EE_Country_App_xx.x.x.x.app**

* **Report 81100 "BCS.LSR VAT Declar"** - used for VAT reporting in **BCS Itera_LSC_EE_Country_App_xx.x.x.x.app**

***Note!** The use of added fields and actions is described in user guides links specified above.*
<br><br>


### Contact Information
For more information and pricing please contact:  
[https://apps.itera.ee/docs/en-us/support](https://apps.itera.ee/docs/en-us/support)
