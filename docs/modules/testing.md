# LiveCasino Testing

The testing added in the project includes two kind of tests:
- **Unit tests**: There is a unit tests class to verify the isolated behavior of each of the components of the integration.
This includes tests for the Connectors, Converters, Enrichers, Services, Controllers, etc... 
- **Integration tests**: There is one IT per Provider integration which check the correct normalization of the data to the common LiveCasinoData object and
there is another IT for verifying the correct notification of the Kafka events for both the Static and Dynamic events to the corresponding external services.

There is a future plan to extend the coverage by adding tests in another level
such as API, Contract or E2E ... by following a common strategy and tools within the team processes.
