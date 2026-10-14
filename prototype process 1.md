I think these changes make the three concepts much more interesting, especially for your role in the project. You're now moving from brainstorming game mechanics to prototyping the visual language of the game: what someone sees when they approach the projection, scan the QR code, join an ongoing game, and start interacting.
Your job is to test whether people can understand what's happening just by looking at the screen, without someone standing there explaining the rules.
I'd approach this as three screen prototypes, one for each game, with a particular focus on visual clarity, player feedback, and how the screen communicates what to do.
1. What your role needs to establish
For each game, you'll want to answer five questions:
- Attract: Can someone walking past understand what kind of game this is?
- Join: Is it obvious how to join, and what changes when a player connects?
- Act: Can a player understand how their avatar interacts with the environment?
- Feedback: Can they immediately see whether their action worked?
- Continue: If someone joins halfway through, can they understand the current game without needing its history?
You don't need to make the final art direction yet. Your first prototypes can be simple wireframes with squares, circles, labels, arrows, and placeholder avatars.
The important thing is to test the visual hierarchy and meaning, not whether the game looks beautiful.
2. Game one — Construction Site / Jenga







about.daangn.com


The screen represents an ongoing construction site. Players contribute to a shared tower, while a crane delivers new blocks. Metal beams/scaffolding provide places for players to stand outside the main building area.
Suggested screen layout
CONSTRUCTION SITE
Players: 18

CURRENT TOWER HEIGHT
12 blocks




CRANE
New blocks










SHARED TOWER


Scaffolding / resting beams





BUILD THE TALLEST TOWER
Tower stability: 65%


This is a layout concept, not a final gameplay screenshot. The stability indicator is optional and would need to match your actual rules.
What should the player understand visually?
Screen element	What it communicates
Tower in the centre	The shared objective
Crane and incoming block	Where new building material comes from
Scaffolding	Where players can stand or wait
Tower height	Collective progress
Stability indicator	The risk of the tower collapsing, if relevant
Other avatars	That other people are currently playing
Risks to test
1. The crane might be mistaken for decoration. Make its movement meaningful: when a block arrives, animate it from the crane to the building area.
2. The tower might look like a finished structure. Show an incoming block or a highlighted placement area to signal that construction is ongoing.
3. Players may not understand how to contribute. When a new player joins, highlight one available block and briefly show a directional movement cue.
4. The scaffolding might be visually confused with the tower. Give it a distinct shape or material, and test whether people understand that they can stand there without affecting the main structure.
Key de-risking question: Can a new player distinguish where to stand, where to get a block, and where to build without reading a paragraph?

3. Game two — Free-for-all Big Ball Soccer







rawg.io


This is now an individual competitive game. Everyone controls their own avatar, pushes balls around, and tries to score against an NPC goalkeeper. There can be multiple balls at once.
That makes the visual challenge different: players need to understand the ball physics, the goal, and their own contribution in a potentially crowded space.
Suggested screen layout
FREE PLAY SOCCER
18 players

GOALS: 24

TIME: ∞


NPC GOALIE

GOAL






TOP SCORERS
1. Player 12 · 8 goals


Layout concept only. The actual field orientation and number of goals depend on the mechanics you choose.
What should the player understand visually?
- The goal and NPC goalkeeper must be obvious.
- Balls should be visually distinct from avatars.
- A goal should trigger immediate feedback: a brief animation, a score increase, and a ball reset or respawn.
- The player's own avatar should be identifiable, ideally through a consistent colour or outline.
- The leaderboard should be visible but secondary to the action.
Risks to test
1. Too many balls create visual noise. If the balls overlap with avatars, players may struggle to see what they are pushing.
Possible approach: Start with one ball. Add a second only if play becomes too slow with more people.
2. Players don't know which avatar is theirs. A small outline, unique colour, or brief join animation can help.
3. Scoring is unclear. Show a visible goal event and a score change at the moment of success.
4. The game becomes a crowd around one ball. Multiple balls may distribute players across the screen, but they also increase complexity. Test both configurations instead of assuming more balls are better.
Key de-risking question: Can a player immediately identify their avatar, understand that touching the ball moves it, and recognise when they score?

