# GDIM 33 In-Class Activities
## W1
### Activity 1

[Inspiration Board](https://miro.com/app/board/uXjVGoFH8zY=/?share_link_id=108447704132)

1. Some patterns I noticed in my inspiration is a lot of outdoorsy related stuff. I think I really like games with visuals that tend to pop out. They games are all unique in their own way. One specific visual aspect that I thought was really interesting was 2.5d or 3d games because of how they are able to manipulate the camera angles.

2. My table-mate Sonia is a big fan of the beach and sports like tennis and soccer. They are interested in building a game related to the beach. She is still contemplating what style of game she wants to build, but definitely something beach themed. We both listed sports as things that inspired us and interested us. We also both liked the outdoors and nature scenery.

3. Elijah came to our table and mentioned that he really liked puzzle platformers. He specifically mentioned that he enjoyed Machinarium and recommended us try it out. My tablemate also really liked 2d-platformer games and thought his recommendation was really cool!


### Activity 2

1. Genre: 3D Cozy Camping RPG

2. Gameplay Loop & Mechanics:
- The player arrives at a campsite and must survive by exploring the world, gathering materials, and managing resources across a day-cycling system.
- Each day, the player experiences gentle pressure from hunger and cold, incentivizing them to find food and craft shelter/fire before nightfall.
- Core actions include exploring to discover materials, gathering via interaction, crafting items, and bartering with a wandering trader.
- Building shelter and fire reduces survival damage, allowing the player to rest and advance to the next day. The cycle repeats with increasing environmental challenges as seasons progress.

3. Breakdown Diagram
<img width="813" height="533" alt="Screenshot 2026-04-01 at 7 32 57 PM" src="https://github.com/user-attachments/assets/420245dc-b486-4c22-92c0-bf8a5a910e8f" />


## W2

### Activity 2 

*See changes pushed

## W3 

### Activity 1 
Updated Breakdown Diagram 

<img width="1047" height="720" alt="Screenshot 2026-04-15 at 7 27 51 PM" src="https://github.com/user-attachments/assets/47eb01d1-b827-4e69-b25a-52bf641e8799" />

### Activity 2 

1. Saving "clickWalrus" as a Scene variable named clickNpcEventName means any graph in the scene can reference that same variable instead of typing the string manually.
   If the event name ever needs to change, you only need to update it in one place instead of than hunting down every graph that hardcoded the string.
   
3. After wiring up the OnMouseDown event in the walrusW3 Graph, I added a Debug.Log node directly after the custom event trigger. Before I had any feedback in
   the game, I could open the Console and confirm whether clicking the walrus was actually firing the event at all. When the transition Debug.Log in the gameStateW3
   Graph also printed, I knew both ends of the chain were working: the walrus was sending the event and the state machine was receiving it. Without those nodes, it
   would be hard to pinpoint the location of the error in this chain of nodes. 
   
5. The cursor lock state is relavent to my vertical slice because the game is played in a third person perspective. The cursor is locked and hidden during the main
   exploration so the player isnt distracted by a visible pointer while moving and exploring the environment. The cursor will be unlocked when the player needs to
   do any UI interactions, like opening the crafting menu or interacting with oth UI elements. This activity helped me better understand what cursor lock is and
   how to implement it in my vertical slice. 
   
7. Game states are highly relevant to my vertical slice. The project has several states that require different systems to be active or inactive; an Exploration state
   where the player moves freely and survival meters tick down, a Crafting state where the world pauses for UI interaction, a Death state where movement stops and the
   player respawns at the shelter, a Day Transition between each of the three in-game days, and a Win state after the third day is survived. A state machine is the best
   fit for managing all of this, using On Enter State to enable or disable the right components and custom events to trigger transitions. This activity helped me understand
   how to better implement this into my vertical slice. 
