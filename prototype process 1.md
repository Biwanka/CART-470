# Week 5: Prototype Process 1

## Purpose of the prototypes

My role is to test whether visitors can understand the projected game screen without someone standing nearby to explain it. The screen should help a passerby:

1. Notice the game and understand its general activity.
2. See how to join and recognize what changes when they connect.
3. Understand what their avatar can interact with.
4. See whether their action worked.
5. Join an ongoing game and understand its current state.

These are early screen prototypes, not final artwork or finished games. Start with simple shapes, labels, arrows, colours, and placeholder avatars. Test the hierarchy and meaning before polishing the visuals.

## Prototype A: Construction Site / Jenga

### Core idea

Players are construction workers who collaborate to build a shared tower. The two metal structures at the sides are scaffolding towers. Players can use the scaffolding as resting platforms and to reach higher levels as the tower grows.

The cranes are part of the construction-site setting; they do **not** place or deliver the blocks. Players move and place the blocks themselves.

### What the projected screen should communicate

- The tower is the shared objective and main focus.
- Players are actively building it.
- The side scaffolding is usable and distinct from the tower.
- The tower's height or collective progress is visible.
- A new player can tell where to go and how to contribute.
- Other avatars show that the game is already in progress.

Possible screen labels:

- **Construction Site**
- **Build the tallest tower**
- **Tower height: 8 blocks**
- **Players: 12**

Treat these labels and numbers as placeholders until the game rules are decided.

### Visual decisions to test

#### Tower and placement area

- Give blocks clear edges and distinguishable shapes.
- Make it visible where a block can be placed.
- If the tower is meant to be unstable, show that visually or with a simple stability indicator.
- Test whether the tower looks like something still being built rather than a finished structure.

#### Scaffolding

- Give the scaffolding a different shape, outline, or material from the tower.
- Show ladders and platforms clearly.
- Test whether visitors understand that workers can stand on or climb the scaffolding.

#### Construction workers

- Use a simple, recognizable avatar.
- Test whether a player can identify their own character among 20-30 workers.
- A distinct outline, colour, or brief join animation could help.

#### Cranes

- Keep cranes visually secondary if they are decorative.
- If they compete with the tower or make visitors think they control block placement, simplify or reposition them.

### Main risks and questions

- Can visitors tell where to stand, where the blocks are, and where to build without reading a paragraph?
- Does the scaffolding look usable rather than decorative?
- Can players distinguish their avatar from the blocks and other workers?
- Does a height counter communicate progress, or distract from the tower?
- What happens when the tower grows beyond the height reachable from the ground?

### Reaching higher levels

Possible approaches:

- **Climb the scaffolding:** Players use ladders and platforms to reach higher parts of the tower. This fits the construction-site setting, but adds movement and collision complexity.
- **Jump onto the tower:** Players jump between blocks. This may feel intuitive, but could become chaotic when many avatars share the space.
- **Use both:** Players climb the scaffolding, then step or jump onto the tower. This offers freedom but is the most complex option.

Start by representing scaffolding and climbing in the visual prototype. Test whether visitors understand the route before adding jumping or more complex movement.

### First prototype test

Show the screen to someone unfamiliar with the game. Before explaining anything, ask them to point out where they would go, what they think they can do, and how they think the tower gets taller.

## Prototype B: Free-for-all Soccer

### Current prototype version

Each player controls an individual avatar, moves around a field, and pushes balls toward a goal defended by an NPC goalkeeper. Multiple balls may be active, and players can compete for goals.

This is the version described in these prototype notes. It is not necessarily the final soccer direction: Jonathan's earlier feedback raised a possible team-based version with many balls and a preference for turn-based play. Confirm the direction before polishing this screen.

### What the projected screen should communicate

- Where the goal and goalkeeper are.
- Which objects are balls and which are player avatars.
- What the player should do to score.
- Whether a goal has been scored and whose score changed.
- Which avatar belongs to the person using the phone.

Possible screen labels:

