# Address Autocomplete
Address Autocomplete solution in Business Central enables the following: 
- Search for addresses as You type
- Fill address fields with selected aadress


## Setup
To use the solution, **Address Search Setup** must be opened and enabled.
  
  
|Field|Explanation|
|---|---| 
| Remove District from City Info | Removes estonian District from City Info (for example "Kesklinna linnaosa"). |
| Service Type | Select the service (Maa-amet or Google) to be used for address autocomplete.<br>Maa-Amet gazetteer service if free of charge and can search for addresses in Estonia.<br>Google maps can search for addresses globally and it's place autocomplete API pricing can be found <a href="https://mapsplatform.google.com/pricing/" target="_blank">here</a>.<br><br>Note! Service type can only be changed when solution is not enabled. |
| Search Result Count | Specifies the number of address suggestions returned. Default and recommended value is 5. <br><br>Note! Value is editable only for Maa-amet service. |
| API-Key | Specifies the Google Places API key.<br>This key can be obtained from Google after registering to use the service. |
| Language | Specifies language for Google address search results. For english enter "en" or for estonian enter "et".<br>Full list of <a href="https://developers.google.com/maps/faq#languagesupport" target="_blank">available languages</a>.|
  
  
#### Address search and autocomplete is supported on following pages:
- Customer Card
  - Ship-to Address
- Sales Quote
- Sales Order
- Sales Invoice
- Vendor Card
  - Order Address
- Location Card
- Contact Card
  - Contact Alt. Address Card
- Employee Card
  - Alternative Address Card
- Service Contract
- Service Order
- Service Quote
- Resource Card
  
  
---

For more information please contact BCS Itera AS:  
<a href="https://www.itera.ee/en/about-us/" target="_blank">www.itera.ee/en/about-us/</a>
