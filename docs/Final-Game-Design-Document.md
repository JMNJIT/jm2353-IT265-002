# IT265 Design Treatment

---

## Title

### *Fire Fight*

---
## Change Log
### Initial development 
- Took inspiration from card games like FLUXX, Explodiing Kittens, Unstable Unicorns, MTG
-- started developing a system that could utilize cards as "fuel," to direct the idea towards fire
- Created Ember cards, mimicing Keepers from FLUXX, but with abilities like the unicorn cards from Unicorns
- Created Action cards, those that would be consuming Embers as fuel.
- After creating action cards, took inspiration from Turn-based games, but hybridized the idea into creating Phases, group and solo duel
-- this idea guides a lot of the progress towards balancing and changing, and became the primary focus and namesake of the game
- Upgraded the Burn idea to be possible out of Fire Fight turns, and allowed card effects to chain

### Intermediate development
- Came up with Fighting Style / Ally cards, persistent cards that defined ways the cards would interact in the Fire Fight Phase
- Came up with Tarot Cards, large effects that changed the course of the game, in attempt to make the win condition malleable, and not as simple as just being the last standing
-- for simplicity, shelved. After early testing the game functioned fine without them, and implementing them was seeming complex
- In its place, Event cards came about, which could be played more freely and were able to affect other players hands/embers
- Received intermediate feedback as described farther below.
-- Some suggested changes, such as turn changes, adjustments to types, health, etc. (see feedback section)
- With the basic card types created, began drawing up a bunch of new cards and winging the effect descriptions, in order to build up the card base.

### Testing
- With the cards developed, a deck on ~50 cards made a real game possible. Tested with an intermediate 3 players, with an attempt at 4 proving to be too few cards.
- Emergent effects were realized:
-- Card effects cascade very well, but removed the "fast-paced" idea
-- There were some holes in how cards could interact, such as being able to affect on-table cards in one direction but not the other.
-- A few dominant-like strategies emerged, to be balanced.
- Generally positive experience!

### Physical Prototype Presentation
- Fixed the holes in the gameplay loop with additional cards
- Built up the card base more, filling in a lot of new strategies and playstyles
- Nerfed some card pairings that seemed to strong.
- Finished the art on many cards ahead of the presentation
- I think the presentation went well, it seemed not too confusing for the group, but I did not receive any specific feedback in that regard.

### Digital Prototype
- Created a sample project to start working
- Created Prefabs for player mats, as a basis for transforms for cards
- Started by creating individual scripts for type bases, like player, card types, hands, etc.
- created a number of functions on these base classes, for burn, play, and turn start effects
- with a game manager and turn manager script, started working on how  the flow of the game would go
- Quickly ran into some big problems, such as how the FF rotation would work, especially with differnt player count
- Struggled to start play effects on cards, and how they might link to burn effects and cascade.

- After a while struggling with the scene, among other issues, something in the project settings broke, and I was no longer able to access buttons or interact with the objects

- took the opportunity to start fresh, 

---
## Concept Statement
<!-- 
Provide a one-sentence summary that captures the core idea of your game. 
This should convey what makes your game unique in a compelling way. 
-->
A high-action Pyrokinetic card game where players fight fire with fire. Collect embers, and start duels with your opponents, and burn brightest.  

---

## Genre and Style

### Genre
<!-- 
Specify the game's genre (e.g., action, adventure, strategy, puzzle). 
Mention any sub-genres if applicable. 
-->
Action, strategy, PVP.

### Style
<!-- 
Describe the tone, visual approach, and gameplay feel. 
Examples: "A dark, gothic horror with hand-drawn 2D animation" or 
"A lighthearted, comedic party game with vibrant colors and exaggerated physics." 
-->
Bright, exciting, fast-paced. 

---

## Target Audience

### Demographics
<!-- 
Identify the target age group, interests, and gamer profile. 
Mention if your game appeals to casual or hardcore players. 
-->
Fantasy fans, Casual or serious card game enjoyers. 

### Accessibility
<!-- 
Describe how the game will accommodate different skill levels. 
Will there be difficulty modes, tutorials, assistive options, etc.? 
-->


### Inclusivity Strategies
<!-- 
Explain how the game promotes inclusivity. 
Consider gender representation, cultural diversity, and accessibility features for disabled players. 
-->
For Colorblind players, each item card type will have an Icon in the top corner which will correspond to its card type.
For less experienced players, Tarot cards can be removed to control randomness, or additional starting health may be added.

Unfortunately the game will rely on basic reading ability, as diverse card effects will be difficult to track without being able to read them.

---

## Core Gameplay Mechanics

### Primary Mechanics
<!-- 
List and describe the core gameplay mechanics players will engage with. 
Explain how they contribute to the game's challenge and fun. 
-->

