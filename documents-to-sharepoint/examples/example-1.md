Example of 2 documents (1st has 4 versions, 2nd has 2).

```bash
to-sharepoint
|
+-- ABC123_Investigation_2010
    |
    +-- 1
        |
        +-- metadata.json
        +-- My First Crime Case.txt
+-- ABC123_Investigation_2012
    |
    +-- 2
        |
        +-- metadata.json
        +-- My First Crime Case and my analysis.txt
    +-- 3
        |
        +-- metadata.json
        +-- My First Crime Case and my analysis (1).txt
+-- ABC123_Investigation_2016
    |
    +-- 4
        |
        +-- metadata.json
        +-- My First Crime Case and my analysis - updated.txt
+-- DRR450_Medical_Records_2017
    |
    +-- 1
        |
        +-- Is Sherlock right.txt
        +-- metadata.json
+-- DRR450_Medical_Records_2018
    |
    +-- 2
        |
        +-- metadata.json
        +-- When is Sherlock right.txt
        
```

metadata.json for document 12003, version 1:

```
{
    "DocumentId": 12003,
    "Version": 1,
    "Name": "My First Crime Case",
    "Extension": ".txt",
    "ClientCode": "ABC123",
    "ContactFirstName": "",
    "ContactSurname": "",
    "AuthorFirstName": "Sherlock",
    "AuthorSurname": "Holmes",
    "AuthorUniqueId": "Sholmes",
    "DateCreated": "2010-12-31T23:59:59.743",
    "AssignmentCode": "Investigation",
    "AssignmentJob": "2010"
}
```
metadata.json for document 12003, version 2:

```
{
    "DocumentId": 12003,
    "Version": 2,
    "Name": "My First Crime Case and my analysis",
    "Extension": ".txt",
    "ClientCode": "ABC123",
    "ContactFirstName": "",
    "ContactSurname": "",
    "AuthorFirstName": "Sherlock",
    "AuthorSurname": "Holmes",
    "AuthorUniqueId": "Sholmes",
    "DateCreated": "2012-01-01T00:59:58.456",
    "AssignmentCode": "Investigation",
    "AssignmentJob": "2012"
}
```
metadata.json for document 12003, version 3:

```
{
    "DocumentId": 12003,
    "Version": 3,
    "Name": "My First Crime Case and my analysis (1)",
    "Extension": ".txt",
    "ClientCode": "ABC123",
    "ContactFirstName": "",
    "ContactSurname": "",
    "AuthorFirstName": "Sherlock",
    "AuthorSurname": "Holmes",
    "AuthorUniqueId": "Sholmes",
    "DateCreated": "2012-06-30T03:34:10.890",
    "AssignmentCode": "Investigation",
    "AssignmentJob": "2012"
}
```
metadata.json for document 12003, version 4:

```
{
    "DocumentId": 12003,
    "Version": 4,
    "Name": "My First Crime Case and my analysis - updated",
    "Extension": ".txt",
    "ClientCode": "ABC123",
    "ContactFirstName": "",
    "ContactSurname": "",
    "AuthorFirstName": "Sherlock",
    "AuthorSurname": "Holmes",
    "AuthorUniqueId": "Sholmes",
    "DateCreated": "2016-06-30T10:45:20.230",
    "AssignmentCode": "Investigation",
    "AssignmentJob": "2016"
}
```
metadata.json for document 56698, version 1:

```
{
    "DocumentId": 56698,
    "Version": 1,
    "Name": "Is Sherlock right",
    "Extension": ".txt",
    "ClientCode": "DRR450",
    "ContactFirstName": "",
    "ContactSurname": "",
    "AuthorFirstName": "John",
    "AuthorSurname": "Watson",
    "AuthorUniqueId": "Watsonj",
    "DateCreated": "2017-02-28T13:23:59.111",
    "AssignmentCode": "Medical Records",
    "AssignmentJob": "2017"
}
```
metadata.json for document 56698, version 2:

```
{
    "DocumentId": 56698,
    "Version": 2,
    "Name": "When is Sherlock right",
    "Extension": ".txt",
    "ClientCode": "DRR450",
    "ContactFirstName": "",
    "ContactSurname": "",
    "AuthorFirstName": "John",
    "AuthorSurname": "Watson",
    "AuthorUniqueId": "Watsonj",
    "DateCreated": "2018-01-31T22:20:01.780",
    "AssignmentCode": "Medical Records",
    "AssignmentJob": "2018"
}
```