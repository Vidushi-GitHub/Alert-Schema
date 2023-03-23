# Fermi LAT Schema
GCN notices are machine-readable packets that are available in different formats; text, binary, and VOEvent. For each event and instrument-specific, different types of notices are available. Each type of notice contains different properties.

In this example, Fermi-LAT GCN notice is used as a text file, then schema and example are created as following steps:
(1) Read from the Fermi LAT GCN notice from the URL: https://gcn.gsfc.nasa.gov/fermi_lat_mon_trans.html
(2) Convert the notice into json example file; fermi_lat_example.json
(3) Obtain the JSON schema as fermi_lat_schema.json from the provided JSON example file using genson 
(4) Validate the schema example against the JSON schema using Draft7Validator

## Kafka notices
> Record type alert reporter contains the following information.

 Properties | Type | Description 
 --------------- | ----------- |----------------------  
 `mission` | string | Name of Mission or Telescope reporting the event 
 `instrument` | string | Name of the Instrument reporting the event
 `record_number` | number | Serial number spanning all the messages that come from the mission during a given trigger 
