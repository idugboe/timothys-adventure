# Timothy's Adventure

A no-build, mobile-friendly 2D platformer prototype made with Phaser 3. The game runs directly in a modern browser and loads Phaser 3.80.1 from jsDelivr. No image or sound assets are required.

## Play

Open `index.html` with an internet connection. Touch controls are shown in-game. On desktop, move with the arrow keys or A/D and jump with Up, W, or Space. Reach the gold flag to advance through all three levels. Coins are worth 10 points and stomped enemies are worth 25. Best score is saved in localStorage.

## Controls and features

- Purple hero with a gold T mark, drawn into a generated canvas texture.
- Touch left, right, and jump controls, plus desktop keyboard controls.
- Patrolling enemies, stomp defeat, contact damage, spikes, and pits.
- Three editable level layouts in the `LEVELS` array near the top of `index.html`.
- Score, health, persistent best score, pause/restart/quit, game-over and victory screens.
- WebAudio-generated jump, coin, stomp, hurt, and victory effects with a mute toggle.
- Phaser Scale.FIT canvas sizing and no-page-scroll mobile layout.

## Editing levels

Each `LEVELS` entry has a name, world width, enemy speed, platform segments `[x, y, width]`, coin positions `[x, y]`, spike segments `[x, y, width]`, enemy patrols `[x, y, minX, maxX]`, and an exit `[x, y]`. Coordinates use the 960x540 game world. Extend the array with another level object to add a level.

## Notes

The game uses Phaser from a CDN, so the first load requires internet access. Audio starts after the first user gesture because browsers restrict autoplay. This is a browser prototype, not an Android APK; APK export is intentionally out of scope for this phase.
