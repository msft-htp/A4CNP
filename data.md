#Data Lab and Workshop

##Introduction
An airline is modernizing their flight status and notification engine. Plane events (ACARS messages) are of two types:
1. OOOI Events -- These are actual events that are fired by the aircraft when the plane pushes off the gate (Out) takes off (Off) lands (On) and arrives at the gate (In).
1. Positional Events -- These are GPS events as the plane moves along its flight.

This data needs to be processed to service as series of downstream services. 
1. First is a real time update of flight arrival times for all flights that are in progress. This feeds status boards, websites, and operation. 
1. Next we need to record key events into a data warehouse for dashboarding and analysis.
1. We also need to bundle and store all this raw data for archival purposes and for the data science team.

We have already developed ML Models that can update the estimated arrival times based on 

##Tech Requirement
Data streams in through a series of processes into Azure Event Hubs (think Kafka, Kineseis Stream, Pub Sub). 

For the Near-Real-Time data we will pushing data into a Mongo DB that has a record for all "current" flights.
For the long term storage we will be updating a Presto DB with all completed flights and key events.


End Users

Questions
