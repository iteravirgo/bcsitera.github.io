---
---
##### Version 15.6.23045.0
- Added fields Country Code (visible) and Country Name (hidden by default) to Expense Report, in order to show country visited on travel report
- Added field Daily allowance entry description (hidden by default) to Expense Report, in order to makedaily allowance G/L entry description editable to user
- Fixed issue, that when changing amounts on expense document lines, then expense document amount on document header did not change immediately (user doesnt have to press F5 anymore)
- Fixed issue, that when expense document had expense type specified but no vendor, then after adding vendor user had to manually remove and reenter cost type in order for the predetermined G/L account to activate  

##### Version 15.6.22178.0
- Fixed situation where it was not possible to add attachments to Expense reports/documents
- Fixed error "The Workflow Event does not exist" that came when reports were imported from CostPocket

##### Version 15.6.22143.1
- It's now possible to add dimensions to expense document lines

##### Version 15.3.22091.0
- Fixed situation where it was possible to post expense report from expense report list without approving although approval workflow was enabled
- Smaller bugfixes and UX improvements

##### Version 15.3.22031.0
- Instead of fixed cost types now there are tree structured editable Expense types that can be synced with CostPocket
- Now You can prepare Expense Report in BC and send it to CostPocket (for adding digitized documents)
- Now You can take pictures of expense documents directly from BC
- Integration between BC and CostPocket now works with status flags - when getting reports and also marking received reports
- Now You can start creation of expense document directly from expense report
- Better prefiltering of G/L account selection
- Travel report fields (Start date and End date and Allowance) now appear only on reports with type Travel
- Fixed situation when adding documents from report didn't make connection between document line and report
- Smaller UX imporvements