**Cores** - Each player is given a Core card, and a number of tokens attached to it (balanced for number of players). A player is eliminated if they have no tokens remaining. 

**Embers** - Item cards which can have special effects. These are played from the hand face up in front of a player, with a maximum per player cap of 5 (Subject to change with prototype balancing). These cards will often be used as fuel for certain attack or event cards, and may be "burned" by Fire Fights and other players' effect cards.

**Events** - Cards which alter the flow of play. This may include altering the rules for the round, forcing a player to take a specific action, or drawing or discarding certain cards. These can be beneficial or harmful, and will state what their course of action is.  

**Allies** - Each player can have 1 ally card in play, which will provide special bonuses while active. These are placed face up in front of a player when played, and must remain separate from Ember cards. Allies persist through rounds, so long as the player survives. 

**Tarot** - Event cards with place specific restrictions or rule changes to the gameplay. Can be removed for simpler gameplay loop (i.e. boring people). Unless otherwise stated, only one Tarot card may be active at a time.

**Fire Fight (Duel)** - At the end of the round, if not during a grace round, the leading player may choose a target, initiating a 1-on-1 exchange of cards. Based on the player's Fighting Style card, they may be able to take different actions, such as playing items, attacks, drawing cards, or exchanging cards. There is only one duel per round, and once all card effects are resolved, play continues with the next player becoming the leading player for that round.

**Roasted Token** - To prevent targeting, the player last aggressed upon by a Fire fight is granted a token, which prevents them from being targeted before another player is first. If the player leads the round, they may still choose to be an aggressor.

**Winning the Game** - Players will win by default if all other players are defeated, by exhausting the tokens on their Core. However, certain Event cards may allow a secondary condition to be met first, securing victory in another way. This may be done by collecting a set of embers, winning a certain number of Fire Fights, or playing certain cards.


### Goals and Challenges
<!-- 
Detail what players aim to achieve and the obstacles they must overcome. 
Explain how these challenges drive player engagement. 
-->
Players will first aim to be the last one standing. In the final version of the game, some Tarot cards may change this objective.
Players will be challenged by numerous trade-offs and unpredictabiliy, as card effects may stack, cascade, or alter the flow of play suddenly.

### Progression
<!-- 
Describe how the gameplay evolves over time. 
Are there new abilities, unlockable levels, skill trees, or difficulty scaling? 
-->
More event cards and evetually Tarot cards will work their way into the game, creating dynamic shifts in goals and strategies as the game goes on. 

If the game is reduced to 2 players, some mechanics will change to make finishing the game easier.
- The Roasted Token will be removed.
- Healing will be capped to half maximum health.

### Game Rules
<!-- 
Outline the core rules governing the gameplay experience. 
Ensure they are clear, structured, and intuitive. 
-->
- The first round is a grace period, where no Fire Fights can be started
-- The leading player does not change in between the first and second round 

- Players may not have more than 3 Embers at a time unless a card states otherwise
- Players have a maximum hand size of 5 cards unless stated otherwise
  -- Players may draw above this limit during their turn, but must Discard cards down to the limit at the end of their turn
  
- Players may have 0 or 1 ally active at a time
- Whenever a player plays a card that they are at capacity for, they must burn (discard and resolve effects) a chosen card of the type, and replace it with the new card.

- Players can always begin their turn by drawing 3 cards
- Players can play any number of cards during their turn, excluding most attack cards.
- When a player is finished playing their cards, play moves to the next player Clockwise.

Fire Fights
- At the end of the Round, the leading player declares a Fire Fight duel with another player, unless they hold the Roasted token, where they may choose not to attack.
- Play starts with the leading player (unless stated otherwise), acting in accordance with their active Fighting style
  -- If a player has an action card that can be played, even if they do not have the embers necessary, they must play it, but its power will treated as 0.
  -- If a player has no usable action cards, their turn is skipped.
- When the Fire Fight is resolved, the difference of the two players' power totals for the fight damages the loser for that many HP
- Win or loss, the player who was aggressed receives the "Roasted" token, preventing them from being targeted for the next round
-- if the player is the next Leading player, they may choose to aggress at the end of the round.

- At the end of the round, All players draw to their maximum hand size (5 unless otherwise stated)

Rule of Thumb
- Most card effects must be resolved as stated on the card. Some are exceptions to general rules.

---

## Story and Setting

### Setting
<!-- 
Describe the game world, its rules, and any unique environmental elements. 
Provide enough detail to establish immersion. 
-->
Set in a Fantasy Dystopia, where magic causes the downfall of great cities, when pyrokinesis became the dominant form of magic in the world. The game is set in the aftermath of a war, where factions of pyrokinetics fight for resources, mastery of fire, and survival.