4. Game three — Maze + Mosaic







thinkygames.com


This is probably the most visually demanding of your three prototypes, because the screen needs to communicate two connected activities:
1. Navigate the maze to find and collect coloured blocks.
2. Bring those blocks to the central mosaic to reproduce a target image.
Your uploaded sketch already establishes a useful composition: the maze occupies the surrounding space, and the large square in the middle becomes the mosaic.
The main thing to test is whether a new player can understand how the maze and mosaic relate to each other.
Suggested screen layout
MAZE MOSAIC
Players: 12

MAZE













Find blocks


TARGET

































Recreate the picture


CENTRAL MOSAIC
8 / 16 tiles





































































































































COLLECT → CARRY → PLACE
Shared progress


Conceptual screen layout, not a final maze design. The target pattern, tile colours, and progress counter are placeholders.
Your most important visual design decisions
A. How do players know which block to collect?
If the mosaic needs a red tile next, players need a way to know that.
Possible approaches:
- Fixed order: Highlight the next required tile in the target.
- Any order: Players can fill any unfinished tile, provided they collect the correct colour.
- Colour-specific collection: Players see coloured blocks throughout the maze and choose which to collect.
These create different games. I'd prototype any order with a visible target, first, because it gives players freedom while preserving the collective goal.
B. How do players know where to put the block?
This is particularly important because you mentioned that players cannot walk over coloured bricks.
If the mosaic tiles become obstacles, filling the central square could eventually block access to the remaining spaces.
Possible solutions:
- Give the mosaic a separate placement edge so avatars don't need to cross completed tiles.
- Allow placement from the surrounding border.
- Make completed tiles solid visually but non-blocking for movement.
- Use a fixed placement order that keeps the next target accessible.
My recommendation: Start by making completed mosaic tiles non-blocking. This preserves your visual idea without introducing a pathfinding problem before you know whether the main mechanic works.
C. How do players understand the whole loop?
Try to communicate the mechanic with three simple visual cues:

1. Find
A coloured block is visible in the maze.



2. Collect
The avatar carries the block, with a small colour indicator above it.



3. Place
A matching mosaic tile fills in, and the shared progress updates.



Key de-risking question: Can someone understand that the maze contains the resources needed to complete the picture, without being told verbally?

5. Your screen-testing method
You don't need to build the entire game to test these questions. Make one static screen for each concept, then create a simple clickable or animated prototype if needed.
I'd use the same test for all three so the results are comparable.
Visual comprehension test
Show one prototype to someone who hasn't heard the game explanation. Don't explain it first.
Choose the prototype

Construction Site / Jenga

Free-for-all Soccer

Maze + Mosaic


After looking at the screen, can the tester…
[ ] Identify the main objective
[ ] Identify what their avatar can interact with
[ ] Explain what happens when they perform an action
[ ] Tell whether the game is already in progress
[ ] Understand what they should do first
[ ] Explain what would happen if another player joined or left
0 of 6 understood


What confused the tester?

Copy test results
A useful extra is to test three different moments, not just the ideal screen:
- Empty state: Nobody is playing. Is the game inviting and understandable?
- Active state: Several players are interacting. Can you still distinguish the important information?
- Late-join state: Someone enters halfway through. Can they infer the objective and current progress?
For the maze in particular, test what happens when the mosaic is half complete. For the tower, test a nearly collapsing tower. For soccer, test multiple balls and many overlapping avatars.
6. What you should document for each visual decision
Use a compact format that shows your reasoning, not just the mockup.
Decision	Potential benefit	Risk / what is lost	Test
Tower height counter	Makes progress obvious	May distract from the tower	Compare screen with and without it
Distinct player colours	Helps identify avatars	Too many colours can become noisy	Test with 20–30 avatars
Multiple soccer balls	Distributes activity	Makes the screen harder to read	Compare one ball vs. two
Highlight next mosaic tile	Helps explain the objective	Reduces player freedom	Compare fixed order vs. any order
No permanent tutorial	Keeps screen uncluttered	Players may miss the rules	Test first-time comprehension
Persistent world state	Welcomes late arrivals	New players may not understand previous actions	Ask late-joining testers what they think is happening
The key is to record what the visual choice gains, what it sacrifices, and what evidence would tell you whether it works. You aren't expected to solve every technical issue yourself; you're identifying which decisions are safe for the Winter students to build on and which still need testing.
My suggested priority is to prototype the maze + mosaic screen first, because it has the most visual relationships to communicate. Then prototype the construction site and soccer screen using the same testing method. That gives your team comparable evidence for the three concepts, rather than three attractive mockups that haven't been tested for clarity.