- **Ball Rush**
- **Move - hit the ball - score**
- **Your score: 12**
- **Top score: 48**

Use a score display or leaderboard only if it supports the gameplay; it should not overpower the field.

### Visual decisions to test

#### Balls and avatars

- Give balls a consistent design and strong outline so they do not look like avatars.
- Give avatars distinguishable colours, silhouettes, or outlines.
- Test recognition with a small number of players first, then increase the crowd.

#### Goal and goalkeeper

- Make the scoring area highly visible.
- Give the NPC goalkeeper a distinctive appearance so visitors do not mistake it for another player.

#### Scoring feedback

Make the cause and effect visible:

**Avatar contacts ball -> ball moves -> ball enters goal -> score increases.**

The goal event should trigger immediate feedback, such as a brief animation and a visible score update. Decide whether the ball resets or respawns after a goal.

### Main risks and questions

- Too many moving objects may make the game hard to read.
- Players may not identify their own avatar.
- A crowd may form around one ball.
- Multiple balls might distribute activity, but could make it harder to see what is happening.
- A free-for-all may not match the client's preference for turn-based play or the suggested team-based variation.

### First prototype test

Start with about five avatars and one ball. Check whether a new player can identify their avatar, understand how contact moves the ball, and recognize a goal. Only add more players or balls if the basic interaction remains clear.

Compare one ball with two or three balls instead of assuming that more balls will improve the game. If the project moves toward turn-based play, test whether a discrete push still feels like soccer before committing to this visual direction.

## Prototype C: Maze + Mosaic

### Core idea

Players navigate a maze to find and collect coloured blocks, then bring them to a central mosaic to recreate a target image. The maze surrounds the mosaic. A reference image shows the intended result, and the partially completed mosaic makes shared progress visible.

The main visual challenge is showing that the maze and mosaic are connected parts of one activity.

### What the projected screen should communicate

- The maze is where players find coloured blocks.
- The central mosaic is where they use those blocks.
- The target image shows what the group is trying to complete.
- Players can see which blocks are collectible.
- A player can recognize their avatar among the walls, blocks, and mosaic.
- Progress updates when a block is placed.

Possible screen labels:

- **Maze Mosaic**
- **Find coloured blocks**
- **Carry: 1**
- **Target mosaic: 8 / 16 tiles**
- **Collect - carry - place**

Keep the target image visible and the instructions short. The screen should communicate the loop through the environment, not a permanent instruction panel.

### The player journey to communicate

1. **Find:** A coloured block is visible in the maze.
2. **Collect:** The avatar picks it up; a small colour indicator shows what it is carrying.
3. **Place:** A matching mosaic tile fills in, and shared progress updates.

### Visual decisions to test

#### Identifying blocks and tiles

- Make collectible blocks in the maze look different from tiles already placed in the mosaic.
- Make the target image and unfilled mosaic spaces easy to compare.
- Add a clear carried-block indicator above or beside the avatar.

#### Choosing which block to collect

Possible rule directions:

- **Fixed order:** Highlight the next required tile in the target.
- **Any order:** Players can fill any unfinished mosaic tile if they bring the matching colour.
- **Colour choice:** Players choose which coloured block to collect and then find a matching open mosaic space.

These options create different games. Begin by testing any-order placement with a visible target, since it allows player choice while keeping the shared objective clear. If players do not know what to do next, test highlighting a suggested tile.

#### Placing blocks and navigating

If completed mosaic tiles block movement, filling the central area could cut off access to unfinished spaces. Possible approaches:

- Let players place blocks from the surrounding edge.
- Give the mosaic a separate placement edge.
- Make completed tiles look solid but remain passable.
- Use a fixed placement order that keeps the next target accessible.

Start with completed tiles as non-blocking. This preserves the visual idea without adding a pathfinding problem before the main loop is understood.

#### Player avatars