### Plot
<!-- 
Outline the central narrative arc. 
What is the player’s role in the story, and what major events drive the gameplay forward? 
-->
After the fall of the last empire, new Pyrokinetics were thrown into a realm of chaos and uncertainty. Though many sought to feed the chaos, factions formed, which sought to control their fire. This led to the creation of the Fire Fight, a duel of fire mastery which would establish strength and net resources to the winning faction. Though many parties continued to fight on their own, nearly all accept a Fire Fight as a final way to settle disputes. However, the use or Embers, relics which can grant additional power, some factions intend to subvert the balance and gain resources for themselves. Now, as more powerful, adaptable pyrokinetics grow, unrest grows and battles erupt.

For survival or for control, it's all about firepower.


### Characters
<!-- 
List key characters, their roles, and how they impact the story. 
Describe their motivations, personality traits, and influence on the player’s journey. 
-->
While there are few defined characters aside from the players, "characters" will exist in the form of Fighting Styles, cards which dictate how each player can attack during a duel. The characters are not associated with particular alignments, but the fighting style cards will feature art and information on specific characters in the world which utilize the style.

There are also Ally cards, which will show some NPCs of the world.

---

## Unique Selling Points (USP)
<!-- 
Identify what makes your game stand out from others in its genre. 
Highlight key features that differentiate it in the market. 
-->
The biggest selling points are the style, 1-on-1 dynamic, and the humor of the game. I was given positive feedback on the design and theme of the cards, so playing with an interesting design and a sense of humor in the tooltips and directions would work on me.

---

## Inspiration

### Sources
<!-- 
List books, movies, historical events, or games that influenced this project. 
-->
- *Fire Force*
- *Avatar: The Last Airbender*
- D&D
- MTG

### Why It Matters
<!-- 
Explain how these inspirations shape the game’s mechanics, visuals, or themes. 
-->
- These references helped me form a lot of ideas around the game, and defined a lot of my expectations. I took elements from them that I thought were most fun or inspiring, and tried to twist them into functions that I as a player would like to be able to do.

---

## Player Experience Goals
<!-- 
Describe the intended player emotions and reactions. 
Examples: excitement, curiosity, tension, relaxation, humor. 
-->
Excitement, tension, humor. Players should hopefully devise strategies to combine cards, or hope for the best and watch chaos unfold. There are many possible interconnections, so I hope emergence comes from the tension of staying alive and fighting your friends 1-on-1.

---

## Technical Requirements

### Platform
<!-- 
Specify where the game will be played (e.g., PC, console, mobile, VR). 
Mention any cross-platform support if applicable. 
-->
PC, console, mobile, are all possible. The most difficult implementation would likely be with certain card combos and the order with which effects are resolved. If that works, then cross-platform play should be simple.

### Tools
<!-- 
List key engines, programming languages, or frameworks required for development. 
-->
Unity, maybe even Tabletop Simulator. I code mostly in C#, so Unity is best for me. 

---

## Art and Sound Direction

### Visual Style
<!-- 
Describe the art direction, including color schemes, animation style, and UI elements. 
-->
Dramatic warm analogous color schemes broken up by start complementary colors, dark backgrounds for contrast.

### Sound Design
<!-- 
Explain the role of music, sound effects, and audio feedback in enhancing immersion. 
-->
Upbeat, heavy music would be best, keeping players excited.

---

## Monetization Strategy
<!-- 
Describe how the game will generate revenue. 
Examples: one-time purchase, freemium model, ads, DLC, cosmetics, subscriptions. 
-->
The easiest option in my mind for a game like this is a one-time purchase with additional paid DLC. The game's simple framework would easily allow for the addition of more cards and strategies in the future.

---

## Treatment Details

### Gameplay Example
<!-- 
Write a step-by-step walkthrough of a core gameplay scenario. 
Explain what the player does, the challenges faced, and how the game responds. 
-->
The most difficult scenario would likely encompass lots on quick-time elements stacking at once. A player could be drawing at the beginning of their turn, and pull multiple event cards. These would need to be resolved in sequence, but may have conflicting results, or cascade with chaining burn effects in the ember or ally cards. On top of this, there are a few cards which may be played out of turn, which could further complicate the round. The game's cards should be able to dictate the response when gone through in sequence, as most cards have additional notes for possible outcomes.

---

### Challenges and Considerations

#### Potential Risks
<!-- 
Identify elements that could fail or require refinement. 
Examples: balancing issues, unclear mechanics, technological constraints. 
-->
Currently, the biggest roadblocks will be balancing and technological constraints. There are some rules which may be difficult to understand, but at this moment I predict that the game's effects stacking may be the most dangerous. it is possible for a player to be eliminated as early as the second round, or possibly not until many later rounds. I have not been able to do extensive testing yet, so this will be easier as more experience is gained.

