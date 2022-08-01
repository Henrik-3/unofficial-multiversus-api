# unofficial-multiversus-api (v.1.0.0)
Unofficial Valorant API by using the Ingame API
<br>

<a href="https://discord.gg/X3GaVkX2YN" target="_blank"><img src="https://discordapp.com/api/guilds/704231681309278228/widget.png?style=banner2"/></a>

# Authentication and Rate Limits
All rate limits are the same for every endpoint, so in general you have 90 requests every minute. If you exceed rate limit you will get following JSON with 429 Status Code:

If you exceed rate limit you will get following JSON with 429 Status Code:
```json
{
  "status": 429,
  "errors": [
    {
      "message": "Rate Limited",
      "code": 0,
      "global": false
    }
  ]
}
```
The API uses a key based system, with the quarantee that you will receive an answer to your application within 24-48h.
You are can generate a key on the linked discord above. 

*You will also have to enter some details about your app, for example the usecase. I will ask you for this so i can make sure the API is not used in a bad way*

Rate Limits:
- Basic Key:
    - 90req/min
    - Suitable for: Private Discord Bots (Servers) | Websites
- Production Key:
    - Rate Limit you requested
    - Suitable for: Production Discord Bots | Websites
    - PLEASE MAKE SURE THAT YOU ALSO REQUEST AN OFFICIAL VALORANT API KEY AT RIOT TO GET RSO IF YOU HAVE A STATS FEATURE FOR EXAMPLE
    
# Error codes
Here are the error codes for the MultiVersus API that could come up. There will always be a more detailed explanation in the `details` field.
| Code | Description |
| ------------- | ------------- |
| 1 | Invalid API Key |
| 2 | Forbidden endpoint |
| 3 | Restricted endpoint |

# Status 403 - Forbidden
If you receive this status code, please ping me on the support discord or contact me over my mail or discord that are linked on the bottom of this page.

# Status
See the current status of the API here: https://status.henrikdev.xyz/

# Documentation
The full documentation for the API is not available yet, it will coming soon.

| Endpoint | Description | Parameter | Possible queries | 
| ------------- | ------------- | ------------- | ------------- | 
| /multiversus/v1/account/details/:name | Returns detailed information about the players stats and some util information | `name: Ingame Name` | ⛔ |
| /multiversus/v1/account/search/:name | Search for MultiVersus accounts/profiles | `name: Ingame Name` | ⛔ |
| /multiversus/v1/by-id/account/details/:id | Returns detailed information about the players stats and some util information by using his `account id`<br />(faster then name due to less requests) | `id: Player Account ID` | ⛔ |
| /multiversus/v1/match/:id | Detailed information about a match | `id: Match ID` | ⛔ |
| /multiversus/v1/matches/:name | Get the match list of a player | `name: Ingame Name` | `size: amount of results that should be fetched`<br />`page: Page number if you want to use pagination` |
| /multiversus/v1/by-id/matches/:id | Get the match list of a player by using his `account id` (faster then name due to less requests) | `id: Player Account ID` |`size: amount of results that should be fetched`<br />`page: Page number if you want to use pagination` |
| /multiversus/v1/leaderboard-placements/:mode/:name | Returns the players leaderboard placement and score | `mode: 1v1/2v2`<br />`name: Ingame Name` | ⛔ |
| /multiversus/v1/by-id/leaderboard-placements/:mode/:id | Returns the players leaderboard placement and score by using his `account id`<br />(faster then name due to less requests) | `mode: 1v1/2v2`<br />`id: Player Account ID` | ⛔ |
| /multiversus/v1/leaderboard/:mode | Get the first 25 leaderboard entries of the given mode | `mode: 1v1/2v2` | ⛔ |
  
# Projects using this API
- [MultiVersus DE - GforG](https://discord.gg/CjYvx6YqGQ) Stats System

# Wrapper
- Not available yet

# Legal
This API isn't endorsed by WB Games and doesn't reflect the views or opinions of WB Games or anyone officially involved in producing or managing WB Games properties. 

# WB Games
Hey, first of all i hope u know that this project is a try to enhance the developer community of MultiVersus and also recognize it as one. If u still have an issue with it, feel free to text me on Discord or something :D

# Contributors
Thanks to @brianbaldner, who helped me searching for the MultiVersus endpoints. 
Also check out his Tracker: https://www.multiversustracker.com/

# Other Stuff
Also would be happy if you give the project a star and give credit when you use it. If you wanna help me to pay the server instance (16€ per month) or want to support my work, you can help me via patreon: [Link](https://www.patreon.com/henrikdev).

If you have any questions write on Discord: Henrik3#1451 or on the support server or write me an email to contact@henrikdev.xyz. 
