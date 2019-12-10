# demo-dragonboat
A simple, fun JavaScript game that uses MQTT to have a dragon boat race
![Screenshot](https://github.com/aaron-613/demo-dragonboat/blob/master/gfx/screenshot.png "Screenshott")

# Instructions
1. Load all the files onto a web server somewhere.
1. Update the credentials for the MQTT connection in the "shared.js" file
   * Sign up for a free Solace Cloud account if you want: https://cloud.solace.com
   * Use any of the MQTT test servers out there
1. Update the displayed URL for players by changing the variable near the top of the `index.html` page
   * For example: `sg.solace.com/db`
1. Then start a race by pointing your Presenter laptop to the full URL with at least _some additional_ URL parameter
   * For example: `http://sg.solace.com/db/index.html?aaron`
   * You will notice a "latency" timer displayed in the bottom corner. This indicates RTT to the MQTT broker and back. Lower numbers indicate more responsive interactions.
1. That will start the race... I always suggest going into Full-Screen mode (F11 on Windows) and reloading
1. Participants can now join the race using the URL displayed on the screen
1. When enough participants have joined, the Presenter clicks anywhere on the background to start the race
1. Participants are given a countdown, after which they simply have to click anywhere on the background, or tap their finger on the background if on a phone

# Licences
There are a bunch of various licenses in the JavaScript libs I use.  I should check to make sure I can distribute them or whatever.