#### Feasibility
<!-- 
Describe any technological, financial, or development constraints. 
How will you mitigate these risks? 
-->
It's a technically intensive game, with a lot of features that cascade into each other. I'm not sure how ready I am to do all of the features, but at the very least I want the flow of the game to be followed.

---

## Visualizing the Game Concept

### Concept Sketches or Storyboards
- Provide at least **two sketches**  
- Ensure sketches accurately represent the game’s concept and theme  
- Maintain coherence with the game’s style and theme  

<!-- 
Upload sketches here, or describe the key visual elements in detail if unavailable. 
-->

![image](https://github.com/user-attachments/assets/282169fe-608e-4afc-be49-015a59ac741a)

![Fire_Fight sample cards](https://github.com/user-attachments/assets/57f2cb52-ea8d-465a-9ee3-cc8dcbc489ab)

![image](https://github.com/user-attachments/assets/3d6ce833-ae2c-4678-a945-a60b21c973c1)


---

## Pitch Preparation

### Pitch Summary
<!-- 
Provide a concise and engaging summary of the game concept and theme. 
Make it persuasive and easy to understand. 
-->

*Fire Fight* is an action twist on classic card games like *Exploding Kittens* and *FLUXX*, where diverse effects to the gameplay loop and modifiers to each player's playstyle can result in unique emergent strategies. The game is stylistically and thematically unique, and pulls from a variety of popular sources using fire as a medium. The game hopes to be an aggressive and fast take on the couch card games, allowing players to duel specific players or work together to maintain a chaotic balance. 

The game hopes to appeal to its demographic with interesting card art, and themes like DnD-like magic, Tarot Cards, and controlled randomness. For players who have played similar games before, the game hopes to break away from the same gameplay loops by introducing different game states, but remaining not too far out of players' experience, such that they may pick up the style quickly.

No other game uses pyrokinesis as a theme and few allow players to independently duel. With strong visual appeal and high replayability, the game aims to add a spark of originality in the tried-and-true.


### Target Audience Appeal
<!-- 
Explain how the game connects with its intended audience. 
What elements make it particularly appealing to them? 
-->
It is stylistically dynamic and unique, taking reference from some palettes and designs from popular media.

### Market Differentiation
<!-- 
Describe what makes this game unique in the current gaming market. 
Compare it to similar games and highlight key advantages. 
-->
The game has a unique style and set of mechanics, most notably the end-of-round duels. It features a diverse amount of effects and a good sense of humor surrounding its logic.

---

## External Feedback
<!-- Duplicate Feedback group as necessary if beyond 3 -->

### Feedback 1
Mason Colon, Roommate (by his request: "reviewed by Mason - card game expert")
He gave me a lot of organizational feedback, focusing on how turns run, and where Fire Fights can happen
as opposed to who can play first. He also suggested the addition of some basic player actions, such as
discarding cards. He also suggested changing the mechanics on Fireball and ally cards to help with balance.
He had a lot of comments, so I cannot go through them all here. This feedback helps with shaping the foundation of the game, how players interact and how the flow of the game works. He suggested a lot of models from other game examples which helped give me some more context to what I should and should not mirror, so I think his feedback will be very useful for the prototyping section.


### Feedback 2
Rick Mohring, my Dad, NJIT Alum. + board game enjoyer, etc.
He pointed out some inconsistencies in my description of certain game rules, such as the grace round, and
encouraged me to give it more structure. On the style of the game, he agreed that it was original, but did not
seem as drawn to it aesthetically as my friends, which confirmed my ideas about the demographic that the
game willappela to. He did, however, agree that the artstyle will be a good selling point with effective use of
color. This feedback is useful as well, as sometimesI flesh an idea out in my head more than I have on paper, and
thus it may not integrate as well as i tmougnt, or will point out exampies where it is mroe difficult for a piayer
understand than it is the creator.


### Feedback 3

Kapila Mane, Friend from high school & in my D&D group
She focused on the aesthetic parts of the game first. She found the basic mechanics easy to follow, but
suggested some additional clarity on the use of Fighting Style cards and how they would interact with the
loop. She suggested making alterations to them such that more cards would be available per round, to make
more actions possible and increase player actions/gameplay pace.
I was glad that she liked it aestetically, as I think the style is a big selling part ofthe game. This will definitely
help with my considerations of the gameplay loop. Overall, the feedback revealed some holes in the logic of
the game, but supported the concept and style. I want to continue using the style I started with, so I am glad
that it seems successful.



---

## Appendix
<!-- 
Include any additional sketches, mood boards, or early design mockups if available.  
If digital assets are unavailable, describe any rough concepts you have in mind. 
-->

---
