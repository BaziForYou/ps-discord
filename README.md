# ps-discord
ps-discord is an efficient queue system for FiveM that has discord integration with a priority system.

## Usage
### Installation
1. Grab the latest release from the releases tab.
2. Extract the files to your server resources folder.
3. Remove any other queue resources & hardcap.
4. Set up `queue/roles.lua` and `queue/card.lua` to your liking. See [Configuration](#configuration) for more information.
4. Set up the resource to your needs with the convars stated below.

### Configuration
You primarily configure the resource with the convars stated below. There however is two files you should edit to your liking.
That is `queue/roles.lua` and `queue/card.lua`, the first one determines which roles have access and their priority and the second one is the card that is displayed in the queue.

### Commands
| Command | Description |
| --- | --- |
| `clearWebhookStatus` | Clears the webhook status message id, in case you want/need to send a new one. |

### Convars
You only have to configure the convars that has `none` as default value. The rest is optional. These should be placed in the `server.cfg` file or a file loaded by it.
| Convar | Type | Default | Description |
| --- | --- | --- | --- |
| `set ps:discordDebug` | STRING | "false" | If you want debug prints in server console. |
| `set ps:discordAPIVersion` | INT | 10 | The Discord API Version you want to use (Recommended Version 10.) |
| `set ps:discordGuildId` | STRING | none | This is for your Discord Guild ID (Right-click Server Name in Dev Mode and Copy Server ID.) |
| `set ps:discordBotToken` | STRING | none | This is for your Discord Bot Token (Bot Token in Discord Developer Portal.) |
| `set ps:discordRequestsPerMinute` | INT | 30 | The Max Amount of Requests to the Discord API per minute (Recommended Amount is 30) |
| `set ps:displayQueueInHostname` | INT | 1 | If you want to display the queue in the hostname (1 = true, 0 = false) |
| `set ps:gracePeriod` | INT | 0 | The amount of time a player can be disconnected and join back to get upped queue priority (in seconds) (0 = disabled) |
| `set ps:ghostCheckInterval` | INT | 60 | The amount of time to check for ghost players (in seconds) |
| `set ps:webhookStatusMessage` | STRING | none | The webhook to send the status message to (leave blank to disable) |
| `ps:webhookStatusUpdateInterval` | INT | 30 | The amount of time to send the status message to the webhook (in seconds) (Defualt is 30) |
