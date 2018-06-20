# Invoice Distribution #

## Accounts Payable ##

Invoice Distribution uses “Accounts payable” relationship to obtain contact/client details (the recipient's e-mail address).

If you do not currently use this relationship, please configure it and apply to clients you would like to distribute invoices to.

Contacts, that act as accounts payable for clients, need to have primary e-mails specified.

Any invoices for clients that either do not have accounts payable relationship and no primary e-mail address configured in contact that acts as accounts payable for that client, would be skipped by Invoice Distribution.

Please note that following configuration is required:

* **Client A "has accounts payable" contact B**

or
* **Contact B "is an accounts payable of" client A**

## Extra Field ##

Invoice Distribution uses "DistributionType" extra field.

Please configure this extra field with following options and apply to relevant clients:

* Electronic
* Post

For e-mails please use **Electronic** extra value on client/contact.

## E-mail Address Rules ##

Invoice Distribution will use either **primary e-mail** for client/contact or **e-mail address of accounts payable** (see *Accounts Payable* section).

Following scenarios detail other combinations and which e-mail address will be used by Invoice Distribution:

1. Client with no accounts payable relationship - client's email address.
1. Client with accounts payable, but no e-mail address on the records for accounts payable - entries will be skipped.
1. Client without accounts payable relationship and no e-mail address - entries will be skipped.
1. Contact without e-mail address but with accounts payable, which doesn't have e-mail specified - entries will be skipped.
1. Client with accounts payable (a), who in turn also has an accounts payable (b) - e-mail address of accounts payable (a) will be used.