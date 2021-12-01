## Open access National Airspace System Resource (NASR) data

This project's goal is to provide NASR data files in an open and user-friendly format. The Federal Aviation Administration (FAA) provides NASR files on 28-day and 56-day cycles. These data files contain a wealth of information about the airspace of the USA, from airport and runway information to navigational aids and weather stations. The files are provided by the FAA in flat-formatted text and XML files. This project parses these files and uploads them into a publicly-accessible PostgreSQL database.

This project is not affiliated or endorsed by the FAA or any department of the US government. It is purely a hobbyist-supported project and should not be used for production systems. It is intended as an educational resource for those who have an interest in both aviation and data analysis.

### Data access

All of the parsed NASR data is provided in a publicly-accessible PostgreSQL database. The database can be accessed with the following connection parameters using the postgres ODBC driver:

```
Driver:    Use the Unicode driver; the ANSI driver will not be able to connect
Host:      ayx-data.postgres.database.azure.com
Post:      5432
Database:  nasr
Username:  nasr_access@ayx-data
Password:  f!5C$66eMxYC&^vz
SSL Mode:  Require
```

### Parsing and replication

The NASR and digital object files are parsed using Alteryx workflows. This repository contains the workflows used to parse and publish the NASR data to a PostgreSQL database hosted on Azure. To encourage an atmosphere of open collaboration, all workflows are provided under an MIT license.

### Object catalog

The following high-level objects are contained in the database, represented by 1 or more tables:

|Object                       |Description|
|-----------------------------|-----------|
|[AFF](/doc/AFF.md)           |Air Route Traffic Control Center (ARTCC) facilities and communications|
|[Airspace](/doc/Airspace.md) |Class B, C, D, and E Airspace|
|[APT](/doc/APT.md)           |Landing facilities (airports, heliports, ultralight aerodromes, etc)|
|[ARB](/doc/ARB.md)           |ARTCC boundary segments|
|[ATS](/doc/ATS.md)           |Air traffic service route airways|
|[AWOS](/doc/AWOS.md)         |Automated weather/surface observing systems|
|[AWY](/doc/AWY.md)           |Airways|
|[CDR](/doc/CDR.md)           |Coded departure routes|
|[DOF](/doc/DOF.md)           |Digital obstacle file|
|[FIX](/doc/FIX.md)           |Radio fixes / reporting points|
|[FSS](/doc/FSS.md)           |Flight service stations|
|[HPF](/doc/HPF.md)           |Holding patterns|
|[ILS](/doc/ILS.md)           |Instrument landing systems|
|[LID](/doc/LID.md)           |Location identifiers|
|[MAA](/doc/MAA.md)           |Miscellaneous activity areas|
|[MTR](/doc/MTR.md)           |Military training routes|
|[NAV](/doc/NAV.md)           |Navigational aids (NAVAIDS)|
|[PFR](/doc/PFR.md)           |Preferred routes|
|[PJA](/doc/PJA.md)           |Parachute jump areas|
|[STARDP](/doc/STARDP.md)     |Standard terminal arrivals (STAR) and standard departure procedures (DP)|
|SUA                          |Special use airspace (not current available)|
|[TWR](/doc/TWR.md)           |Terminal communications services (towered airports)|
|[WXL](/doc/WXL.md)           |Weather reporting locations|
