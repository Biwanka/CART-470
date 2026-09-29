
# **WEEK 3**

Notes taken during first meeting with Jonathan: 
https://docs.google.com/document/d/1Mx3We4dOp7mKr-jSiF4E0hrWiADEWIQM-2A8vSljJS4/edit?usp=sharing 


We had a meeting today with our client Jonathan about what we are doing for him. We learned more that we are doing the more test and prototype journey. We do not need to have a working base game at the end, as for him the importance is that all the different approaches to the project and trying to mediate and lessen the amount of risk and problems is what he wants us to do, so that when the 415 class, do not need to lose time on this and can automatically just work on building the game/project.


question to think when thinking about the game :
-  What does the player do with their phone?
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


Reference game: 

Babba is You : https://www.youtube.com/watch?v=VjqdPjTKPiU 




SOKOBAN : 
Sokoban minigames and variants generally fall into a few distinctive categories based on how they alter the classic box-pushing, grid-based formula.

- push boxes onto labeled tiles, when all the label tiles have a box on them, do you pass the level.




https://www.youtube.com/watch?v=_iZLe05aJuU 

https://www.youtube.com/watch?v=TgWibgp2NwM 








To build a projected, drop-in/drop-out exhibition game that balances asynchronous multiplayer, persistence, and player interaction, your core technical constraint is the "zero-friction" lifecycle. Because players scan a QR code, play for two minutes, and walk away, the game must never wait for an input, never display a menu, and gracefully clean up abandoned avatars.




1. Concept: 'Eco-System' (The Cooperative Scale Game)
- The Gameplay: The projection displays a massive, living ecosystem (a forest, an ocean, or a space nebula). When a player scans the QR code, they are assigned a creature or element (e.g., a cloud, a plant, a herbivore, a small planet).
- The Interaction: Players control their element's movement and simple actions. A "Cloud" player rains on a "Plant" player to help them grow. A "Herbivore" player eats the fruit dropped by plants.

Why it fits:
- Asynchronous & Persistent: The ecosystem constantly moves. If 20 people are playing, it's frantic and lush. If no one is playing, automated AI takes over the idle nodes, keeping the projection beautiful.
- No End Game: It is a looping simulation. If a certain milestone is reached (e.g., a "Super Tree" grows), a 10-second celebration animation triggers globally, and the map shifts layout or season automatically.

2. Concept: 'The Infinite Construction'
- The Gameplay: A single, giant, collaborative architectural structure (like a skyscraper, a giant marble run, or a fantasy castle) slowly climbs higher and higher up the projected wall.
- The Interaction: Your phone acts as a crane hook or a magnet. You fly around the screen, grab floating building blocks or mechanical gears from the edges, and attach them to the central structure to help it expand.
 Why it fits:
- High Interaction: Players work together to build complex pathways. One player might place a conveyor belt, while another places a booster pad to move materials up.
- Drop-In/Drop-Out: If a player walks away, their crane simply vanishes. The block they were holding drops back into the pool. The monument remains intact for the next person.
- Progression: Once the tower reaches the absolute top of the projection, it "launches" into space, a fresh foundation appears, and the next level of building starts without stopping the game.

3. Concept: 'Sokoban Swarm' (Asynchronous Grid Puzzle)
- The Gameplay: Since you were just researching Sokoban, you can actually adapt it into a persistent massive multiplayer game. Imagine a giant grid with hundreds of boxes and hundreds of goals scattered everywhere.
- The Interaction: Each player controls a little worker. On your phone, you only see 4 arrow buttons. You can push boxes toward goals to clear paths.
Why it fits:
- Persistent Impact: If Player A leaves a box in a hallway, it stays there. Player B walks up 20 minutes later and has to deal with that layout.
- Progression: When the collective group manages to push all boxes on the screen into goals (or hits a target percentage), the screen flashes "Success!", automatically dissolves into a brand-new maze layout, and players keep moving instantly.


4. Concept: 'Constellation / Nebula Control' (The Slither Evolution)
- The Gameplay: Similar to slither.io, players spawn as tiny glowing cosmic particles. They absorb floating cosmic stardust to grow larger and trail a massive, glowing tail of light behind them.
- The Interaction: Instead of eating each other to kill them (which frustrates short-term exhibit visitors), colliding with another player fuses your light trails together, temporarily boosting both of your speeds and drawing beautiful constellation lines across the wall.
Why it fits:
- Simple Control: Purely 2D directional steering on the smartphone screen.
- No Menus: When you close your browser or walk away, your particle gently burns out into static stardust over 10 seconds, leaving food for the others.



Exhibit Architecture Rules for This Concept

**Rule or ideas to think about :** 

