# Introduction
Trying to separate business logic from the provider and business logic of the application 
and performance the execution has been separated by two well differentiated flows
* Provider Flow
* Common Flow

# Provider Flow
The responsibility of this flow is to recollect data from the provider, process, transform
to the common contract and remove duplicates.
Also to avoid high amount of event has been implemented an accumulator that will only send
events each 5 secs, so in this way, all the events coming with the same data will be merged
and transform in only one unique event.

<img src="../../assets/provider-flow.jpg" />

# Main Flow
The main flow has the responsability of combine with previous events (in case of update),
store in DB, populate the cache and also calculate additional information as the connection
with the internal game through ES. Also is incharge of dispatch different events (dynamic/static)
if a change has been produced

<img src="../../assets/common-flow.jpg" />
