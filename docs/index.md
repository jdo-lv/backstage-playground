# LiveCasino Service Overview
LiveCasino service is responsible for handling live casino table data.
It connects with every configured and enabled provider to start reading the live casino data of the different available games
in the lobbies to transform this data into the internal model so that the Frontend application can subscribe to and 
render it in the tiles of the games.

Following a high level block of the integration:
### High level block diagram 
<img src="assets/overview.jpg" width="700" height="600" />

### Framework
The application has been implemented using [Spring Web Flow](https://spring.io/projects/spring-webflow) to define different flow for processing data. In matter of performance (and future splitting) 
has been created multiple kind of flow, one of them is the common one and one flow per provider.

# Runtime
Aligned with the current status of the rest of the services in the Platform, the LiveCasino runtime is the Java Runtime version 17 (LTS).

