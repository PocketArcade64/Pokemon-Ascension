# Pokemon-Ascension

Spin Off Pegglin/Slay The Spire/Pegglin

Use Gen 2 Sprites on Dropbox (there are both front and back sprites included)

The Main gameplay loop is like Slay the Spire but rewards give you coins to use on
- a crane machine mini game (like NES Kirby’s Adventure)
- a mini game like Pegglin
- Both mini games unlock new cards (Pokemon) for your starting deck.

Peggle-style minigame ("catch" mode)
* Player drops from the top of the screen a Poké Ball into a peg field; which pegs it hits along the way doesn't matter.
* Reward is determined by which slot the ball lands in at the bottom — each slot maps to a specific Pokémon or reward tier.
* Poké Ball type is chosen before the shot, purchased with coins earned from the Spire climb.
* Ball type affects trajectory/behavior only (e.g., homing, splitting, guaranteed slot, odds-shifting toward certain slot types) — skill is in aiming, not in what you hit along the way.
* This mode is the sole source of new Pokémon for the deck; the crane machine (items/equipment) is kept separate.

Crane Machine minigame ("prize" mode)
* Purchased plays using coins earned from the Spire climb.
* Prize field contains a mix of starting items/equipment and shiny variants of Pokémon already unlocked — no new base Pokémon here, that's Peggle-mode only.
* Controls (matching Kirby's Adventure's Crane Grabber exactly):
    * Crane moves left/right automatically on a fixed sweep, oscillating back and forth across the top of the play field.
    * Player presses a single button to stop the crane's horizontal movement at the desired position.
    * Crane then drops straight down automatically, grabs whatever prize is directly beneath it, and retracts.
    * No manual control over the grab strength or drop timing beyond the single left/right stop — success is purely about timing the horizontal stop, same as the original.
    * Optional (matching Kirby's Adventure structure): a fixed number of grabs per "session" (Kirby's Adventure typically gives limited attempts before the game ends), rather than unlimited plays per coin spent.

Slay the Spire “Ascend” mode (main gameplay loop)
* Run start: player picks a starting Pokémon (from those unlocked via Peggle mode) and a starting item (from those unlocked via Crane mode).
* Map traversal: branching node-based path up the Spire — battles, elite fights, rest sites, shops, and events, same structural variety as Slay the Spire.
* Battles: turn-based, deck-of-cards combat using moves tied to the player's Pokémon roster.
* Rewards after battles: coins (spent on Peggle/Crane minigames between nodes) plus standard in-run boosts (relics/items, healing, gold) — but no direct new-Pokémon or new-item drops here, since that's reserved for the two minigames.
* Goal: reach and defeat the top-of-Spire boss; deck/roster power comes from what you've unlocked externally (via Peggle + Crane) rather than from random in-run card draws alone.

Main Menu Layout
* Top — "Ascend": large, primary button, visually dominant (top of hierarchy, likely centered or full-width). Launches Slay the Spire mode — starting Pokémon/item selection screen.
* Below "Ascend" — three secondary buttons, roughly equal size/weight:
    * Collection — browse unlocked Pokémon and items (roster/dex view, no gameplay action)
    * Poke Drop — launch the Peggle-style catch minigame (spend coins → unlock new Pokémon)
    * Crane Machine — launch the crane minigame (spend coins → unlock items/shinies)
    * Settings - music volume, sound effects volume, developer mode button where code “Ascension” opens up a menu with developer testing biuttons (like add coins, etc)
Hierarchy logic: "Ascend" is the core loop and sits alone at the top since it's where coins are earned and the run actually happens. The four supporting buttons sit below as a row or stack, reflecting that they're all in service of Ascend — Collection is passive (view only), while Poke Drop Mode and Crane Machine are the active spend-coins-to-unlock loops, kept visually parallel since they're deliberately symmetrical in function (both convert coins into progression, just via different skill types).
