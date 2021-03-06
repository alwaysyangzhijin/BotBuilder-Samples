# Authentication Bot Utilizing MS Graph

This bot has been created using [Microsoft Bot Framework](https://docs.microsoft.com/en-us/azure/bot-service/?view=azure-bot-service-4.0).

This sample uses the bot authentication capabilities of Azure Bot Service. In this sample we are assuming the OAuth 2 provider
is Azure Active Directory v2 (AADv2) and are utilizing the Microsoft Graph API to retrieve data about the
user. [Check here](https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-authentication?view=azure-bot-service-4.0&tabs=csharp) for information about getting an AADv2
application setup for use in Azure Bot Service.
The [scopes](https://developer.microsoft.com/en-us/graph/docs/concepts/permissions_reference) used in this sample are the following:
- `email`
- `Mail.Read`
- `Mail.Send.Shared`
- `openid`
- `profile`
- `User.Read`
- `User.ReadBasic.All`

## To try this sample
- Clone the repository
  ```bash
  git clone https://github.com/microsoft/botbuilder-samples.git
  ```
- In a terminal, navigate to samples/javascript_nodejs/24.bot-authentication-msgraph
  ```bash
  cd samples/javascript_nodejs/24.bot-authentication-msgraph
  ```
- [Optional] Update the .env file under samples/javascript_nodejs/24.bot-authentication-msgraph with your botFileSecret
    For Azure Bot Service bots, you can find the botFileSecret under application settings.
- Install modules
  ```bash
  npm i
  ```
- Update `authentication-msgraph.bot` with required configuration settings
  - App ID and Key for registered bots
- Update `CONNECTION_SETTING_NAME` in `bot.js` so the bot can perform OAuth calls through Azure Bot Service
- Run the sample
  ```bash
  npm start
  ```


## Testing the bot using Bot Framework Emulator
[Microsoft Bot Framework Emulator](https://github.com/microsoft/botframework-emulator) is a desktop application that allows bot developers to test and debug their bots on localhost or running remotely through a tunnel.

- Install the Bot Framework Emulator from [here](https://aka.ms/botframework-emulator)
- In Settings, enable `Use a sign-in verification code for OAuthCards` to receive the magic code

### Connect to bot using Bot Framework Emulator v4
- Launch Bot Framework Emulator
- File -> Open Bot Configuration and navigate to `samples/javascript_nodejs/24.bot-authentication-msgraph` folder
- Select `authentication-msgraph.bot` file

## Additional Resources

### Dependencies

- **[Restify](http://restify.com)** Used to host the web service for the bot, and for making REST calls
- **[dotenv](https://github.com/motdotla/dotenv)** Used to manage environmental variables

### Configuring the bot

Update `.env` with the appropriate keys:

- App ID and Key for registered bots.
- botFilePath and botFileSecret from `authentication-msgraph.bot` file

## Further Reading
- [Azure Bot Service](https://docs.microsoft.com/en-us/azure/bot-service/bot-service-overview-introduction?view=azure-bot-service-4.0)
- [MS Graph Docs](https://developer.microsoft.com/en-us/graph/docs/concepts/overview) and [SDK](https://github.com/microsoftgraph/msgraph-sdk-javascript)