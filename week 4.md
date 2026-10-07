# Week 4: Game Ideas and De-risking

## Why we are doing this

We narrowed the team's ideas to three concepts and are evaluating them from different lenses. The goal is to identify what works, what could fail, and what should be tested before CART 415. We are not expected to deliver a finished game.

The project is a large-screen exhibition game. Visitors should be able to scan a QR code, use a phone as a controller, understand what to do quickly, play briefly, and leave without interrupting the experience.

**Ideation board:** [Figma](https://www.figma.com/board/joIBlHFDXsKuD8T4MNxz97/CART-470-_Ideation?node-id=1-24&t=nfvc4baqqIPk503x-0)

![Week 4 ideation board](./image.png)

## Client feedback and implications

In a recent email, Jonathan said:

- Prefer turn-based ideas. Avoid concepts that depend on real-time engagement, synchronized actions, or very good networking.
- Avoid choice-driven stories: they require reading and context, and people who join late may not understand what is happening.
- Avoid an explicitly war or fighting theme unless it is presented playfully.
- He likes the Jenga idea.
- He is interested in a large collective task, such as sorting a big mess of objects into the right places.
- He suggested a pixel-art puzzle: place scattered colored blocks in the right places and order, accounting for blocks that obstruct one another.
- Big-ball soccer sounds fun, but its central interaction is unclear. One possible variation is chaotic soccer with 20+ balls, where visitors join either team and push balls toward a side.

These comments are new constraints and directions to consider, not proof that a concept has already been selected. In particular, the current soccer idea depends on real-time pushing, so it needs substantial redesign to fit Jonathan's preference for turn-based play.

## Team lenses for this week's discussion

- **Multiplayer flow (Alex):** What happens with 1 player, 20-30 players, and changing player counts?
- **Asynchronous / continuous play, phone controls, and simple rules (Bianca / my lens):** Can a visitor join, understand the game, act, and leave without a lobby, tutorial, or coordinated start?
- **Reasons to stay (Emma):** What gives someone already playing a reason to continue?
- **Reasons to join or return (FayFay):** What attracts someone passing by or returning later?

Each lens should identify benefits, risks, possible mitigations, trade-offs, and a prototype or test that could reduce uncertainty.

## My lens: async play, phone controller, and clear rules

### Questions to ask of every idea

**Asynchronous and continuous**

- Can the game continue if people are not playing at the same time?
- What does a new player see and do when joining an ongoing game?
- What state remains after someone leaves?
- Can the game continue without a host, lobby, coordinated start, or required waiting?
- Does the mechanic still work with one player and with a crowd?

**Phone controller**

- What is the one main action on the phone?
- Can a visitor use the control without learning a complicated interface?
- Does the phone need to show anything beyond controls and immediate feedback?
- Can the shared screen show the game state and the player's effect?

**Simple interface and rule communication**

- Can menus and long instructions be removed?
- Can a stranger work out the next action in about 10-20 seconds?
- Can the game teach through an obvious first interaction instead of a tutorial?
- What happens if a player misunderstands or makes an unhelpful move?

### Design principle

**Teach the next action through play; do not explain the whole game up front.**

For an exhibition, a visitor may only give the game a few seconds of attention. A clear goal, a simple phone control, and visible feedback should teach the loop. Keep behind-the-scenes details such as team balancing, disconnect handling, and reset rules out of the player's way unless they need to know them.

## 1. Tower-building / Jenga

### Core idea

Players collectively build the tallest possible tower. They move around and interact with blocks; the tower becomes less stable as it grows and may eventually fall. The current sketch includes pushing, picking up, placing, and possibly jumping.

Jonathan specifically likes the Jenga direction.

### Fit with my lens

- **Joining:** A new player can enter the current game and see the tower and its existing state.
- **Leaving:** The tower can remain as a visible contribution after players leave.
- **Phone:** A small number of movement and interaction controls could be enough.
- **Rules:** "Build the tallest tower" is a clear goal, and the effect of a placed block is visible.
- **One or many players:** The shared structure gives players a common focus, though crowding and interference need testing.

### Risks and possible mitigations

#### Risk: Players need to act at the same time or compete for the same block

- **Possible mitigation:** Make each placement a discrete turn or action that a player can take whenever they join.
- **Trade-off / test:** Turn-taking may reduce Jenga's energetic, simultaneous feel. Test whether it remains engaging without requiring people to coordinate.

#### Risk: It is unclear where blocks come from

- **Possible mitigation:** Try supply piles at the sides of the screen, with players moving a block from a pile to the tower.
- **Trade-off / test:** Extra piles and movement may add clutter. Test whether the source and destination are obvious.

#### Risk: The tower is already unstable or tall when a new visitor arrives

- **Possible mitigation:** Keep the current tower state visible and make the goal persistently clear. Reset automatically after a collapse.
- **Trade-off / test:** A reset loses the previous tower's progress; keeping rubble is more persistent but may be harder to understand and implement.

#### Risk: A player disconnects while carrying or moving a block

- **Possible mitigation:** Remove the avatar and return or drop the held block into a safe, visible state.
- **Trade-off / test:** Returning the block is predictable; dropping it may feel more physical but can make the tower harder to manage.

#### Risk: A player does not know how to move or interact

- **Possible mitigation:** Test a very small controller: directional buttons plus one interaction action, or a swipe/tap alternative. Highlight a usable block and show only the next instruction.
- **Trade-off / test:** A joystick, movement, pickup, and placement may still be too many controls. Test control comprehension with first-time players.

#### Risk: A player joins above the ground or away from the structure

- **Possible mitigation:** One idea from the notes is to spawn near the top with a parachute and let the player steer left or right while descending.
- **Trade-off / test:** This could be visually clear, but adds animation and movement rules. Compare with a simpler spawn beside the tower.

### Rule and screen communication

Try one short instruction at a time, such as **"Place a block to build the tower."** Show the available block and the tower as the visual explanation. Keep the phone focused on the next action; keep the overall tower and progress on the projection.

### Prototype tests

- Can a first-time player identify the goal and make a useful move without verbal help?
- What happens if the player leaves while holding a block?
- Does turn-based placement still feel like Jenga?
- Does the game remain understandable after a collapse and automatic reset?
- Is the screen still readable with 20-30 players?

## 2. Big-ball soccer

### Core idea

Players join one of two teams and push a large ball toward the opposing goal. New players could be assigned to the smaller team. After a goal, the score updates and the ball returns to the center without a lobby or a new match.

Jonathan likes the broad, playful potential, but said it is not yet clear how the large ball is pushed. He suggested a possible variation with 20+ balls and players joining either team.

### Fit with my lens

- **Joining:** The ball, goals, and score can communicate the current state to a late-arriving player.
- **Leaving:** An avatar can disappear without stopping the game; the score and ball state persist.
- **Phone:** Directional controls are simple, and the phone does not need to reproduce the soccer field.
- **Rules:** "Move into the ball to push it toward the goal" could be learned from a visible demonstration.

### Main issue: real-time dependence

The current idea relies on players pushing the ball in real time. Team balance and scoring also depend on who is present at the same moment. This conflicts with Jonathan's preference not to require synchronous play or excellent networking.

### Possible redesigns and risks

#### Risk: It is unclear how a player moves or pushes the ball

- **Possible mitigation:** Make the effect of one action highly visible; spawn a new avatar near the ball for its first move.
- **Trade-off / test:** This may help onboarding but does not solve the dependence on real-time play.

#### Risk: Uneven teams make play unfair when people leave

- **Possible mitigation:** Automatically assign new players to the smaller team and remove departing players from the active count.
- **Trade-off / test:** Automatic balancing reduces player choice and still assumes players are active together.

#### Risk: A goal normally implies a match reset or coordinated restart

- **Possible mitigation:** Update the score, return the ball to center, and continue immediately.
- **Trade-off / test:** Continuous scoring is simple, but players may not understand what happened unless the score change is obvious.

#### Risk: Real-time pushing conflicts with the client's preference

- **Possible mitigation:** Prototype a turn-based version where each player makes one discrete move or push, then the game updates. Consider the multi-ball variation separately.
- **Trade-off / test:** Turn-based actions could lose the physical, chaotic soccer feel. Test before treating this as a viable direction.

#### Risk: Many balls may make the screen chaotic

- **Possible mitigation:** Test a small number first and make teams, goals, and ball direction visually distinct.
- **Trade-off / test:** Clearer visuals may reduce the intended chaos; find the point where spectators can still read the game.

### Rule and screen communication

Keep the phone to movement or one push action. Put the score and goals on the projection. If a ball is pushed, make the result unmistakable so players learn the mechanic rather than reading a tutorial.

### Prototype tests

- Can one player make progress without waiting for opponents or teammates?
- Can players leave without stopping the game or making team assignment confusing?
- Does a turn-based push still feel like soccer?
- With many balls, can a visitor tell which team they are helping and where the balls are going?

## 3. Maze / collection

### Core idea

Each player controls an avatar in a maze and collects gems or other objects. The maze may change by moving or rearranging blocks. The concept could be individual and competitive, with player scores visible on the projection.

### Fit with my lens

- **Joining:** A new player can spawn into the maze and start collecting immediately.
- **Leaving:** Remove the avatar; the maze and other players' progress can continue.
- **Phone:** Four directional controls are enough for movement.
- **Rules:** "Move and collect items to score" is a direct, visible loop.
- **Player count:** The basic action does not depend on teams, so it could work with one player or several.

### Risks and possible mitigations

#### Risk: A timed maze change traps a player or blocks a visible goal

- **Possible mitigation:** Signal a change in advance, or make layout changes happen after a number of player actions rather than on a real-time timer.
- **Trade-off / test:** Warning players adds information; action-triggered changes may be less surprising.

#### Risk: A late player does not know what is happening

- **Possible mitigation:** Keep the collect-and-score goal visible and show the current maze and score.
- **Trade-off / test:** More screen labels may make the projection cluttered.

#### Risk: Players compete for too few objects or crowd one another

- **Possible mitigation:** Test object density and whether items respawn or are shared.
- **Trade-off / test:** More items reduce competition; fewer items may create more interaction but frustrate players.

#### Risk: A player needs to understand multiple rules at once

- **Possible mitigation:** Start with one action and one collectible; introduce changing walls only after the basic loop is understood.
- **Trade-off / test:** A simpler first version may be less distinctive.

### Rule and screen communication

The phone can show only directional controls. The projection should make collectibles visible and show the score changing when an item is collected. Avoid explaining a maze-change system before the player has learned to move and collect.

### Prototype tests

- Can a visitor collect an item within their first few moves?
- Does the game still work if only one person is playing?
- Are changing walls understandable and fair, especially if they block a route?
- Can someone join after the maze has already changed and know what to do?

## Client-requested directions to explore

These came from Jonathan's recent email and can be explored as variations or alternatives to the three concepts above.

### 4. Collective sorting task

**Core idea:** Players work together to sort a large mess of objects (for example, 100 objects) into the correct places.

- **Async potential:** Objects can remain sorted when a player leaves, and the task can continue as new people join.
- **Simple phone possibility:** Pick up one object and place it in a destination.
- **Rule clarity:** Use visibly distinct objects and destinations so the correct action can be inferred from the screen.
- **Main risks:** The sorting rule may need too much explanation; players may move the same object or disagree about its destination.
- **Possible tests:** Can a first-time player sort one object correctly without instructions? Can one action be completed at a time without waiting for a crowd?

### 5. Pixel-art block puzzle

**Core idea:** Players place scattered colored blocks into a target pixel-art image, in an order that accounts for blocks obstructing one another.

- **Async potential:** The target and puzzle state can persist between visitors; each person can contribute one move.
- **Simple phone possibility:** Move or push a block with directional controls and one action button.
- **Rule clarity:** Show the target image and highlight a block that can move.
- **Main risks:** Block order and obstruction may make the puzzle hard to read; an incorrect move could frustrate a player who does not know how to undo it.
- **Possible tests:** Can players identify a valid next move from the projection alone? What happens after a mistaken move or when someone leaves mid-action?

The block-puzzle direction may share mechanics with the maze/collection concept, but the goal is different: arrange blocks into an image rather than navigate to collect items.

## Comparison at a glance

### Tower-building / Jenga

- **Async / drop-in fit:** Strong if the tower persists and actions do not require simultaneous coordination.
- **Phone and rule simplicity:** Clear goal; block selection and placement need testing.
- **Main risk:** Shared physics, block supply, and what happens after a collapse.
- **Fit with Jonathan's feedback:** Promising; the client likes it, but test a turn-based version.

### Big-ball soccer

- **Async / drop-in fit:** Weak in its current form; players and teams act together in real time.
- **Phone and rule simplicity:** Directional controls are simple, but the push mechanic needs to be demonstrated.
- **Main risk:** Depends on real-time interaction and balanced teams.
- **Fit with Jonathan's feedback:** Needs major redesign to fit the preference for turn-based play.

### Maze / collection

- **Async / drop-in fit:** Strong if the maze persists and changes do not depend on real-time timers.
- **Phone and rule simplicity:** The move-and-collect loop is easy to show.
- **Main risk:** Moving walls may feel random or trap players.
- **Fit with Jonathan's feedback:** Potentially compatible after reducing real-time changes.

### Collective sorting

- **Async / drop-in fit:** Strong if players can complete independent, persistent actions.
- **Phone and rule simplicity:** Could be very simple if object categories and destinations are obvious.
- **Main risk:** Sorting rules and overlapping actions.
- **Fit with Jonathan's feedback:** Strong direction from the client; prototype one-object actions.

### Pixel-art block puzzle

- **Async / drop-in fit:** Strong if each move updates a persistent shared puzzle.
- **Phone and rule simplicity:** The target image gives a visual goal; move order may need explanation.
- **Main risk:** Obstructions and wrong moves can confuse or frustrate.
- **Fit with Jonathan's feedback:** Strong direction from the client; test whether the next move is visually apparent.

## A simple evaluation and testing framework

Test each idea in these situations:

1. **No players:** Does the projected screen still invite someone to join?
2. **One new player:** Can they understand the next action without an explanation?
3. **Several players:** Does the game remain readable and does collaboration or competition emerge?
4. **A player leaves:** Does the game continue and does their unfinished action resolve safely?
5. **A late arrival:** Can someone understand the current state with no earlier context?
6. **A crowd:** Does the screen remain understandable with 20-30 players?
7. **No simultaneous players:** Does the game still make progress without requiring people to act at the same time?

For each mechanic, document:

**Approach -> Benefit -> Risk -> Possible mitigation -> Trade-off -> Prototype test**

The aim is not to solve every design question now. It is to identify the uncertainty that matters most and make a small test that can answer it.

## Conclusion: Week 4 reflection

This week, I felt like I moved from brainstorming ideas to testing what actually fits a public, low-friction, drop-in experience. At the start, I was excited by the range of possibilities, but I quickly realized that the more interesting question was not which concept was the most elaborate, but which one would still make sense to a stranger walking up to the screen for five seconds. That shift in thinking was important for me. I started to see game design as less about inventing an impressive mechanic and more about designing a situation that someone can understand, join, and leave without feeling confused.

What stood out to me most was how strongly Jonathan's feedback shaped the direction. The idea of a game that works asynchronously, on a phone, and with simple rules became the lens through which I evaluated everything. Looking back, I can see that I was naturally drawn to more complicated systems at first, but the more I tested them against the real constraints, the more I gravitated toward concepts that were cleaner and more readable. The tower-building and pixel-art puzzle ideas felt promising because they had a clear visual goal and a simple action loop, while the soccer and real-time variants felt less suited to the project's goals.

I also noticed that the strongest concepts were not necessarily the ones with the biggest novelty. Instead, they were the ideas that could be explained in a sentence and still invite participation. That was a useful realization for me. I think this week taught me that the design challenge is not only about making a fun interaction, but about making a social, public, and accessible one. A player should not need a full tutorial, a long explanation, or a shared group context to understand what they are supposed to do. If the game can invite someone instantly, then it has already done part of its job.


////

the maze game, are we doing multi level or map and if so how do we show when a map can be done: timer ? or after all visible gem disapeared ? 
needs to be thought about as if a player join towards the end of the timer they could never gather a big score. however a visible timer identify the end of something so the player may realize that they can get familiar with the control and then 


/////