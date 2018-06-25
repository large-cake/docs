## General Notes (ref: GN) ##

Please review requested requirements below and provide us with feedback on each requested point. 

In some cases we would not be able to proceed with work/project until all requested requirements are fullfilled and confirmed by e-mail.

## Access Requirement (ref: AR) ##

Please arrange access to the servers of interest (see *Affected Servers* section). The access should allow us to connect to required SQL or application servers (or both). We do not have preferred way or software to connect to the system.

However, we have following preferences:

1. Unattended access (*ref: AR-1*).
1. Being able to access the system during both office and out-of-office hours (*ref: AR-2*).
1. The sessions to be "switchable", so that we can reconnect into the same session from different PC, without having to request new session credentials (*ref: AR-3*).
1. Any timeouts (screen locks, etc.) are configured to be off (*ref: AR-4*).

*Please inform us about any periods during which the access would not be available (system maintanence, etc.) (ref: AR-5).*

## Directory Requirement (ref: DR) ##

Single directory is required to store work files:

1. At least 5 GB of free space (*ref: DR-1*).
1. Accessible from both application and SQL server(s) (*ref: DR-2*).
1. Being covered by in-house backup procedures (*ref: DR-3*).

## Internet Access (ref: IA) ##

In some cases we might require to download/upload work files.

Please provide following:

1. Access credentials to the server, which has internet access (*ref: IA-1*).

Once we download required files they will be moved to the directory mentioned in *Directory Requirements* section. 

*Please note that no confidential information will be downloaded/uploaded to comply with GDPR and our internal security procedures.*

## Affected Servers (ref: AS) ##

Please provide following information:

SQL Servers:

1. All SQL Server(s) - if some databases of interest are run on different SQL Server instances, please let us know about all relevant SQL Server instances (*ref: AS-1*).

The application directories:

1. All servers that run the system and the locations of ***Deploy*** directory on each server (*ref: AS-2*).

*Please let us know about all test environments that are available* (*ref: AS-3*).

## SQL Server Access (ref: SSA) #

1. SQL Server Management Studio access credentials (*ref: SSA-1*).
1. Connection string credentials for programmatic access (*ref: SSA-2*).

*SQL Server accounts with **Windows Authentication** enabled are preferred, because we don't have to be provided with password (ref: SSA-3).*

The SQL Server account provided should have **db_owner** role for databases of interest. Database roles can be found in *Security Folder -> Login -> name of account -> Properties -> User Mapping* in SQL Server Management Studio (*ref: SSA-4*).

## Application Directory Access (ref: ADA) ##

Administrative permissions are required on all *Deploy* directories of the application in application server(s).

Permissions including:

1. Run or Execute (*ref: ADA-1*).
1. Copy (*ref: ADA-2*).
1. Modify (including Delete) (*ref: ADA-3*).

## Switching Off The Application (ref: SOTA) ##

We might require exclusive access to the application to perform required actions.

Either of the following scenarios will be requested:

1. SQL Server database and application directories (*ref: SOTA-1*).
1. Applications directories only (*ref: SOTA-2*).

When exclusive access to the application directories only is required, please arrange steps in *Notifying Users* section.

When exclusive access to database(s) is required, please follow steps in both *Notifying Users* and *Database Backup* sections.

## Notifying Users (ref: NU) ##

For some operations we might require the system to be turned off and not available to the users.

Please arrange following:

1. Notify users they **will not be able to access the system** during specified window (*ref: NU-1*).
1. Notify users they **will lose any unsaved work** if the system is not closed prior to the specified window (*ref: NU-2*).
1. Notify users they have to close the system before specified window (*ref: NU-3*).
1. Provide access to ***Computer Management -> Shared Folders -> Sessions -> clear all locks***, so that we can reset any session left open on all servers we require access to (*ref: NU-4*).
1. Send us confirmation that all users have been notified about scheduled window of work (*ref: NU-5*).

Right before the specified window of work begins:

1. Clear all locks related to the application (as stated above).

*Please note that if access to clear all locks is not provided, we might have to abandon and rescheduled specified window of work.*

## Database Backup (ref: DB) ##

During some operations we might require database backups done outside of main backup schedule.

We require following:

1. Inform us about existing database backup schedule(s): the exact time operation is performed on each database of interest and the location of backups (*ref: DB-1*).
1. Schedule additional backups on our request (*ref: DB-2*).
1. Provide us with required access credentials and the ability to restore database(s) (*ref: DB-3*).
1. Inform us about any steps required to be performed post restore (*ref: DB-4*).
1. Inform us about the type of backups: incremental/full with transaction logs or without (*ref: DB-5*).

Once additional backups are arranged:

1. Inform us about approximate time backup is likely to complete. In some cases full database backups can take long time to complete, so please let us know when they are normally completed by (*ref: DB-6*).
1. The exact name and location of backup taken or scheduled (*ref: DB-7*).

Please ensure that there is enough space to complete requested backups. If full backups are requested or done during existing backup schedule, please inform us:

1. How many backups can be done before requesting additional storage (*ref: DB-8*).

## Document Storage (ref: DS) ##

The free space storage requirement in *Directory Requirement* section is significantly increased when working with Document database.

We cannot estimate the exact storage required, because it depends on number and size of the files stored in Document database. 

The maximum required storage can be estimated by taking **the size of Document database and adding 5%** to it. For example, if total size of Document database is 100 GB, please provide us with at least 105 GB of free storage (*ref: DS-1*).

However, if the project/work involves only part of Document database, we can begin the project if relevant portion is allocated with condition that we might have to re-run some stages if we run out of space. For example, if the work affects only 20% of documents, we can begin the project when 25% (20% + 5% mentioned earlier) of storage space is provided (*ref: DS-2*).