- The Ghost Timeout (Crucial): If a phone doesn't send an input for 30 seconds (or if the phone screen locks because the visitor put it in their pocket), the game must smoothly fade that player's character out.
- Automated Level Rollover: Never have a "Play Next Level" button on the screen. Use a 5-second countdown timer overlayed on the gameplay (e.g., "Next Grid Loading in 5...4...") so current players know a transition is happening, then seamlessly swap the assets.
- Color-Coded Onboarding: When a user scans the QR code, their phone web page background should turn a bright, solid color (e.g., Neon Green), and their avatar on the projection wall should match that exact color with a label saying "You". This instantly tells the user which character they control without them having to guess.


- Bomb disconected player: if a player leaves there avatar could be a timmer bomb that explodes (depending on the type of game)

thinking of concept/ideas of games: 

- circle timer : circle appear on the screen in different sizes and starts to get smaller, if you are able to walk over it you get points, try to gather as much points as possible (leaderboard)

- colour tiles: have a grid where a player walks on a square and it colours it, try to have the most coloured squares on the map. 
- could be a collection game 

*****need to think of a pushing idea game 






1. Circle Timer — "Catch the Circles"

The projected screen has circles appearing around the map.

- Circles have different sizes.
- Each circle has a timer.
- Players move their avatars over them before they disappear.
- Smaller circles = harder to catch / potentially more points.
- A player standing over a circle collects it.
- New circles continuously appear.
- The leaderboard is always visible.

Loop : Move → find circle → collect → earn points → repeat


The interesting part is that you can make the circles collectively or individually competitive.

For example:

Individual:
Everyone is trying to get their own highest score.

Shared:
Everyone contributes to one giant community score.

Mixed:
Individual leaderboard + collective goal.

The mixed version could be particularly useful because it gives people a reason to interact with the same world without requiring formal teams.

Problem to test: With 30 players, do people have enough circles to interact with, or does it become chaos?

That's a very good de-risking question.






2. Colour Tiles — "Claim the Map"

I really like this one for your project because it is extremely easy to understand visually.

The screen starts as:


□ □ □ □ □ □ □ □
□ □ □ □ □ □ □ □
□ □ □ □ □ □ □ □
□ □ □ □ □ □ □ □
□ □ □ □ □ □ □ □

Each player has an avatar.

When they walk over a tile:

□ □ ● □ □
□ ■ ■ ■ □
□ ■ ■ ■ □
□ □ ● □ □


Their path colours the floor.

Now you have a persistent question:

What happens to a tile after it has been claimed?

A. Permanent tiles

Once coloured, they stay coloured.

This makes the whole screen gradually transform.

B. Temporary tiles

Tiles fade back to neutral after 10–30 seconds.

This keeps the game active.

C. Ownership

Walking over another player's tile changes its ownership.

Now players are competing for territory.

D. Combination

Players can create shapes by connecting tiles.

For example:

Complete a 5×5 area → bonus.

That could make the game much more interesting than simply "colour as many squares as possible."

And it naturally creates a persistent game state.

Someone leaves:

Their coloured territory stays.

Someone joins:

They enter an already-developed map.

That's exactly the kind of problem your project needs to investigate.







3. Collection Game

This could actually become a family of games rather than one specific concept.

The basic mechanic:

Move around → find object → collect object → bring it somewhere / accumulate it → score.

For example, the screen could have:

coins
stars
food
resources
pieces of a puzzle
objects that belong together

Players could have limited carrying capacity.

So:

Find → collect → return → deposit → score

Then the persistent element becomes important.

Maybe the world is slowly being emptied of resources.

Or resources regenerate.

Or everyone is collectively trying to fill a giant storage container.





And your "bomb when disconnected" idea is actually really useful

I wouldn't necessarily make it the entire game mechanic.

I'd treat it as a solution to the player-leaving problem.

For example:

Player disconnects → their avatar becomes a bomb → 15-second countdown → explosion affects the environment.

That immediately gives meaning to someone leaving.

But you could adapt the idea depending on the game.

In the circle game

Disconnected player becomes a bonus/time bomb.

PLAYER LEAVES
      ↓
   💣 10 sec
      ↓
   EXPLOSION
      ↓
Nearby circles disappear
OR
Nearby circles become bonus circles


In the tile game

Their avatar becomes a bomb planted on their last tile.

When it explodes:

Tiles around them change ownership/reset.

That creates a really interesting consequence to leaving.

In the collection game

Their avatar becomes a resource crate.

Other players can collect what they left behind.

That would connect nicely to your client's:

"does the character disappear, or does his body become dead to be consumed"

You don't necessarily need to make it dark. The basic principle is:

A disconnected player leaves something behind that other players can interact with.

I think that's a very strong design principle for your project.





I'd also change how you're thinking about the leaderboard

Your client specifically likes the leaderboard, but you don't want it to simply be:

Bianca — 532 points
Alex — 489 points
etc.

because then you have to figure out how individual scoring works in every possible mechanic.

Instead, you could experiment with different scoring models.

Individual

Who collected the most?

Territory

Who controls the most?

Contribution

Who contributed the most to the collective objective?

Survival

How long has the community kept the world alive?

Global + individual


COMMUNITY
██████████████░░░░  72%

TOP PLAYERS
