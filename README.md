# CODPM-API-Discord

A simple JavaScript script to parse the [cod.pm](https://api.cod.pm) API and display formatted text in a Discord channel via the Discord [webhook](https://discord.com/developers/docs/resources/webhook) API.

# Screenshots

![ANSI sample](https://raw.githubusercontent.com/cato-a/CODPM-API-Discord/main/Sample-ANSI.png "ANSI colored masterlist")

<br>

![Bordered sample](https://raw.githubusercontent.com/cato-a/CODPM-API-Discord/main/Sample-Bordered.png "Unicode bordered masterlist")

# Configuration

The configuration variables are at the top of the JavaScript file.

Adjust the `DISCORD_WEBHOOK` variable and add the correct ID, TOKEN for the Webhook.

```plaintext
const DISCORD_WEBHOOK = new WebhookClient({ id: "<id>", token: "<token>" });
```

# Running the script

**Option 1)** Via NodeJS directly.

```plaintext
node CODPM-API-Discord.js
```

**Option 2)** Via a NodeJS Docker container.

```plaintext
docker run --detach --name CODPM-API-Discord -e 'NODE_ENV=production' -v "$PWD/CODPM-API-Discord.js":/usr/src/app/run.js -w /usr/src/app node:current-alpine node run.js
```