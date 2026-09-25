# Elemental Battle 五行

A card battle game built on the five elements: Wood, Fire, Earth, Wind, and Water.
Play against the computer (Easy, Medium, or Hard) or against a friend online.

## Play

Open `index.html` in a browser, or visit the GitHub Pages link for this repository. The landing page shows a picture guide to the rules.

The game board is designed for **landscape**: on a phone, turn it sideways (an upright phone shows a reminder). On Android you can tap ⛶ for full screen.

- **vs Computer:** type your name and pick a difficulty.
- **vs a friend:** one player presses **Host a game** and shares the 5-character code; the other types it into **Join game**.

## How to play

- Knock your opponent's health (30) to 0, or have more health after 15 rounds. A tie goes to overtime (round 16); a tie after that is a shared win.
- **Two spots each round:** a ⚔️ attack spot for Damage cards and a 🛡️ defense spot for Defense cards. Support cards fit either spot, but only one Support card per round. Play one card or both.
- Drag one card onto another to **merge** them into a combo.
- Press **Ready** to lock in (it's final). After a 3-second countdown, shields and healing happen first, then attacks. Attacks hit the shield before health; burns and cuts skip the shield. Healing past full health becomes shield.
- **Refill:** after each round you draw up to 2 new cards, or a fresh 5 if your hand is empty. Your hand holds up to 5 cards (a combo counts as one).
- **🗑️ New hand:** once per game, throw away your whole hand and draw 5 new cards right away. Your held card stays.
- **Tired:** Wind and Root Quake make the other player Tired ⚔️; Mudslide and Tornado make them Tired 🛡️. A Tired spot only takes single cards for one round. Water, Campfire, Garden, Great Tree, and Rain block Tired if played that same round.
- **Power rounds (11 to 15):** attacks hit ×1.5 (shields and heals don't), and the arena crumbles: both players lose 2, 3, 4, 5, then 6 health at the start of each round.
- The **Hold slot** saves one single card for later. Drop a hand card on it to swap.
- **Meadow** (Earth + Wind) is a free action: drop it in one of your spots to see their hand, and their cards once they press Ready. You still play your cards.
- **Garden** lets you take any card from the discard pile: tap it to see its combos, then drag it into your hand (onto a card to swap it out if your hand is full).
- **Rain** washes off your burns, cuts, and Tired, and heals 3. **Forge** doubles your next card in the same spot.
- **Double knockout:** if both fighters hit 0 at the same moment, whoever dealt more damage that round wins. Equal damage is a tie.
- Both players draw from one shared, shuffled deck of 30 cards (6 of each element).
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
