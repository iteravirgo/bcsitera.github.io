# Bidrento Interface for Business Central User Guide

Bidrento Interface enables the following:
- Get Customers from Bidrento
- Update Customer's info in Business Central
- Get Sales invoices from Bidrento


## Contents
- [Bidrento Installation](#bidrento-installation)
- [How to setup](#how-to-setup) 
  - [Setup](#setup)
  - [Setup customers](#setup-customers) 
  - [Setup Sales invoices number series](#setup-sales-invoices-number-series)
  - [Setup Dimensions in Moderan and BC](#setup-dimensions-in-Moderan-and-BC)
  - [Setup Payment Terms Code in Moderan and BC](#setup-payment-terms-code-in-Moderan-and-BC)
  - [Setup Accounting Codes in Moderan](#setup-accounting-codes-in-moderan) 
- [How to Get Customers or Vendors from Moderan](#how-to-get-customers-or-vendors-from-moderan) 
- [How to Get Invoices from Moderan](#how-to-get-invoices-from-moderan)
  - [Dimensions in the sales invoice header](#dimensions-in-the-sales-invoice-header)
  - [Job Queue](#job_queue)
  - [Periodization of Invoices](#periodization-of-invoices) 
- [How to Get Contacts from Moderan](#how-to-get-contacts-from-moderan)
- [How to Send Customer Balances to Moderan](#how-to-send-customer-balances-to-moderan) 
  
  <br/>
  

## Bidrento Installation
Open **Extension Management** and check if extension named ‘Bidrento’ is installed. If not, please find and install it from AppSource or contact BCS Itera AS.




## How to setup

### Setup

Open the page **Sales & Receivables Setup** and then the fast tab **Bidrento**. Plese fill the fields as following (mandatory fields marked with *):

|Field|Description|
|---|---|
|Bidrento Account Filter *|Specity the G/L account numbers to be sent to Bidrento. There those accounts are reported as articles| 
|New customer Template *|Specify the customer template to be used when creating a new customer imported from Bidrento| 
|Bidrento Invoice Rounding Account *|Set the G/L account number for rounding|
|Automatically Create Invoice Dimensions *|Choose Yes, if you want the Dimension Values for the Dimension specified in Bidrento to be generated automatically|
|Customer Registration No. Field |Choose which field is used for a Customer Business Registration No. in the Customer table|
|Invoice Payment Reference No.Field |Choose which field is used for a Payment Reference No. in the Invoice Header table|

  <br/>
 

 <br/>



<br/>





### Setup Sales invoices number series

**NB!** It is important that Sales invoices and Posted sales invoices use different number series.


### Setup Dimensions in Moderan and BC
To use dimensions, add the Accounting Code in the Bidrento invoices card. 



### Setup Payment Terms Code in Bidrento and BC
Describe the same Payment Terms Codes in Bidrento and in BC.

For example: 10 DAYS
If the Payment Terms codes ar the same in BC and in the Bidrento contract, the Invoice Due Date will be calculated based on this code.


### Setup Accounting Codes in Bidrento

In addition to mapping customers, services should be mapped. To do so, setup accounting codes in Bidrento.

Accounting code should be in format: “Type:No.:GeneralProductPostingGroup”

For example – G/L Account:6115:RENT

 <br/>

## How to Get Customers and Sales Invoices from Bidrento

**NB!** Before performing any data exchange between Business Central and Moderan, existing customers in Business Central and Moderan must be mapped. To do so, open **Customers** and fill in **Moderan ID** (located in **Invoicing** fasttab) for every customer which should be mapped.

To get customers or vendors from Moderan, run action **Moderan – Get Customers/Vendors**. Existing (mapped) customers or vendors will be updated, and new customers or vendors (who have a Registration No in Moderan) created.

The customers or vendors who do not have a Registration No. will be skipped.

If the customer has English as the invoicing language in Moderan, the Language code is also displayed on the BC customer card.

When new customers or vendors were created, review customer or vendor cards and fill in missing data like **Posting Groups**.

**Moderan – Get Customers/Vendors** can be setup to run automatically by using **Job Queue** functionality.

To do so, open **Job Queue Entries** and create new entry as:

|Field/Tab|Value/Description|
|-|-|
|Object Type to Run|Report|
|Object ID to Run|24007900|
|Recurrence|Indicate desired recurrence|

 <br/>


## How to Get Invoices from Moderan

To get invoices from Moderan, run action **Moderan – Get Invoices** and fill in the parameters as following:

|Field|Description|
|-|-|
|Period Start*|Choose period from which invoices will be retrieved|  
|Posting Date*|Enter Posting Date for the invoices|  
|Document Date*|Enter Document Date for the invoices|  
|Payment Terms Code|Select Payment Terms Code. This applies to invoices that do not have a payment term specified in Moderan|
|Customer Filter|If set, invoices of other customers will be skipped|  
|Invoice Type*|Choose **Rent** or **Costs** |  
|Cost Optional Filters*|Choose Distribution Sets |



![GetInvoices](GetInvoices.png)

After successful import, open **Sales Invoices.** Review, post and issue invoices. 
Separate invoices can be issued for one tenant if they are entered in Moderan as separate agreements.


If you run action **Moderan – Get Invoices** more than once for the same period and invoice type, then the following logic will apply:

|Invoice in Business Central|Explanation|
|-|-|
|Invoice does not exist|Import will create invoice|
|Invoice has not been posted|Import will update the invoice (delete old and create new)|
|Invoice has been posted|Import will skip invoice|


<br/>








