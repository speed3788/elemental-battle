# Elemental Battle 五行

A card battle game built on the five elements: Wood, Fire, Earth, Wind, and Water.
Play against the computer (Easy, Medium, or Hard) or against a friend online.

## Play

Open `index.html` in a browser, or visit the GitHub Pages link for this repository.

- **vs Computer:** type your name and pick a difficulty.
- **vs a friend:** one player presses **Host a game** and shares the 5-character code; the other types it into **Join game**.

## How to play

- Knock your opponent's health (30) to 0, or have more health after 15 rounds. A tie goes to overtime (round 16); a tie after that is a shared win.
- **Power rounds:** in rounds 11 to 15 (and overtime), every card played hits ×1.5, rounded up. Burns and heals over time stay the same.
- Each round, both players secretly choose a card, press **Ready**, and after a 3-second countdown the cards battle.
- Drag one card onto another to **merge** them into a combo. After playing a combo you're tired and can only play a single card next round (the board shows a Tired banner).
- The **Hold slot** saves a card (or combo) for later. Drop a hand card on it to swap.
- Your hand holds up to 5 cards; a combo counts as one.
- Both players draw from one shared, shuffled deck of 30 cards (6 of each element).
- Shields and healing happen first, then attacks. Healing past full health becomes shield.
- After each battle, both players press **Continue** to move on.

## Hosting on GitHub Pages

1. Upload `index.html` to the repository (it contains the whole game, including all art).
2. Go to **Settings → Pages**, choose the main branch and root folder, and save.
3. After a minute or two the game is live at `https://<your-username>.github.io/<repository-name>/`.

## Replacing the art (optional)

All card art and the arena background are built into `index.html`. To use new art, add an `assets` folder next to `index.html` with any of these files; the game uses them instead of the built-in versions:

- Elements: `card-wood.png`, `card-fire.png`, `card-earth.png`, `card-wind.png`, `card-water.png`
- Combos: `combo-<a>-<b>.png`, with elements in the order wood, fire, earth, wind, water (for example `combo-wood-fire.png` for Campfire)
- Arena background: `arena-mat.jpg`
- Card back: `card-back.png`

Online play uses [PeerJS](https://peerjs.com/) to connect players directly.
