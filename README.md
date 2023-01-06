# Alert-Schema
GCN notices are machine-readable packets that are available in different formats, GCN classic over Kafka distributes in JSON format. For each event and instrument specific, different types of notices are available. Each type of notices contain different properties.

## Kafka notices
> Record type alert reporter contains the following information.

 Properties | Type | Description 
 --------------- | ----------- |----------------------  
 `mission` | string | Name of Mission or Telescope reporting the event 
 `instrument` | string | Name of the Instrument reporting the event
 `record_number` | number | Serial number spanning all the messages that come from the mission during a given trigger 
