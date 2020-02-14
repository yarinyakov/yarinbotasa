# yarinbot
 
const Discord = require('discord.js');
const client = new Discord.Client();
client.login('your token');

var request = require('request');
var mcCommand = '/minecraft'; // Command for triggering
var mcIP = 'const Discord = require('discord.js');
const client = new Discord.Client();
client.login('your token');

var request = require('request');
var mcCommand = '/minecraft'; // Command for triggering
var mcIP = 'yarin_yakov.aternos.me
'; // Your MC server IP or hostname address
var mcPort = 25565; // Your MC server port (25565 is the default)

// IMPORTANT: You need to run "npm install request" (without quotes) in your terminal before executing this script

client.on('message', message => {
    if (message.content === mcCommand) {
        var url = 'http://mcapi.us/server/status?ip=' + mcIP + '&port=' + mcPort;
        request(url, function(err, response, body) {
            if(err) {
                console.log(err);
                return message.reply('Error getting Minecraft server status...');
            }
            body = JSON.parse(body);
            var status = 'Minecraft server is currently offline';
            if(body.online) {
                status = 'Minecraft server is online  -  ';
                if(body.players.now) {
                    status += '' + body.players.now + ' people are playing!';
                } else {
                    status += 'Nobody is playing!';
                }
            }
            message.reply(status);
        });
    }
})'; // Your MC server IP or hostname address
var mcPort = 25565; // Your MC server port (25565 is the default)

// IMPORTANT: You need to run "npm install request" (without quotes) in your terminal before executing this script

client.on('message', message => {
    if (message.content === mcCommand) {
        var url = 'http://mcapi.us/server/status?ip=' + mcIP + '&port=' + mcPort;
        request(url, function(err, response, body) {
            if(err) {
                console.log(err);
                return message.reply('Error getting Minecraft server status...');
            }
            body = JSON.parse(body);
            var status = 'Minecraft server is currently offline';
            if(body.online) {
                status = 'Minecraft server is online  -  ';
                if(body.players.now) {
                    status += '' + body.players.now + ' people are playing!';
                } else {
                    status += 'Nobody is playing!';
                }
            }
            message.reply(status);
        });
    }
});
