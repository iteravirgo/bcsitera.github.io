# Expense Reports
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
| Vendor Registration No. Field | Solution uses vendor registration number for automatic detection of Vendor. Since different country localisations use different fields for storing this data, we have made this value selectable by User.|

All expense documents are posted via journal and User can **select a Journal template and Batch** for this. 

To use digitization partner **CostPocket** functionality, action **Registration** must be used. User information in CostPocket registration form page is used to determine Primary user, who shall receive e-mail from CostPocket along with instructions how to use CostPocket app. After successful registration connection with CostPocket is established.

For pretermined cost types User can setup default cost accounts. That can be done in **Cost Types** page. Now when expense documents are imported from CostPocket system assigns a default G/L account determined by document cost type.

Solution is ment to be used with logic:  
User operates daily/weekly in CostPocket app, taking pictures of expense documents and combining them to form an Expense report. Bookkeeper operates in BC, getting expense reports with connected expense documents from CostPocket to BC.   
For special cases where Expense reports are not used, User can mark **Allow Documents without Report**, which makes individual document posting possible.
