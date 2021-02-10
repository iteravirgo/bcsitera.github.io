# MCDS Connector - User Guide

MCDS (My Company Data Service) Connector allows to issue business transactions in XBRLGL format. Transactions can be issued to file or directly to the MCDS.

MCDS is a service that stores company's business transactions in XBRGL format and allows to forward transactions to justified parties.

Currently two types of transactions and parties are supported:
 - Sales Transactions which can be forwarded to e-invoice operator
 - Payroll Transactions which can be forwarded for reporting to Estonian Statistics

## Table of Contents
- [MCDS Connector - User Guide](#mcds-connector---user-guide)
  - [Table of Contents](#table-of-contents)
  - [Setup](#setup)
    - [MCDS Connector](#mcds-connector)
    - [Electronic Document Formats](#electronic-document-formats)
    - [Document Sending Profiles](#document-sending-profiles)
    - [G/L Accounts](#gl-accounts)
  - [Usage](#usage)
    - [Issue Sales Documents](#issue-sales-documents)
    - [Check Sales Document Status](#check-sales-document-status)

## Setup
### MCDS Connector
To enable MCDS connection, open MCDS Connector and fill in the following with information provided to you by MCDS operator:
Field | Description
-- | --
Service URL | 
Device Certificate Filename | upload the certificate file provided by MCDS operator
Device Certificate Password | 
Click **Test Connection** to validate connectivity.

### Electronic Document Formats
To enbale XBRLGL as format open **Electronic Document Formats** and ensure that following format has been setup:
Field | Value
-- | --
Code | MCDS-XBRLGL
Description | XBRLGL format for MCDS
Usage | Sales Invoice
Codeunit ID | 70466925
Delivery Codeunit ID | 70466927

### Document Sending Profiles
To prepare MCDS as a document sending profile for the customers open **Document Sending Profiles** and create new profile as following:
Field | Value
-- | --
Code | MCDS
Description | My Company Data Service
Electronic Document | Through Document Exchange Service
Format | MCDS-XBRLGL
Assign this profile to the customers who's sales documents should be sent to MCDS.

### G/L Accounts
In XBRLGL format Et-Gaap accounts are used instead of company's internal chart of accounts. 

Open **Chart of Accounts** and assign **Account et-gaap Category** for every account that will be used in business transactions forwarded to MCDS.

## Usage
### Issue Sales Documents
To issue sales doument as XBRLGL transaction either use action **Post and Send** on sales document or use action **Send** on posted sales docuemnt.

Choose the sending options either to save the XBRLGL document to a file or to send to MCDS:

Field | Value | Usage
-- | -- | --
Disk | Electronic Document | to save to file
Electronic Document | Through Document Exchange Service | to send to MCDS
Format | MCDS-XBRLGL | 
Click **OK** to send the document.

In case of MCDS, if sending was successful, field **MCDS Status** gets value 'Validation' indicating that MCDS has received the document and it is being validated against the XBRLGL schema and MCDS business rules.

### Check Sales Document Status
After sales document has been sent to MCDS, its status in MCDS can be checked by running the action **MCDS Check Status**.

There are two types of statuses which may get to be updated as following:

Field/Value | Description
-- | -- 
**MCDS Status:**  | 
'Valid'  | Transaction is valid and stored in MCDS.
'Not Valid' | Transaction is invalid and not stored in MCDS.
**MCDS E-invoice Status:** | 
'Transmitted' | Indicates invoice has been received by the e-invoice operator for delivering to the buyer.
To investigate status updates in more detail (for troubleshooting) open document **Activity Log**. To see the techical details of the particular communication log entry, you can click **View Details**.