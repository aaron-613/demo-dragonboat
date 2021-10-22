# demo-dragonboat
A simple, fun JavaScript game that uses MQTT to have a dragon boat race
![Screenshot](https://github.com/aaron-613/demo-dragonboat/blob/master/gfx/screenshot.png "Screenshott")

## Instructions to Install
1. Load all the files onto a web server somewhere.
1. Update the credentials for the MQTT connection in the `lib/shared.js` file. Note that you must use a WebSocket connection, and it must be secure `wss://` if hosting on a web server with `https`
   * Sign up for a free Solace Cloud account if you want: https://cloud.solace.com
   * Use any of the MQTT test servers out there
1. Update the displayed URL for players by changing the variable near the top of the `index.html` page
   * For example: `sg.solace.com/db`
1. Then start a race by pointing your Presenter laptop to the full URL with at least _some additional_ URL parameter
   * For example: `http://sg.solace.com/db/index.html?aaron`
   * You will notice a "latency" timer displayed in the bottom corner. This indicates RTT to the MQTT broker and back. Lower numbers indicate more responsive interactions.
1. That will start the race... I always suggest going into Full-Screen mode (F11 on Windows) and reloading
1. Participants can now join the race (phone or laptop) using the URL displayed on the screen
1. When enough participants have joined, the Presenter clicks anywhere on the background to start the race
1. Participants are given a countdown, after which they simply have to click anywhere on the background, or tap their finger on the background if on a phone


## Want to just play?

It's already setup on my demo server.

- Point your (desktop) browser to https://sg.solace.com/db/index.html?UNIQUE-NAME-HERE
   - That browser is the "Race Controller"
   - Give your race a unique name, so you can make sure people join the right race
- Get your friends to use their phones/tablets to join the race. Goto https://sg.solace.com/db
- Once everyone joins, the Race Controller clicks anywhere on the background to start the race
- Tap your phone background as fast as you can once the race starts


## Licences

Check the LICENSE file
