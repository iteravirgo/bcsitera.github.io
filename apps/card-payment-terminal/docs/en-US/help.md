
# Card Payment Terminal - User Guide

## Setup
The app needs connection parameters for the card payment terminal. To do that. Users must use the Card Payment Terminal Setup page. The field's meanings are shown in the table.

| **Field name** | **Type** | **Length** | **Description** |
| --- | --- | --- | --- |
| **General**  |   |   |   |
| **Code** | Code | 10 | Cashier's designation |
| **Description** | Text | 50 | Description |
| **Active** | Boolean |   | Informative, specifies that the cash register is active |
| **Related Location Code** | Code | 10 | The associated warehouse designation, i.e. determines the location where the POS is located |
| **Cash Payment Method** | Text | 20 | Cash payment method designation |
| **Bank Card Payment Method** | Text | 20 | Card payment method designation |
| **Bank Payment Method** | Text | 20 | Bank transfer payment method designation |
|  **EFT Terminal** |   |   | Fields required for card payment interface connection |
| **Service Connection String** | Text | 250 | IP of the card payment terminal |
| **Service Port** | Code | 20 | Card payment terminal port |

## Imlementation
Based on codeunit 70467125 "BCSPOS Card Payment Terminal" or your own maded code unit.


### Contact Information
For more information and pricing please contact:  
[https://apps.itera.ee/docs/en-us/support](https://apps.itera.ee/docs/en-us/support)