he maze surrounds the central mosaic, and the coloured blocks in the maze are resources players collect to reproduce the picture in the middle.
The small shape at the top right appears to be the reference image showing what the mosaic should become.
What I understand from your prototype









1. The maze
Players navigate the paths between the white blocks. Some of the blocks in the maze become coloured resources that players can collect.












2. The central mosaic
Players bring coloured blocks here to reproduce the reference image. The partially coloured strawberry shows the collective progress toward completing the picture.












3. The missing player character
Each connected player needs a clearly identifiable avatar that moves through the maze. It should be visually distinct from the coloured blocks, walls, and mosaic tiles.



The main visual questions I would test
Your screen already communicates the overall structure quite well. The biggest unknowns are the interactions.
- Can players recognise their own character? Give each avatar a distinctive colour or outline, and test how it looks with 20–30 players.
- Can they tell which blocks are collectible? A coloured block in the maze should look different from a coloured tile already placed in the mosaic.
- Can they understand where to deliver the block? The central mosaic and reference image should make the objective visible without needing a permanent instruction panel.
- Can they tell when they have completed a task? When a block is placed correctly, the tile should visibly fill in and the shared progress should update.
One particularly important rule to decide is whether players can collect any colour and place it anywhere, or whether they must collect the exact colour needed for a particular tile. That choice changes how much guidance the screen needs to provide.
I would keep your existing composition for now and add the player character as the next prototype step. Then test the screen with someone unfamiliar with the game before adding more UI.




The main idea is that the players are little construction workers who move around the building area and help build the tower together. The two metal structures on either side are scaffolding towers that act as resting platforms. As the building gets taller, players can use the scaffolding to reach higher levels instead of being limited to the ground.
The cranes at the top are part of the construction-site aesthetic, but they aren't responsible for placing the blocks. The players themselves do that.
I actually think this is a useful visual direction for your prototype because the environment can help explain the game mechanics without needing a large instruction menu.
What I would test in your construction-site prototype









1. Scaffolding as a resting place
Can players immediately understand that the side structures are usable platforms, rather than decoration? Make ladders and platforms visually clear, and consider a subtle highlight when a player can climb onto one.











2. The construction worker
Use a simple, recognisable character. Test whether players can distinguish their own avatar from the other workers when 20–30 are on screen. A coloured outline or small identifier could help.











3. The central tower
It should remain the main visual focus. As it grows taller, players need to understand where they can safely stand, where they can place blocks, and whether the structure is becoming unstable.



One important decision to de-risk
What happens when the tower becomes taller than the player can reach from the ground?
- Option A — Climb the scaffolding: Players use ladders and platforms to reach higher levels. This makes the construction site feel physical, but adds movement and collision complexity.
- Option B — Jump onto the tower: Players can jump between blocks and build upward. This is intuitive for a platform game, but could become chaotic when many avatars occupy the same space.
- Option C — Use both: Players climb the scaffolding to reach higher areas, then jump or step onto the tower to build. This offers more freedom but is the most complicated to prototype.
I'd start with Option A, then test whether climbing alone makes the building process engaging enough.
For your visual prototype, you don't need working ladders, physics, or a real tower yet. You just need to show the character, the tower, the side scaffolding, and the possible routes between them. Ask testers what they think they can do before explaining the game. Their misunderstandings will tell you what the screen needs to communicate better.