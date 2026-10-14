I think this is a really useful change to the project, because your role is now much more concrete: you are prototyping the visual language and screen layout of the three games, then testing whether people can understand what they are seeing without someone explaining it to them.
You're not just making the games look good. You're de-risking the communication of the game: where players need to look, how they recognize objects, how they understand what they can interact with, and how they know what to do next.
Since the game will be projected at an exhibition, people may walk up halfway through, scan a QR code, and start playing immediately. The projected screen needs to communicate enough that a newcomer can understand the game while 20–30 other players are already there.
I'd approach your prototypes as three playable-looking screen mockups, starting with simple shapes and labels rather than polished artwork.
1. What your prototype should test
For each game, I would create a screen mockup showing the game in its normal state, not just a title screen.
Then test whether a person can answer these questions by looking at the screen:
- What is happening?
- What am I supposed to do?
- Which objects can I interact with?
- Where do I go?
- How do I know that my action worked?
- What happens if I join when the game is already in progress?
You can test the visuals before the game mechanics are fully programmed. Use rectangles, circles, simple avatars, arrows, and colour coding. If people don't understand the wireframe, adding better artwork won't necessarily solve the problem.
2. Prototype A — Construction Site / Jenga







hooked-a-tower-crane-game-ios.soft112.com


The visual idea is a construction site where players collaborate to build a tower. A crane delivers new blocks, and steel beams provide platforms where players can stand or rest outside the main building area.
What should be visible on the projected screen?
CONSTRUCTION SITE
12 BUILDERS

CRANE · NEW BLOCK



BEAM PLATFORM


TOWER
















HEIGHT: 8 BLOCKS
BUILD THE TALLEST TOWER


Schematic layout concept — not the final game artwork.
Visual decisions to test
Element	Recommended approach	Risk to investigate
Tower	Make blocks visually distinct, with clear edges and shadows	Can players tell where a block can be placed?
Crane	Show a block being carried or lowered	Is it obvious that the crane delivers blocks?
Metal beams	Give them a different material and shape from tower blocks	Do players understand that they can stand there?
Player avatars	Small, high-contrast characters with visible movement	Can players distinguish their characters among 30 people?
Tower height	Display a simple height counter	Does this communicate progress better than a score?
Falling tower	Use a clear collapse animation followed by automatic rebuilding	Do players understand that the next building cycle has started?
The main visual risk: the screen could become cluttered with players, blocks, the crane, and the tower.
I would visually separate the construction area from the resting platforms. Use different floor textures or outlines rather than adding lots of explanatory text.
Also, make the crane's delivery action visually obvious. If the crane is decorative and players don't understand its function, it is taking up valuable screen space.
3. Prototype B — Free-for-all Soccer







globalgamejam.org


This version is a free-for-all: every player moves around the field, multiple balls can be active, and an NPC goalkeeper protects the goal.
The biggest challenge for your lens is communicating the objective when there are many moving objects and no teams to explain the situation.
What should be visible?
BALL RUSH
18 PLAYERS


NPC GOALKEEPER






























MOVE · HIT THE BALL · SCORE


YOUR SCORE: 12
TOP SCORE: 48


Schematic layout concept — the final arrangement depends on the actual field dimensions.
Visual decisions to test
Element	Recommended approach	Risk to investigate
Balls	Use a strong outline and consistent ball design	Can players distinguish balls from avatars?
Avatars	Use varied silhouettes or colours	Can people track their own character?
NPC goalkeeper	Give it a distinctive shape and position	Is it obvious that this character is not another player?
Goals	Make the scoring area highly visible	Can players tell where they need to send the ball?
Score	Show personal score and a small persistent leaderboard	Can players understand what earns points?
Multiple balls	Start with one, then test two or three	Does more activity make the game more fun or just harder to read?
The main visual risk: too many moving objects.
I would not start the prototype with 30 avatars and several balls. Start with 5 avatars and one ball, establish whether the interaction reads clearly, and gradually increase the count.
A useful visual feedback loop would be:
Avatar hits ball → ball visibly moves → ball enters goal → score increases.
If players cannot connect those events, the scoring rules may need to be made more explicit.
4. Prototype C — Maze + Mosaic







