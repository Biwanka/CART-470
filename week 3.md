# WEEK 3

## Meeting Notes

Notes taken during the first meeting with Jonathan:
https://docs.google.com/document/d/1Mx3We4dOp7mKr-jSiF4E0hrWiADEWIQM-2A8vSljJS4/edit?usp=sharing

We had a meeting today with our client Jonathan about what we are doing for him. We learned that this is more of a testing and prototyping journey. We do not need to have a working base game at the end. The important thing for him is that we explore different approaches to the project and try to mediate and lessen the amount of risk and problems, so that the 415 class does not need to lose time on this and can automatically just work on building the game/project.

## Questions to Think About

- What does the player do with their phone?
- What does their avatar do on the projected screen?
- What are 20–30 players doing at once?
- What happens when someone leaves?
- What happens when someone joins?
- What is the player's goal?
- How does the player know they're succeeding?
- What persists after they leave?
- Is there a reason to keep playing for ~5 minutes?
- What happens if only 1–3 people are there?
- What happens if there are 30 people?
- Can the game exist without a lobby, host, countdown, or coordinated start?

## References

### Baba Is You

https://www.youtube.com/watch?v=VjqdPjTKPiU

### Sokoban

Sokoban minigames and variants generally fall into a few distinctive categories based on how they alter the classic box-pushing, grid-based formula.

- Push boxes onto labeled tiles. When all the label tiles have a box on them, do you pass the level?

https://www.youtube.com/watch?v=_iZLe05aJuU

https://www.youtube.com/watch?v=TgWibgp2NwM

## Shared Exhibit Constraints and Ideas

To build a projected, drop-in/drop-out exhibition game that balances asynchronous multiplayer, persistence, and player interaction, the core technical constraint is the "zero-friction" lifecycle. Because players scan a QR code, play for two minutes, and walk away, the game must never wait for input, never display a menu, and gracefully clean up abandoned avatars.

### Architecture Rules to Think About

- **Ghost timeout (crucial):** If a phone doesn't send an input for 30 seconds (or if the phone screen locks because the visitor put it in their pocket), the game must smoothly fade that player's character out.
- **Automated level rollover:** Never have a "Play Next Level" button on the screen. Use a 5-second countdown timer overlaid on the gameplay (e.g., "Next Grid Loading in 5...4...") so current players know a transition is happening, then seamlessly swap the assets.
- **Color-coded onboarding:** When a user scans the QR code, their phone web page background should turn a bright, solid color (e.g., neon green), and their avatar on the projection wall should match that exact color with a label saying "You". This instantly tells the user which character they control without them having to guess.
- **Disconnect idea:** If a player leaves, their avatar could become a timer bomb that explodes, depending on the type of game.

## Game Concepts

### 1. Circle Timer — "Catch the Circles"

The projected screen has circles appearing around the map.

- Circles have different sizes.
- Each circle has a timer.
- Players move their avatars over them before they disappear.
- Smaller circles are harder to catch and could be worth more points.
- A player standing over a circle collects it.
- New circles continuously appear.
- The leaderboard is always visible.

**Loop:** Move → find a circle → collect it → earn points → repeat.

The game could be competitive individually, shared, or mixed:

- **Individual:** Everyone tries to get their own highest score.
- **Shared:** Everyone contributes to one giant community score.
- **Mixed:** Individual leaderboard plus a collective goal. This could give people a reason to interact with the same world without requiring formal teams.

**Problem to test:** With 30 players, do people have enough circles to interact with, or does it become chaos?

**Disconnect variation:** A disconnected player's avatar could become a bonus/time bomb. After a 10-second countdown, the explosion could make nearby circles disappear or turn them into bonus circles.

### 2. Colour Tiles — "Claim the Map"

This idea is extremely easy to understand visually. The screen starts as a grid, and each player has an avatar. When they walk over a tile, their path colours the floor.

The main question is: what happens to a tile after it has been claimed?

