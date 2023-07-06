# LiveCasino API endpoints
The LiveCasino service exposes 4 endpoints:

- `DELETE /aux-livecasino/api/v1/data/all`: Remove the cache
- `GET /aux-livecasino/api/v1/data/all`: Get all live casino data
- `GET /aux-livecasino/api/v1/data/{id}`: Get live casino data by live casino id
- `GET /aux-livecasino/api/v1/data/provider/{provider}`: Get live casino data by provider

The DTO response returned by the endpoints is built from a Protobuf file and has the following structure:
- **status**: String with the status of the request.
- **data**: List of data with the following fields:
  - **id**: String value with the internal id of the live casino game
  - **name**: String with the name of the live casino game
  - **provider**: String with the name of the provider
  - **tableType**: String with the type of the table of the game
  - **latestUpdateTS**: String with the timestamp fo the last update of the game 
  - **stakes**: Map with the different stakes of the live casino game
  - **slots**: Object with the information of the availability of the game
  - **betBehind**: Boolean to indicate if the bet is behind or not
  - **isOpen**: Boolean to indicate if the game is open or not
  - **openingHours**: Object with the information of the opening hours of the game (fullTime or not, opening, closing and timeZone)
  - **latestRouletteNumbers**: List of numbers for Roulette games (value and color)

For more information go to the OpenAPI doc link: [LiveCasino OpenAPI](https://gaming.leo-dev-common.lvg-tech.net/services/clients/swagger-ui/index.html?urls.primaryName=LiveCasino%20service)
