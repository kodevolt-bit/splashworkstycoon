# Splashworks Tycoon

An isometric water park tycoon game that runs in the browser. Build pools, slides and food stands on a beachfront plot, hire staff, set prices and keep your guests happy.

The game itself is one file, `index.html`. The other files are the background music, the home-screen icons and the app manifest. There is no build step and nothing to install.

## Play it

- **Locally:** download `index.html` and open it in any modern browser.
- **Online:** host it with GitHub Pages (see below).

## Goal

Reach **150 guests in the park at once** with a **park rating of 600** by **day 10**. After that the game carries on in sandbox mode.

## What you can build

**Pools & Slides:** Splash Pad, Lazy River, Wave Pool, Body Slide, Tube Twister, Freefall Drop, Kiddie Pool, Splash Fort, Lily Pad Walk, Diving Pool, Whitewater Rapids, Whirlpool Bowl, Boomerang Wall, Mat Racer, Surf Rider, Water Coaster, Aqua Loop, Family Raft Ride, Twin Racers, Bumper Boats, Splash Zip Line and Pirate Splash Ship.

**Slide Designer:** design your own slide square by square. You pick the tower, route, height, color and name, and the game works out its thrill rating, cost and upkeep.

**Food & Drink:** Snack Shack, Smoothie Hut, Ice Cream Cart, Pizza Oven, Taco Truck, Lemonade Stand, Shave Ice Shack and Funnel Cake Stand, plus sit-down restaurants with patio seating: Sushi Bar, Burger Grill, Noodle House and Smokehouse BBQ.

**Facilities:** Restrooms, Sunscreen Stand, Sun Loungers, Locker Room, First Aid, Cabanas, Outdoor Showers and ATM.

**Scenery:** palm trees, beach umbrellas, flower beds and trash cans.

**Staff:** lifeguards, janitors and mechanics.

## How the simulation works

- Guests get hungry and thirsty, need the restroom, get tired and slowly get sunburned. They walk to whatever meets the need, and they get unhappy if it's missing.
- Each guest has a thrill limit, and they skip rides that are too intense for them.
- Guests walk away if prices are too high. You set the price of each ride and stall and the park entry fee.
- Rides wear out and break down. Mechanics repair them.
- Water rides with no lifeguard nearby can have incidents.
- Litter builds up on paths. Janitors clean it and trash cans reduce it.
- The weather changes every day, and rain keeps visitors away.
- At closing, you pay staff wages, upkeep and loan interest, then get a day report.

## Controls

| Action | Mouse / keyboard | Touch |
|---|---|---|
| Pan | Drag, right-drag, or arrow keys / WASD | Drag (two fingers while placing paths) |
| Zoom | Scroll wheel or `+` / `-` | Pinch |
| Browse the build menu | Scroll wheel or the arrow buttons | Swipe the row of cards |
| Place | Click (drag for paths and scenery) | Tap to preview, tap again to build |
| Rotate before placing | `R` or the Rotate button | Rotate button |
| Stop building | `Esc` | Select tool |
| Pause / speed | `Space`, `1`, `2`, `3` | Speed buttons |
| Music on / off | `M` or the speaker button | Speaker button |

Click any guest, staff member or building to inspect it.

## Installing on an iPad or iPhone

Once the game is online (for example on GitHub Pages), open its address in **Safari**, tap the **Share** button, then choose **Add to Home Screen**. The Splashworks Tycoon icon appears on the home screen, and the game opens full screen without the browser bars, like an app.

The icon files are `apple-touch-icon.png` and the `icons/` folder. `manifest.webmanifest` gives the same icon and full-screen behavior on Android and desktop Chrome. To change the icon, replace those PNGs with images of the same sizes.

## Music

Background music: "Seratonin from the Sun" by RAGE, in `music/seratonin-from-the-sun.mp3`. It loops quietly and starts the first time the player taps or clicks, because browsers block sound until then. The speaker button in the top bar turns it on or off, and the game remembers that choice. Music pauses when the game is in the background.

To use a different song, replace that file with another MP3 of the same name.

## Saving

The game saves automatically to your browser's `localStorage` every 30 seconds and at the end of each day. Saves stay in the browser and on the device where you played. Clearing site data erases them.

## Publishing on GitHub Pages

1. Create a new repository on GitHub and upload everything in this folder to the root: `index.html`, `apple-touch-icon.png`, `manifest.webmanifest`, the `icons/` and `music/` folders and this `README.md`.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose `main` and `/ (root)`, then click **Save**.
4. After a minute or two the game will be live at `https://<your-username>.github.io/<repository-name>/`.

## Technical notes

- It's written in plain HTML, CSS and JavaScript and draws to a `<canvas>`. It doesn't use any frameworks or libraries.
- Opening `index.html` directly from your computer works, including the music.
- The only external request is to Google Fonts for the Lilita One and Nunito typefaces. If those can't load, the game falls back to system fonts.
- It works in current versions of Chrome, Edge, Firefox and Safari, on desktop and mobile.
