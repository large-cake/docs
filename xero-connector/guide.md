# Xero Connector #

## Cash Header ##

Following fields are populated for each cash header record:

1. Date - receipt date in the source system
1. Total - total amount on all cash lines, including VAT
1. SubTotal - total amount without VAT
1. TotalTax - total amount of VAT on all cash lines
1. Reference - unique identifier (ReceiptId) in the source system
1. Contact - client/contact in the source system
1. Type - either **SPEND** (for negative amounts) or **RECEIVE** (for positive or zero amounts)
1. Line Amount Types - either **INCLUSIVE** or **NOTAX** (for zero amounts)
1. Is Reconciled - always set to **NO**
1. Status - always set to **AUTHORISED**


### Cash Line ###

Following fields are populated for each cash line:

1. Description - unique reference (CashLineId) in the source system
1. Tax Amount - VAT on the line
1. Amount - total amount including VAT
1. Tax Type - either **OUTPUT2** (for positive amounts), **INPUT2** (for negative amounts) or **NONE** (for exempt or zero amounts).

### Bank ###

All cash transaction are recorded in **711** bank account.

## Contacts (Clients) ##

Contacts (or Clients as they are referred to in the source system) are linked using *ContactNumber* field in Xero. This field is used to store client id from the source system. During search if no 
match by ContactNumber is found, the contact will be created in Xero. This is the only scenario when contact data will be synchronised from the source system to Xero. 
Any subsequent changes to contact in the source system would not be reflected in Xero (contacts are only created once).

### Creating Contact ###

Following fields are populated during contact creation:

1. Customer - always set to *yes*
1. Name - first and last names
1. Account Number - client code in the source system
1. First Name
1. Last Name
1. Contact Number - client id in the source system
1. Address - see *Contact's Address* section

### Contact's Address ###

Single contact's address is synchronised to Xero during creation.

Following fields are brought from the source system during contact creation:

1. Address Line 1
1. Address Line 2
1. Address Line 3
1. City - town field in the source system
1. Country
1. Postal Code
1. Type - always set to **Street**.

## Terms ##

*Terms "**Xero**", "**Xero site**" and "**Xero API**" refer to the property and trademark of www.xero.com*.