- **Permanent tiles:** Once coloured, they stay coloured. The whole screen gradually transforms.
- **Temporary tiles:** Tiles fade back to neutral after 10–30 seconds. This keeps the game active.
- **Ownership:** Walking over another player's tile changes its ownership, so players compete for territory.
- **Combination:** Players can create shapes by connecting tiles. For example, completing a 5×5 area could earn a bonus.

This could make the game more interesting than simply colouring as many squares as possible, and it naturally creates a persistent game state:

- Someone leaves: their coloured territory stays.
- Someone joins: they enter an already-developed map.

**Disconnect variation:** A disconnected player's avatar could become a bomb planted on their last tile. When it explodes, tiles around them change ownership or reset.

### 3. Collection Game

This could be a family of games rather than one specific concept.

**Basic mechanic:** Move around → find an object → collect it → bring it somewhere or accumulate it → score.

Possible objects include coins, stars, food, resources, puzzle pieces, or objects that belong together. Players could have limited carrying capacity, creating this loop:

**Find → collect → return → deposit → score.**

The persistent element could work in a few ways:

- The world is slowly emptied of resources.
- Resources regenerate.
- Everyone is collectively trying to fill a giant storage container.

### 4. Sokoban Swarm — Asynchronous Grid Puzzle

Since Sokoban was part of the research, it could be adapted into a persistent, massive multiplayer game. Imagine a giant grid with hundreds of boxes and hundreds of goals scattered everywhere.

- Each player controls a little worker.
- On their phone, they only see four arrow buttons.
- Players push boxes toward goals to clear paths.
- If Player A leaves a box in a hallway, it stays there. Player B might arrive 20 minutes later and have to deal with that layout.
- When the group pushes all boxes on the screen into goals (or reaches a target percentage), the screen flashes "Success!", automatically dissolves into a brand-new maze layout, and players keep moving instantly.

### 5. Ecosystem — The Cooperative Scale Game

**Gameplay:** The projection displays a massive, living ecosystem (a forest, an ocean, or a space nebula). When a player scans the QR code, they are assigned a creature or element (e.g., a cloud, a plant, a herbivore, or a small planet).

**Interaction:** Players control their element's movement and simple actions. A cloud player rains on a plant player to help them grow. A herbivore player eats the fruit dropped by plants.

**Why it fits:**

- **Asynchronous and persistent:** The ecosystem constantly moves. If 20 people are playing, it's frantic and lush. If no one is playing, automated AI takes over the idle nodes, keeping the projection beautiful.
- **No end game:** It is a looping simulation. If a milestone is reached (e.g., a "Super Tree" grows), a 10-second celebration animation triggers globally, and the map shifts layout or season automatically.

### 6. The Infinite Construction

**Gameplay:** A single, giant, collaborative architectural structure (like a skyscraper, a giant marble run, or a fantasy castle) slowly climbs higher and higher up the projected wall.

**Interaction:** The phone acts as a crane hook or a magnet. Players fly around the screen, grab floating building blocks or mechanical gears from the edges, and attach them to the central structure to help it expand.

**Why it fits:**

- **High interaction:** Players work together to build complex pathways. One player might place a conveyor belt, while another places a booster pad to move materials up.
- **Drop-in/drop-out:** If a player walks away, their crane simply vanishes. The block they were holding drops back into the pool. The monument remains intact for the next person.
- **Progression:** Once the tower reaches the absolute top of the projection, it "launches" into space, a fresh foundation appears, and the next level of building starts without stopping the game.

### 7. Constellation / Nebula Control — The Slither Evolution

**Gameplay:** Similar to slither.io, players spawn as tiny glowing cosmic particles. They absorb floating cosmic stardust to grow larger and trail a massive, glowing tail of light behind them.

**Interaction:** Instead of eating each other and killing them (which frustrates short-term exhibit visitors), colliding with another player fuses their light trails together, temporarily boosting both players' speeds and drawing beautiful constellation lines across the wall.

**Why it fits:**

- **Simple control:** Purely 2D directional steering on the smartphone screen.
- **No menus:** When a player closes their browser or walks away, their particle gently burns out into static stardust over 10 seconds, leaving food for the others.