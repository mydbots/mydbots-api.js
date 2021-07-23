# myDbots.js

<a href="https://myDbots.ml/discord" target="_blank"><img src="https://img.devsforum.net/tr/img/h1Z2X3.png" alt="Join our discord" width="256"></a><br>
**Support:** [https://myDbots.ml/discord](https://myDbots.ml/discord) <br>
**NPM:** [npmjs.com/package/mybots-api.js](https://www.npmjs.com/package/mybots-api.js)<br>

## Installation

_If you have trouble with the installation, please feel free to visit our [discord](https://myDbots.ml/discord)._

- `npm i mybots-api.js`

# Define Module & Client

```js
const Discord = require("discord.js");
const client = new Discord.Client();
const myDbots = require("mybots-api.js");
const dbl = new myDbots("myDbots Token", client);

client.login("Discord Bot Token");
```

# Server Count & Shard Count Posting

```js
client.on("ready", async () => {
  dbl.serverCount();
  /* 
  -> Server count posted. 
  or 
  -> Server count & shard count posted.
  */
});
```

# Vote Checking

```js
let hasVote = await dbl.hasVoted("485716273901338634"); // -> User ID
if (hasVote === true) {
  console.log("Voted");
} else {
  console.log("Vote please.");
}
// -> Vote please.
```

# Search on vCodes

```js
let botFind = await dbl.search("742738378445029387");
console.log(botFind.username); // -> EcoBot
```
