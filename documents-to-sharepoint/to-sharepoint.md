# Documents #

## Concepts ##

All documents are versioned. Each version of the file is preserved in the it’s original form. Each version of the document has a set of metadata properties. Document has at least one version and would be assigned either against client or contact, optionally marked against combination of assignment code and assignment job and would have author and date created. Additional metadata properties can be included on request.

## Document Properties ##

* **DocumentId** - integer, unique identifier for a document (all versions of this document would have the same document id), link to source system.
* **Version** - integer, starting at 1, sequential.
* **Name** - string, the file name of current version without file extension.
* **Extension** - string, file extension including preceding "."
* **ClientCode** - string, unique identifier for a client
* **ContactFirstName** - string
* **ContactSurname** - string
* **AuthorFirstName** - string
* **AuthorSurname** - string
* **AuthorUniqueId** - string, unique username of the author in source system
* **DateCreated** - date created for this version of the document
* **AssignmentCode** - string, unique identifier of the assignment
* **AssignmentJob** - string, filing/category within the assignment

## Rules ##
1. Document is assigned either to client or contact, not both. So either ClientCode or combination of ContactFirstName and ContactSurname will be specified.
1. Document can have no AssignmentCode and no AssignmentJob.
1. AssignmentJob is always against existing AssignmentCode, it cannot exist without AssignmentCode.
1. AssignmentCode can exist without AssignmentJob.
1. At least one of three author fields (AuthorFirstName, AuthorSurname, AuthorUniqueId) would have information on author.
1. The uniquiness of AuthorUniqueId field is not guaranteed - it originates from the source system. 
1. If document is against contact either ContactFirstName or ContactSurname or both would be provided. 
1. The combination of ContactFirstName and ContactSurname is not unique.
1. ClientCode field uniquely identifies client in source system.
1. Versions of each document are sequential.

## Folder Structure ## 

```bash
to-sharepoint (top directory)
|
+-- directory with "ClientCode_AssignmentCode_AssignmentJob" or "ContactFirstName_ContactSurname_AssignmentCode_AssignmentJob" mask
    |
    +-- directory - version of the document
        |
        +-- metadata.json - contains metadata about current version
        +-- actualFile.file - actual file of current version       
```

**All spaces in second level directories are replaced with underscores*

**Version directory starts at 1, sequentially increasing - 2, 3, etc.*

## Exceptions ##

The format of exception file:

```
{
    “Description”: “the description of exception”,
    “Path”: “relative path to relevant folder/file”
}
```

Types:

1. Contact first name contains invalid character.
1. Contact surname contains invalid character.
1. Client code contains invalid character.
1. File name clashing with metadata file name.
1. Assignment code contains invalid character.
1. Assignment job contains invalid character.
1. Versions are not sequential.
1. No author's details.
1. Missing both client and contact information.