motivs.eu


This is probably the most visually demanding concept of the three, because the screen must communicate two related activities:
1. Navigating a maze to find coloured blocks.
2. Using those blocks to complete a mosaic in the central grid.
Your reference image already provides a useful spatial structure: maze corridors around the edges and a large central square for the mosaic.
What should be visible?
MAZE MOSAIC
9 PLAYERS

COLLECT IN THE MAZE































FIND COLOURED BLOCKS



BLOCKS



CARRY: 1


TARGET MOSAIC
12 / 36 TILES













































































COLLECT → CARRY → PLACE → COMPLETE THE IMAGE

Schematic layout concept. The final prototype should use your maze layout and a target image that matches its tile grid.
Visual decisions to test
Element	Recommended approach	Risk to investigate
Maze walls	Strong contrast between walls and walkable paths	Can players immediately identify where they can move?
Collectible blocks	Give each colour a consistent, recognizable shape or outline	Can players distinguish collectibles from decorative tiles?
Central mosaic	Show the target image clearly and keep placed tiles visible	Can players tell what remains to be completed?
Carrying state	Show the block above or beside the avatar	Do players understand that they are carrying something?
Placed blocks	Make occupied tiles visibly different from empty tiles	Is it clear that players cannot walk over them?
Progress	Show tiles completed, such as 12/36	Does this help players understand the collective objective?
The main visual risk: players may not understand the order of operations.
The game has more steps than the other two:
Find a block → collect it → navigate back → place it correctly → repeat.
You need to communicate all of those actions without turning the screen into an instruction manual.
My recommendation is to make the next useful action obvious. For example, when a player is carrying a blue block, the corresponding empty tile in the mosaic could briefly glow blue. This teaches placement through visual feedback rather than text.
One important design decision to resolve early is whether players can carry only one block. A one-block limit is easier to communicate and creates a simple loop, but it means more trips through the maze. Carrying several blocks reduces the number of trips but adds UI complexity.

5. What to test across all three screens
I would use the same evaluation framework for each concept, so you can compare them fairly.
Test	What you observe	What failure tells you
First glance	Ask what the person thinks the game is about	The objective isn't visually clear
First action	Ask them to start without explaining the controls	The interaction isn't discoverable
Feedback	Ask what changed after their action	The effect of the action isn't obvious
Late joining	Show the game already in progress	The current game state lacks context
Player leaving	Remove one avatar during play	The screen may depend too much on individual players
Crowd test	Add 20–30 avatar markers	The visual hierarchy may collapse at scale
Phone test	Show the phone controller separately	The controls may require too much explanation
A simple usability test you can run
You don't need a functional multiplayer game to start. You can show someone the wireframe and ask them to think aloud.
Usability test checklist
0 of 5

[ ] First glance
What do you think is happening on this screen?

[ ] Goal
What do you think you are trying to accomplish?

[ ] First action
What would you do first if you scanned the QR code?

[ ] Feedback
How would you know that your action worked?

[ ] Joining late
If this game had been running for 20 minutes, could you join now?

Reset checklist
Try this with people who haven't heard your team's explanations. Don't explain the game beforehand, because the point is to find out what the screen communicates on its own.
Record what they misunderstand, where they look first, and which elements they ignore. A person misunderstanding the game is not a failed test — it tells you what needs redesigning.
6. My recommendation for your next step
Build three low-fidelity wireframes with the same visual discipline:
- A clear game title or objective.
- The playable area taking up most of the screen.
- Only the essential score/progress information.
- Consistent visual language for avatars, interactive objects, and feedback.
- A small, persistent leaderboard if the game needs one.
- No lobby screen or mandatory tutorial overlay.
Keep the phone controller separate in your mockups, because the projection and phone have different jobs. The projection should communicate the shared game state; the phone should communicate the actions available to that player.
Then test the three concepts with the same people and the same questions. Your deliverable becomes more than three attractive screens: it becomes evidence about which visual approach makes the rules easiest to understand, especially for people joining an already-running game.