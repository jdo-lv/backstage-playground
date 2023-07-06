# LiveCasino Data model
The LiveCasino service stores the Static data in a table in the SQL database
and the Dynamic data in a Hazelcast cluster as explained in the Cache system section.

The model of the Static data looks like:

- **id**: Internal id composed like: providerName_tableId
- **externalId**: External id of the game
- **tableId**: Identifier of the table of the game
- **name**: Name of the game
- **provider**: Provider identifier of the game
- **gameType**: Type of the game: ROULETTE, BLACKJACK, ...
- **gameVariant**: Variant of the game
- **stakes**: List of stakes of each game. For each currency which is the max and min bet
- **openingHours**: Information about the opening hours of the game. If it is fullTime or not, opening and closing information and the timeZone
- **lastUpdated**: Timestamp of the last update of the Game

The key-value stored in Hazelcast for the DynamicData looks similar except that it also includes that specific dynamic piece of information:
- **open**: Indicates if the game is or not opened
- **privateTable**: Indicates if for a private table.
- **betBehind**: Indicates if the bet is behind which allow the player to tail another Blackjack player at the table.
- **handsPerPlayer**: Number of hands done by player
- **slots**: Number of slots available for a BlackJack game
- **rouletteNumber**: Current number of a Roulette game
