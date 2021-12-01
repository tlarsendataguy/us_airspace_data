[Object catalog](https://github.com/tlarsen7572/us_airspace_data#object-catalog) / Airspace

## Class B, C, D, and E Airspace

Class B, C, D, and E airspace are controlled airspace in the United States, suited for different purposes:

* Class B airspace surrounds the busiest airports in the nations (e.g. Chicago O'Hare and Atlanta). Class B airspace is individually tailored to each airport and is designed to encompass all instrument procedures.
* Class C airspace surrounds airports that have a control tower, are serviced by radar approach control, and have a certain level of activity. Class C airspace generally resembles an upside-down wedding cake with standard dimensions, but can be individually tailored as needed.
* Class D airspace surrounds airports with an operational control tower. Class D airspace generally consists of a cylinder of airspace with a standard radius, but can be individually tailored.
* Class E airspace covers most of the United States, usually starting at 1,200 ft above the ground. While considered controlled airspace for IFR operations, VFR pilots are not required to be in communication with controllers while flying in Class E airspace.

Airspace is defined using 2 tables.

|Table          |Description|
|---------------|-----------|
|Airspace       |Information for each 'piece' of airspace, including its classification, bottom altitude, and top altitude|
|Airspace-Points|Each point of each shape for each 'piece' of airspace. Airspaces can be quite complex and consist of multiple polygons and/or holes. All of these details are in this table. For Alteryx users, a helper macro called 'Convert Airspace-Points to SpatialObj.yxmc' is provided in the root of the repository to convert this table to spatial objects.|
