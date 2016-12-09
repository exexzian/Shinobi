# Shinobi

Shinobi is an Open Source CCTV software written in Node.JS

<img src="https://github.com/moeiscool/Shinobi/blob/master/web/libs/img/demo.jpg?raw=true">

# Why?

Most people probably first think of ZoneMinder when they look to open-source CCTV software. Frankly from my point of view zm has been nothing but a pain. It eats resources when it doesn't have to.

-MJPEG stream that are presented in the browser. They cannot be terminated without a hard refresh of the page... or by putting it in and iframe or popup as the writers of the zm community have done.

This method puts serious strain on the client browser. zm has caused countless browser crashes while just viewing multiple streams.

-It also by default records to JPEG.. if video formats are desired one must install bleeding edge or branches of the main software. Then being left with even less support and more of a mess than previous.

-zm has so many bugs and bounties many of them are just being left behind in the ocean of bugs reports.

# Shinobi is the solution to ZoneMinder's short comings.

- Written in a simple structure. `camera.js` and `web` folder.
- Easy Install. (not as easy as apt-get install zoneminder yet though. See below)
- Streams are `img` tags, but not MJPEG. Images are transferred through `WebSocket`.
- Any websocket enabled browser can support the image stream (including mobile)
- Interface is nicer to look at and works better in mobile.
    -- Client Side Tested on : 
    --- iPad Mini 2 - Safari and Chrome
    --- iPhone 5 - Safari and Chrome
    --- Windows 7 - Chrome
    --- Mac OS - Safari and Chrome

    - Server-Side Tested Successfully on:
    -- Ubuntu 16.04 (should work on any linux)
    -- Mac OS Sierra

# How to Install and Run

`For a Test deployment enviroment I suggest grabbing an old MacBook (what I did) and installing Node.JS on there. Open up Terminal to get started.`

Open `Terminal`.

Select directory `cd /your/directory/for/shinobi`. Where `camera.js` is located.

Setup `conf.json` with your SQL details. then go to `sql` and install the SQL files in your database. `Framework` then `Default Data`. Return to main directory.

with terminal while in the directory run `npm install` then to start `node camera.js`

to daemonize the process install pm2 with `npm install pm2 -g` then run `pm2 start camera.js`

open up `localhost` in your browser. Login with `ccio@m03.ca/password`.

run `pm2 logs` to see the console for any errors.

# To Do

-Organize this README

-Fix Pipe error that occasionally occurs

-better vieweing for saved events

-purging for old events (a cron script)

-better mobile support

# Donate

If you like what I am doing here and want me to continue please consider donating :)

Quick Links on the site page : https://moeiscool.github.io/Shinobi/

<a href='https://pledgie.com/campaigns/33051'><img alt='Click here to lend your support to: Shinobi, Open Source CCTV written in Node.js and make a donation at pledgie.com !' src='https://pledgie.com/campaigns/33051.png?skin_name=chrome' border='0' ></a>

PayPal : paypal@m03.ca

Patreon : https://patreon.com/moeiscool

Please note : donating directly through paypal will show more support :)

# Author

Moe Alam, just a guy who needed CCTV

# Want me to Host an Instance for you?
email me at : shinobi@m03.ca

    You would get:
    +50GB SSD
    +2GB RAM
    +Quad Core ARM Processor
    +200Mbps Default Throughput, Soft-Max 800Mbps Throughput per Server
    +Static IP
    +Location : Italy
    ----------
    $55/month

    Optional
    +1000GB = +$75/month

# Credits

If you wish to use this software for commercial purposes please consider donating :) If not.. including my name would be nice.

    Shinobi
    Copyright (C) 2016-2025 Moe Alam, moeiscool

    This program is free software; you can redistribute it and/or
    modify it under the terms of the GNU General Public License
    as published by the Free Software Foundation; either version 2
    of the License, or (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.