- Add a clearly identifiable player character to the maze.
- Use a distinct colour or outline so the avatar does not blend with collectible blocks, walls, or mosaic tiles.
- Test the screen with 20-30 avatars to see whether a player can still track their own character.

### Main risks and questions

- Can a visitor tell that the maze contains resources needed to complete the picture?
- Can they tell which blocks are collectible and where a block should go?
- Does the reference image make the goal obvious?
- Can players recognize when they have completed an action?
- Is the intended block colour or placement order clear without verbal explanation?
- Do completed mosaic tiles prevent players from reaching remaining spaces?

### First prototype test

Use the existing maze-around-the-mosaic composition and add the missing player avatar. Show the screen to someone unfamiliar with the game and ask them to describe what they think the maze, coloured blocks, target image, and central mosaic are for. Add more UI only in response to what testers misunderstand.

## Screen-comprehension test

Use the same test for each concept so the results can be compared. Show the prototype to someone who has not heard the rules. Do not explain the game first.

Ask whether the tester can:

- Identify the main objective.
- Identify what their avatar can interact with.
- Explain what happens when they perform an action.
- Tell whether the game is already in progress.
- Understand what they should do first.
- Explain what they think happens when another player joins or leaves.

Record each answer and note what confused the tester. The "0 of 6" in the earlier draft was a placeholder for recording results, not a completed test result.

Test three different screen states:

- **Empty:** Nobody is playing. Does the screen invite someone to join?
- **Active:** Several people are playing. Can the important information still be seen?
- **Late join:** Someone arrives partway through. Can they infer the objective and current progress?

Also test a challenging state for each game:

- **Construction site:** The tower is very tall or close to collapsing.
- **Soccer:** Several avatars and multiple balls overlap.
- **Maze + mosaic:** The mosaic is partly complete.

## How to record a visual decision

For each decision, write down:

- **Decision:** What visual feature or rule are you testing?
- **Benefit:** What might it help players understand?
- **Trade-off:** What could become harder, less clear, or less fun?
- **Test:** What comparison or question would provide evidence?

Examples:

### Tower-height counter

- **Benefit:** Makes collective progress visible.
- **Trade-off:** Could distract from the tower.
- **Test:** Compare the screen with and without the counter.

### Distinct player colours

- **Benefit:** Helps players identify avatars.
- **Trade-off:** Too many colours may make a crowded screen noisy.
- **Test:** Check avatar recognition with 20-30 players.

### Multiple soccer balls

- **Benefit:** May distribute activity across the field.
- **Trade-off:** Makes the screen harder to read.
- **Test:** Compare one ball with two or three.

### Highlighted mosaic tile

- **Benefit:** Suggests what to do next.
- **Trade-off:** Reduces freedom to choose where to contribute.
- **Test:** Compare a highlighted next tile with any-order placement.

### No permanent tutorial

- **Benefit:** Keeps the screen uncluttered.
- **Trade-off:** Players may miss the rules.
- **Test:** Measure first-time comprehension with a short visual cue versus no cue.

### Persistent game state

- **Benefit:** Welcomes late arrivals and preserves earlier contributions.
- **Trade-off:** New players may not understand how the current state came about.
- **Test:** Ask late-joining testers what they think is happening.

## Suggested next steps

1. Make a simple screen mockup for each concept using the same visual-comprehension test.
2. Start with the maze + mosaic, since it has the most visual relationships to explain.
3. Add the player avatar to the maze and test the current composition before adding more interface.
4. Prototype the construction site and soccer screens with simple shapes and placeholder labels.
5. Test soccer's current free-for-all version against the client's turn-based and team-based preferences before polishing it.
6. Record what each visual choice improves, what it sacrifices, and what evidence would help the team decide.

The goal is not to resolve every technical or design question. It is to identify which choices are clear enough to build on and which still need testing.

## Visual inspiration noted in the original draft

The draft included the following domains as image references. The exact page URLs were not recorded:

- Construction site: `about.daangn.com`
- Soccer: `rawg.io`
- Maze and mosaic: `thinkygames.com`
