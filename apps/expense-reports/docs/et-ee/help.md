# Kuluaruanded
Expense Reports solution in BC enables the following:

- Management of expense and travel reports
- Management of expense documents
- Digital archive of expense documents
- Connection to digitization partner <a href="https://costpocket.com/en" target="_blank">CostPocket.com</a>

## Settings
To use the solution, **Expense Reports Setup** must be opened and following fields filled:

|Field|Explanation|
|---|---| 
| Expense Document Nos. | For defining Expense document number series. Value can be chosen from **No. Series List**.|
| Expense Report Nos. | For defining Expense report number series. Value can be chosen from **No. Series List**.|
| Vendor Registration No. Field | Solution uses vendor registration number for automatic detection of Vendor. Since different country localisations use different fields for storing this data, we have made this value selectable by User. **This selection is recommended but NOT mandatory**.|

All expense documents are posted via journal and User can **select a Journal Template and Batch** for this. 

To use digitization partner **CostPocket** functionality, action **Registration** must be used for one time. User information in CostPocket registration form page is used to determine Primary user, who shall receive e-mail from CostPocket along with instructions how to use CostPocket app. After successful registration connection with CostPocket is established.  

For pretermined cost types User can setup default cost accounts. That can be done in **Cost Types** page. Now when expense documents are imported from CostPocket, system assigns a default G/L cost account determined by document's cost type.  

Solution is ment to be used with logic:  
User operates daily/weekly in CostPocket app, taking pictures of expense documents and adding them to an Expense report. Bookkeeper operates in BC, getting expense reports with connected expense documents from CostPocket.   
*For special cases where Expense reports are not used, User can mark **Allow Documents without Report**, which makes individual document posting possible.*

## Use
### Expense Reports

**Manual creation** of an expense report is usually done after manual creation of expense documents. User can add documents to report with action **Add documents to Report**.

Expense reports *(with status Report ready)* will be imported from CostPocket, when user presses button **Get Reports from CostPocket**.  Among with an expense report all expense documents, that are connected to this report, shall also be  imported to BC.  
On Expense report card User can see total sum of expense documents in LCY.  
User can edit submitter information by selecting value from Employees table to **Submitter No.** field. When selecting new value system asks if documents (report lines) should also be updated.  
User must set posting date for report and all connected expense documents by entering value to field **Posting Date**.  
User can open list of connected expense documents when clicking on **Number of Documents** field value.  
To **Post** an expense report means that all connected expense documents are posted. *Documents are posted individually.*  

Posted expense reports can be found in **Posted Expense Reports** archive.  

### Expense Documents

Manual creation of expense document is possible and is similar to regular purchase invoice.  

**Vendor and Submitter must be used**.  When getting documents from CostPocket system looks for Vendor Registration No. and/or VAT Registration No. in order to find Vendor from Vendors. Similarly submitter e-mail is used to look for Employee with matching company Email from Employees.  
User can make multiple document lines with different posting groups (to manage VAT).    
**Dimensions** are applied for header only.  
Only .jpg type attachments can be uploaded.
Expense document's **Billing Type** can be Personal or Company, depending on finances used.  
Currency exchange rate can be adjusted by **Currency Factor** field.  
User can work with documents on document card or in expense documents list *(mainly to assign Vendor/Submitter/Expense account)*.  
When an expense account is assigned to document header, User shall be prompted, if document lines should also be updated.  
User can check posting with action **Post Preview**.  
Solution will make posting entries to both Vendor ledger entries and Employee ledger entries *(when Submitter has paid for expense document using personal finances).*  

Documents are usually posted from Expense Report. *In special case, when Allow documents without reports selection is used, expense documents can be imported separately with action **Get Documents from CostPocket** and then a document can also be posted from Expense Document list/card.*

Posted expense documents can be found in **Posted Expense Documents** archive.  

---

For more information please contact BCS Itera AS:  
https://www.itera.ee
