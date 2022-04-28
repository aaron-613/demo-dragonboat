# demo-dragonboat
A simple, fun JavaScript game that uses MQTT to have a dragon boat race
![Screenshot](https://github.com/aaron-613/demo-dragonboat/blob/master/gfx/screenshot.png "Screenshott")

## Instructions to Install
1. Load all the files onto a web server somewhere.
1. Update the credentials for the MQTT connection in the `lib/shared.js` file. Note that you must use a WebSocket connection.  If hosting on a website with `https`, the WebSocket connection must be secure `wss://` (cannot mix secure & non-secure).
   * Sign up for a free Solace Cloud account if you want: https://cloud.solace.com
   * Use any of the MQTT test servers out there, e.g.:
       * https://test.mosquitto.org
       * https://www.hivemq.com/public-mqtt-broker
       * https://www.emqx.com/en/mqtt/public-mqtt5-broker
1. Update the displayed URL for players by changing the variable near the top of the `index.html` page:
   * `  const URL_TO_DISPLAY = "sg.solace.com/db";`
1. Then start a race by pointing your Presenter/Controller laptop to the full URL with at least _some additional_ URL parameter
   * For example: `http://sg.solace.com/db?aaron`
   * Give the race a name, which is useful if there are multiple races happening concurrently
   * You will notice a "latency" timer displayed in the bottom corner. This indicates Round Trip Time (RTT) to the MQTT broker and back. Lower numbers indicate more responsive interactions.
1. That will start the meet... I always suggest going into Full-Screen mode (F11 on Windows) and reloading
1. Participants can now join the race (phone or laptop) using the URL displayed on the screen
1. When enough participants have joined, the Presenter clicks anywhere on the background to start the race
1. Participants are given a countdown, after which they simply have to click anywhere on the background, or tap their finger on the background if on a phone


## Want to just play?

It's already setup on my demo server.

- Point your (desktop) browser to `https://sg.solace.com/db?UNIQUE-NAME-HERE`
   - That browser is the "Race Controller"
   - Give your race a unique name, so you can make sure people join the right race
- Get your friends to use their phones/tablets to join the race. Goto https://sg.solace.com/db
- Once everyone joins, the Race Controller clicks anywhere on the background to start the race
- Tap your phone background as fast as you can once the race starts


## Event Portal Design

![Screenshot](https://github.com/aaron-613/demo-dragonboat/blob/master/pubsub+event-portal/2021-10-22T12-21-48.png "Screenshot")

Check out the [pubsub+event-portal](https://github.com/aaron-613/demo-dragonboat/tree/master/pubsub%2Bevent-portal) folder for two ways of visualizing the flow of events and request-reply messages for the game.  Also included are the Event Portal schemas you can import yourself to https://solace.com/products/portal


## Licences

Check the LICENSE file
