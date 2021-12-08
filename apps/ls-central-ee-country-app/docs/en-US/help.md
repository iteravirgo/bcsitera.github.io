# LS Central Estonian Country App – User Guide
LS Central Estonian Country App extends Dynamics 365 Business Central Estonian localization functionality related data fields and actions to LS Central pages (metadata cards/lists and documents).

## Setup
There is no special setup needed for LS Central Estonian Country App. Installation and configuration (according to User Guide linkes provided below) of the following Dynamics 365 Business Central Estonian localization apps is a prerequisite for using LS Central Estonian Country App:
* Estonian Dynamics Partners Estonian Language (Estonia) – Estonian translations for Business Central W1 version. User Guide: [https://dynamicspartnersee.github.io/apps/estonian-language/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-language/docs/en-US/help)
* Estonian Dynamics Partners Balance Statements – User Guide: [https://dynamicspartnersee.github.io/apps/balance-statements/docs/en-US/app](https://dynamicspartnersee.github.io/apps/balance-statements/docs/en-US/app) 
* Estonian Dynamics Partners Business Register localization for Estonia – User Guide: [https://dynamicspartnersee.github.io/apps/estonian-business-register/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-business-register/docs/en-US/help)
* Estonian Dynamics Partners Banking Formats localization for Estonia – User Guide: [https://dynamicspartnersee.github.io/apps/estonian-banking-formats/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-banking-formats/docs/en-US/help)
* Estonian Dynamics Partners Intrastat Reporting localization for Estonia – User Guide: [https://dynamicspartnersee.github.io/apps/estonian-intrastat-reporting/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-intrastat-reporting/docs/en-US/help)
* Estonian Dynamics Partners Package Excise localization for Estonia – User Guide: [https://dynamicspartnersee.github.io/apps/estonian-package-excise/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-package-excise/docs/en-US/help)
* Estonian Dynamics Partners Prepayment Management – User Guide: [https://dynamicspartnersee.github.io/apps/prepayment-management/docs/en-US/help](https://dynamicspartnersee.github.io/apps/prepayment-management/docs/en-US/help)
* Estonian Dynamics Partners VAT Reporting localization for Estonia – User Guide: [https://dynamicspartnersee.github.io/apps/estonian-vat-reporting/docs/en-US/help](https://dynamicspartnersee.github.io/apps/estonian-vat-reporting/docs/en-US/help)


### Technical detail about LS Central Estonian Country App
BCS Itera_LSC_EE_Country_App_xx.x.x.x.app is a small app which adds Dynamics 365 Business Central Estonian localization functionality related data fields and actions to LS Central pages (metadata cards/lists and documents). It includes the following objects:
* Pageextension 81100 "BCS.LSC CustomerListExt" extends "Retail Customer List"
* Pageextension 81101 "BCS.LSC CustomerCardExt" extends "Retail Customer Card"
* Pageextension 81102 "BCS.LSC VendorListExt" extends "Retail Vendor List"
* Pageextension 81103 "BCS.LSC VendorCardExt" extends "Retail Vendor Card"
* Pageextension 81104 "BCS.LSC ItemCardExt" extends "Retail Item Card"
* Pageextension 81105 "BCS.LSC PostedSalesInvCardExt" extends "Retail Posted Sales Invoice"
* Pageextension 81106 "BCS.LSR Sales Order" extends "Retail Sales Order"
* Codeunit 81100 "BCS.LSR Management"
* Peport 81100 "BCS.LSR VAT Declar"



### Contact Information
For more information and pricing please contact:  
[https://apps.itera.ee/docs/en-us/support](https://apps.itera.ee/docs/en-us/support)
