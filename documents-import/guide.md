# Documents #

## Concepts ##

All documents are versioned. Each version of the file is preserved in the it’s original form. Each version of the document has a set of metadata properties. Document has at least one version and would be assigned either against client or contact, optionally marked against combination of assignment code and assignment job and would have author and date created. Additional metadata properties can be included on request.

## Document Properties ##

* **DocumentId** - integer, unique identifier for a document (all versions of this document would have the same document id), link to source system.
* **Version** - integer, starting at 1, sequential.
* **Name** - string, the name of the document.
* **Extension** - string, file extension including preceding "."
* **ClientCode** - string, unique identifier for a client
* **ContactLastName** - string, optional last name of contact.
* **AuthorFirstName** - string.
* **AuthorSurname** - string.
* **AuthorUniqueId** - string, unique username of the author in source system.
* **DateCreated** - date created for this document.
* **CompanyName** - string.
* **DepartmentName** - string.
* **OfficeName** - string.
* **Description** - string.
* **Comments** - string.
* **DocumentDate** - date, optional.
* **VersionFileName** - the file name of current version.
* **DocumentLibraryName** - string.
* **DocumentSourceDescription** - string.
* **DocumentTypeName** - string.
* **AssignmentName** - string.
* **AssignmentCode** - string.
* **AssignmentNameRight** - string.
* **AssignmentCodeRight** - string.
* **AssignmentTypeDescription** - string.
* **AssignmentCentreCode** - string.
* **AssignmentNominalCode** - string.
* **ScheduleName** - string, filing/category within the assignment
* **ScheduleStartDate** - date, optional.
* **ScheduleEndDate** - date, optional.

## Rules ##
1. When **DocumentLibraryName** isn't specified, default value will be used.
1. When **DocumentSourceDescription** isn't specified, default value will be used.
1. **Document store location** is obtained using office.
1. When **DocumentTypeName** isn't specified, default value will be used.
1. **Author** is matched using **first and last names**.
1. When author cannot be matched, default value will be used.
1. When **AssignmentNameRight** isn't specified, default value will be used.
1. When **AssignmentCodeRight** isn't specified, default value will be used.
1. When **AssignmentName** isn't specified, it will be constructed using following pattern: "**ContactLastName/AssignmentNameRight**". If **ContactLastName** isn't available, default value will be used.
1. When **AssignmentCode** isn't specified, it will be constructed using following pattern: "**ClientCode/AssignmentCodeRight**".
1. When **AssignmentCentreCode** isn't specified, default value will be used.
1. When **AssignmentNominalCode** code isn't specified, default value will be used.
1. When **AssignmentTypeDescription** isn't specified, default value will be used.
1. When **ScheduleName** isn't specified, default value will be used.
1. When **ScheduleStartDate** isn't specified, default value will be used.
1. When **ScheduleEndDate** isn't specified, default value will be used.
1. Single date (using the same timestamp) will be used as **UploadDate**.

### Examples of Default Values ###

In reference to *Rules* section, following default values can be used:

Rule-1. Default value is "**Client**".

Rule-2. Default value is "**Import**".

Rule-4. Default value is "**Pending**".

Rule-6. Default values are "**- -unspec**" as first name and "**-unspec**" as last name.

Rule-7. Default value is "**Administration**".

Rule-8. Default value is "**Adm**".

Rule-9. Default value for **ContactLastName** is "**Holding client**".

Rule-11. Default value is "**-unspec-**".

Rule-12. Default value is "**001**".

Rule-13. Default value is "**Administration**".

Rule-14. Default value is the year of date created. For example, **"2010", "2011", "2012", etc.**

Rule-15. Default value is **no date (null)**.

Rule-16. Default value is **no date (null)**.