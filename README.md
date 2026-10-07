# Final Buzzer Map

A mobile-first egress planner for fans leaving Madison Square Garden after a Knicks championship. Built for the Plug and Play × PMAI Hackathon, Challenge 2.

Open `index.html` in any browser. It's a single file with no build step, and all data is mocked.

## What it does
- **Destination + mode picker:** choose Upper West Side, Hoboken, Brooklyn, Long Island or Murray Hill, then walk, transit or drive.
- **Confidence-scored closures:** official alerts, social posts, photos and on-site reports are fused into one score per incident with a noisy-OR model that decays signals over time. Only incidents scoring ≥ 0.70 change your route. Rumors that an official source denies are marked debunked.
- **Station recommendation:** for transit, every candidate station (Penn 1/2/3 vs A/C/E, Moynihan, Herald Sq, Times Sq, 28 St, PATH 33rd/23rd) is scored as walk time around closures + forecast platform crowding + train time. Blocked stations show the reason.
- **Escape Window:** door-to-door time for each departure slot from now to +45 min. It recommends "wait N min, leave at X" when waiting gets you home sooner.
- **Time slider:** replay the hour after the buzzer, or preview the forecast.

## Mock data → real feeds
NYC Open Data street closures and 511NY · NYC DOT Traffic Speeds · MTA GTFS-Realtime · NJ Transit GTFS-RT · PATH realtime · NYC DOT traffic cameras (crowd counts) · Bluesky Jetstream (social) · NYPD, Notify NYC and Port Authority official accounts · Valhalla routing with avoid-areas.
