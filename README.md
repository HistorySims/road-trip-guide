# Road trip guide

A single-page prototype that tells short stories about the places you drive past: history, geology, oddities, and the hometowns of your favorite artists. Music is the default. Stories slot into the gaps between songs, or cut in when something is in view.

## Put it on GitHub Pages

1. Create a repo (for example `roadside-radio`) and upload `index.html`.
2. In the repo, go to **Settings → Pages**, set Source to **Deploy from a branch**, pick `main` and `/ (root)`, and save.
3. After a minute it's live at `https://<your-username>.github.io/roadside-radio/`.

It has to be served over https for GPS, the wake lock and Spotify sign-in to work, so opening the file from your computer won't do.

## In the car

- Open the page in Safari on your phone and allow location when asked.
- Type a destination and tap **Plan route** if you want the strip of what's coming up. Leave it blank to free-roam.
- Tap **Drive with GPS**. The tap also unlocks the voice.
- Keep the screen on and the page in front. iPhone stops location updates when the screen locks or Safari goes to the background.
- Set it up before you pull out. It's built to run hands-free.

**Simulate** runs a drive at your desk. With no destination it uses the demo route picked next to the **Demo route** button: Port Chester to Phoenixville (I-287 and US-202) or White Plains to Cairo, NY (I-287, the Thruway and NY-32).

## Spotify (optional)

Needs Spotify Premium on the account that owns the developer app.

1. At [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard), create an app and tick **Web API**.
2. Add the Redirect URI shown in the page's settings, exactly as shown. Always open the page at that same address (with or without `index.html`, but the same one every time).
3. Paste the app's Client ID into the page and tap **Connect Spotify**.
4. Start music in the Spotify app before you drive.

With Spotify connected, the app pauses at the end of a song, tells the story, queues a song tied to the place, and skips to it. It also reads your top artists and looks up where they were born or formed, using Wikidata.

## Where the stories come from

- About 40 hand-written stories around Port Chester and along I-287 and US-202 to Phoenixville.
- Wikipedia articles with coordinates near your position and along the route, filtered and ranked by page views.
- Your top Spotify artists matched to hometowns through Wikidata.

## Known limits

- Routes come from the free OSRM demo server, which doesn't know about traffic. If you leave the planned route, the app notices and asks for a new one.
- Voices are the device's built-in text-to-speech. On iPhone, download an Enhanced or Premium voice under Settings → Accessibility → Spoken Content → Voices.
- Trigger points for the hand-written "in view" stories are approximate.
- The free routing, place-search and Wikipedia services are fine for personal testing, not for a public app with many users.
