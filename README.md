const Hypixel = require('hypixel-js');
 
const client = new Hypixel({ key: 'xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx' });
 
// old school callbacks
client.getPlayerByUsername('Codies', (err, player) => {
  if (err) {
    return console.info('Nope!');
  }
  
  // or a Promise if no callback provided
  client.findGuildByPlayer(player.uuid)
     .then((guildId) => {
        ...
     })
     .catch((err) => {
        ...
     });
});