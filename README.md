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

## W4 

### Activity 1 
Playtesting 
Group Members: Pinhsuan Wang, Sonia Mangat, Rebecca Han

1. The current build is basic movement with animations attached to WASD. The player should be able to walk in the procedurally generated world. The camera should be able
   to follow the player around from a third person perspective. The movement should be still be intuitive no matter which direction the player is looking.
   
3. Goals for playtest: Ensuring animations load correctly with player movement. Ensuring camera perspective is correct and is following correctly.
  
4. The animations walking foward sometimes is loading the backwards walking animation. The walking animation only seems to be loading correctly when facing true north. There also seems to be some holes in the map generation near the rock/hill assets. The player doesnt fall through but there is a visual discrepency with being a hole in the ground. 

### Activity 2 
1. Yes, this can be complteted without writing a single line of code. Since each dialogue node is a Scriptable Object, the writer can create new ones directly in the Unity Project window, fill in the Line and Reply options
   and link the nodes together through the inspector without having to touch any scripts, graphs or code. 
3. There should be no limit. The writer can create as many dialogue nodes as they want since each one is just a Scriptable Object asset.
4. Regenerating the nodes refresehes the Visual Scripting Nodes to match the current state of their scripts. If anything is modified in the class, the nodes referencing that class in the graph is now outdated.
   Regenerating the nodes updates them to the latest version so the graph is still in sync. Its similar to refreshing a tab to see new changes.

## W6

### Activity 1
1. Things that are new in this version of the vertical slice is the campfire and cut scene. When the player is interacting with the campfire at night, they are able to speed up the night cycle. Players are also able to now
   craft items in the UI screen. The only craftable item currently is the campfire. 
2. [Itch Link](https://andrewxuu.itch.io/snow-peak-demo-3) 
3. Testing Goals:
   - Main priority: checking if inventory system works as well as crafting system. 
   - Secondary priority: checking if campfire cutscene works, camera pulls into correct position and timelapse occurs.
4. Notes:
   - the campfire is missing UI to tell player to trigger the scene
   - issues with placement mechanic, possible collider issue
   - should add some UI notification to tell player campfire sleep interaction is only available at night

### Activity 2 
1. Multiply makes the color darker and less saturated because the RGB values are stores as floats between 0.0 and 1.0. When two of these values are multiplied, they will always produce a result smaller than or equal to either input. Only way for them to remain bright is if one of the numbers is fixed at 1.0.
2. More translucent (lower alpha). It is the same idea as the answer above, the two float values are between 0.0 and 1.0. When they are multiplied, their values will always produce a result smaller than or equal to either input unless one value is 1.0.
3. The UV coordinates come from the mesh. When the 3d model is unwrapped, it forms a flat 2d map. These UV coordinates are stroed as vertex data on the mesh. 
4. I think there is something satisfying about playing around with the visuals. I think its interesting to be able to make such visual changes like tinting, transparency, blending and color manipulation in a predictable and reproducable way with just simple arithemetic. I think this gives me a better appreciation for math and its relation to art.

## W7 

### Activity 1 
1. The vertex color comes from the mesh itself. The color is stored in each vertex as part of its mesh data. 
2. The color on the shiba in step 3 is  blended at the edges becasey the color is defined only at each vertex not polygon.
3. The shiba from step 3 less detailed because the vertex color is limited by the number of vertices in the mesh. There can only be as many distinct color points as there are vertices. The textures can have far more pixels than a mesh has vertices, hense they carry much more detail in the color. 
4. Yes, the back left leg looks wrong. The color doesnt match the normla direction pattern. 
5. You could debug using the UV coordinates by outputting them as a color. This would help verify that the UVs are laid out correctly and not distorted, flipped or missing. This can help explain texture stretching or misalignment. 
6. the light direction vector points towards the shiba, while the surface normals point away from it. The two vectors are pointing in opposite diretions, creating a negative dot product making lit areas appear dark. The solution is to multiply the light by -1 to fix this.
7. I think we set the blend mode to additive for the fire effect in step 5 because the additive blending adds the shader's color on top of whatever is behind it. It makes bright areas glow and darker/transparent areas invisible. This is ideal for the fire because the fire emits light and brightens the scene. 


## W8

### Activity 1 
[Itch Build](https://andrewxuu.itch.io/snow-peak-demo-4)

Updates since last build
- Players are able to craft tools like the axe and pickaxe. These two items should be able to speed up the chopping progress. The big update since last build is the snow shader and particle effect. During night, snow will build up which will affect the player movement speed. This will also lower the player warmth bar, when the player is too cold they will freeze and lower their health bar. Players are able to stay warm during the night by being near the campfire and fueling the campfire with wood. 

Playtesting Goals: 
-Testing shader and particle effect functionality 
-Balancing the player crafting and seeing if the item is being properly holding in the player hands 
-Checking warmth and health bar functionality
-Checking if fireplace warmth system works at night 

Playtesting Notes: 
1. Snow Shader & Particle Effects
   - The snow looked really cool at night, didn't expect it to start building up on the ground
   - Wasn't sure at first if the snow was affecting my movement — it felt slower but I thought my character was just tired
   - No visual indicator that snow is slowing me down, would be nice to have some kind of hint
   - Snow particles felt a little heavy/dense, almost too much on screen at once
   - Transition from day to night was smooth, liked how the snow gradually picked up
2. Crafting & Item Holding
   - Player item holding position is weird
   - Crafting felt easy and straight foward
   - Could balance item crafting cost more
3. Warmth & Health Bar
   - Warmth bar drained pretty fast once night hit, felt a little punishing
   - Wasn't immediately obvious what the warmth bar was — mistook it for a stamina bar at first
   - When it froze, it wasn't clear why my health was dropping, no tooltip or feedback
   - Health bar dropping felt very sudden, went from fine to almost dead quickly
   - Would appreciate some kind of warning before the freezing starts
4. Fireplace Warmth System
   - Works lol.
   - Warmth radius felt decent
  

  



