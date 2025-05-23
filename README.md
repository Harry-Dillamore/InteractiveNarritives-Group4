# InteractiveNarritive-Group4
Harry Dillamore

2402521

## Research
### AI / Zombies
#### Aims
We want the zombies in the game to have different types which will determine their attributes and behaviors. The types we have come up with as a starting point are:
- Regular: Slow moving, 'traditional' zombies. The majority of the zombies will be this type
- Scouts: Faster zombies with ability to track and follow the player
- Leaders: Similar to regular zombies but more intelligent, with the ability to alert nearby zombies of the player's location.

For these types I will need to research how to adjust the senses and behaviour of AI characters and find out how to allow for some level of communication between them.  

#### Examples
###### The Last of Us
In *The Last of Us (2013)* The zombie like enemies have an in depth progression from when they first get infected and have mostly human characteristics (Runner, 2025). To when they have been infected for much longer and gain abilities such as echolocation and have less human physical characteristics (Clicker, 2025).

<img src="https://images.steamusercontent.com/ugc/913534958639653803/1FAC12D23FA522F70EE1760A4C80E09B1123AF69/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false"/>

*Figure 1 - types of infected in The Last of Us*

In *The Last of Us* the different infected types are gradually introduced in order to create more varied and interesting gameplay and deepen the narrative. Allowing players to learn and their behaviours and the best tactics for dealing with them, as well as learning the reason they exist and have the characteristics they do. 

I believe that this exemplifies an ideal way of implementing different types of enemies. But also makes clear that this works best over a long period of gameplay so that they player can encounter the types one by one before they are combined - avoiding the player feeling overwhelmed or confused. For this reason we may want to consider having more subtle differences between enemies in order to keep the variety and narrative depth, while allowing the player to quickly understand and respond to the types of enemies. 

#### Tutorials and Resources
###### Documentation on AI perception in UE5 (AI Perception in Unreal Engine | Unreal Engine 5.5 Documentation | Epic Developer Community, s.d.)
This documentation goes over the different types of AI perception such as sight, damage and hearing. This can be applied to our zombie AI by allowing us to give the different types of zombies varied abilities in each of these areas of perception - e.g. one type could have very good hearing but bad sight, while another type could have the opposite.

<img height=400 src="https://img.edc-cdn.net/imgproxy/EIKVPAwxHc2oML8yucZgGV8o-3dNe1EHjTlgtFFkwJg/filename:perception-sight.png/resizing_type:fit/width:1400/height:829/enlarge:true/aHR0cHM6Ly9kMWl2N2RiNDR5aGd4bi5jbG91ZGZyb250Lm5ldC9kb2N1bWVudGF0aW9uL2ltYWdlcy83OTY5YmZiOC02YzRiLTRjZGMtODQ3Ny0wM2U0MzI0OTZiMjkvcGVyY2VwdGlvbi1zaWdodC5wbmc"/>


<img height=400 src="https://img.edc-cdn.net/imgproxy/7kcJpwjPjrjU2YcT1vLHUpSf4x6xp5hx2UupD3A1TU4/filename:perception-hearing.png/resizing_type:fit/width:0/height:0/aHR0cHM6Ly9kMWl2N2RiNDR5aGd4bi5jbG91ZGZyb250Lm5ldC9kb2N1bWVudGF0aW9uL2ltYWdlcy9jZGNhYzFiYi1hNmViLTRjODYtOGYwOC1jMjUzNjY3OWMzNGMvcGVyY2VwdGlvbi1oZWFyaW5nLnBuZw"/>

Another key feature detailed in this documentation is AI teams, which is a function allowing AI to create a stimulus to broadcast to nearby AI agents on the same team. This can allow for coordination between enemies - which, in our game, would give the player reason to avoid larger groups of zombies as they will be able to spread information of the player's location.

<img src="https://img.edc-cdn.net/imgproxy/jLY09Yw8iQ1JE53QUHgUMJnyA12vKL1Ef7pHsGzqAUs/filename:perception-team.png/resizing_type:fit/width:0/height:0/aHR0cHM6Ly9kMWl2N2RiNDR5aGd4bi5jbG91ZGZyb250Lm5ldC9kb2N1bWVudGF0aW9uL2ltYWdlcy9jZTYxODU5Zi1hMWFkLTRlZWQtYmIzMy1hMmMzMWY1ZjhiMmYvcGVyY2VwdGlvbi10ZWFtLnBuZw"/>

###### Zombie AI Tutorial (Survival Game - Behaviour Trees & AI Senses (Section 3), s.d.)
This article and videos outline how to set up an AI which detects the player using sight and hearing using C++ and a behaviour tree. It covers important details such as using a custom AnimNotify to trigger the player's footsteps at the right point in their animation. It also shows an example of the AI's behaviour tree which controls what actions the AI performs, such as moving towards the player if they are sensed or patrolling if they are not. Overall, this tutorial gives a very good starting point for the AI in our game that we will be able to build upon to add some complexity and variation in the behaviour of.
- - -
### Combat
#### Aims
While combat is not the focus of the game, and we do not want the player to be able to kill zombies in order to progress, we do want the player to have some options for defending themselves. The methods we plan to experiment with are:
- Slingshot / throwing stones – giving the player a slingshot or something similar that would not do much or any damage to enemies, but would be capable of causing distractions that they player can take advantage of to get past zombies.
- Pushing enemies – we want to give the player a melee attack which allows them to stagger and push back zombies, but not kill them. The purpose of this would be to give the player some agency to get past zombies when they are blocking the path, while keeping them as a formidable threat and meaning that a group of zombies is still very difficult to get through.

#### Examples
###### Spider Man (Marvel’s Spider-Man, 2018)
In the spider Man games, there are stealth missions in which the gameplay is based around avoiding detection and distracting enemies in order to get past them. In these levels, the player has various options such as interacting with environmental objects and performing takedowns on isolated enemies if certain conditions are met.

<img alt="alt text" src="https://i.redd.it/eyln83zyg1nb1.jpg"/>

One element of these levels in the *Spider Man* games that we want to avoid is having the level fail when the player is spotted. This is because we want it to be the player's choice whether they commit fully to stealth or allow themselves to be spotted and attempt to make it past the zombies before they can be caught. We will also likely reduce the player's ability to completely take down enemies, but introduce an attack to briefly push them back or out of the way allowing the player to make a path through enemies to some degree. I think that this will help to mitigate some of the frustration that players find when playing stealth games as it gives them the choice of how to play.

#### Tutorials and Resources
###### Video on Distracting Enemies With Noise (How To Distract An Enemy With Noise | AI Hearing – Unreal Engine 4 Tutorial, 2021)

<iframe width="560" height="315" src="https://www.youtube.com/embed/w0t75DdkazU?si=O9R0JrMeBcF1LWG0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

This video goes over a similar concept to the slingshot we are considering implementing. In the video they demonstrate how to allow the player to throw an object which makes noise, and how to get the AI to then investigate this sound. The steps include, creating the object, then adding an input which spawns the object with a velocity based on the direction the player is facing, and broadcasts a sound which the AI are able to detect upon impact.

###### Video on UE Combat System (How To Create A Melee Combat System in Unreal Engine | Full Tutorial Course, 2023)

<iframe width="560" height="315" src="https://www.youtube.com/embed/wZ11YqdidFA?si=KZgI9RcOPzAjoyLk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

In this video and the following videos in the tutorial series detail creating a melee combat system. The system demonstrated is not quite the same as what we currently have planned for our game – as it allows for the player to defeat the enemies, but we're looking to limit the player's ability to defeat enemies. To make these changes, I will reduce or remove the damage dealt to enemies, as well as increase the hit reaction from enemies to create a more prolonged stagger effect.

### Cutscenes and Quick Time Events
#### Aims
In the game, we want to blend short cutscenes with gameplay to create cinematic moments without making the player feel like they don't have control of the characters' actions for long periods of time. This will allow for dynamic sequences and moments where the narrative can be developed, while keeping the gameplay as the main focus. 



## Implementation
### Zombie AI
As the zombies will be a core part of the gameplay - being the main obstacle that the player must get around in order to progress the narrative - I have decided to start implementing the zombie AI straight away. This will allow me to develop the AI behaviour and make improvements throughout the project. This is also something new to me so I want to avoid leaving it too late, and not having time to implement the AI the way we want.

To begin with I made a simple AI which followed a random roam sequence then chased the player if they could see them. To implement the sight perception I followed this tutorial:

<iframe width="560" height="315" src="https://www.youtube.com/embed/bx7taRBjJgM?si=D0qFL7R-SdOLYg3y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

*AI sight sense:*
<iframe src="https://blueprintue.com/render/du8jkqa5/" scrolling="no" allowfullscreen height="500" width="100%"></iframe>

The AI behaviour tree at this stage consisted of telling the AI to roam to random nearby locations if there was no target player and to chase the target if one was set.

<img alt="img.png" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/image-1.png?token=GHSAT0AAAAAADELVC76CCJ3DXXTBLEZYE6C2BQR4SA"/>  

#### Combat
As mentioned in my research, I want there to be level of combat that allows the player to stagger the zombies in order to get past them. Below is the blueprint which added the ability to attack AI characters. It starts an animation and then does a sphere trace around the hand the player is using to attack, triggering the hit event on the zombie blueprint if it collides with one. We decided that the player should not be able to kill the zombies so the attack serves more as a way to stun the enemies and then escape.

I also made a variation on this sequence which would allow the player to attack using a gun by changing the trace to a line trace projecting forward from the camera. However, the gun never got fully implemented so is not used in the game.

When I made this code, I had an issue where the AI would play the animation of being stunned - but did not have the correct logic in the behaviour tree for them to stay still while the animation played. I was able to fix this by updating the blackboard key 'Hit' and using it as a decorator which aborts the normal behaviour of the AI.

*Player punch:*
<iframe src="https://blueprintue.com/render/5bxo5ikt/" scrolling="no" allowfullscreen height="500" width="100%"></iframe>

*Punch trace:*
<iframe src="https://blueprintue.com/render/5u4wxb4t/" scrolling="no" allowfullscreen height="500" width="100%"></iframe>

*Zombie hit:*
<iframe src="https://blueprintue.com/render/xhx1q2po/" scrolling="no" allowfullscreen height="500" width="100%"></iframe>

Next I was able to use a very similar system to allow the zombies to attack the player once they have reached them, The main difference being that I added some vignette and chromatic aberration to the players screen each time they are hit to signify how damaged they are. On hit I also added some screen shake and a red flash to the screen. The number of times the player has been hit is kept track of and the effects are amplified each time, until the third time, where the player is respawned.

*Player hit:*
<iframe src="https://blueprintue.com/render/v9lg7wu7/" scrolling="no" allowfullscreen height="500" width="100%"></iframe>

The other core part of the combat system I wanted to implement is causing a distraction, in the team we discussed using a slingshot or some other item to throw things. However, the assets were not ready at the time I was implementing this so I stuck with simply throwing a stone. The aim with this mechanic is for the player to have a way to move the enemies out of their way by causing a distraction which they would go and investigate. This is done through audio perception which is picked up by the AI and they prioritize investigating the sound over their regular roaming sequence, with the investigation then being aborted if they spot the player.

*rock blueprint:*
<iframe src="https://blueprintue.com/render/ps7foz-s/" scrolling="no" allowfullscreen height="500" width="100%"></iframe> 

*Throw rock:*
<iframe src="https://blueprintue.com/render/er04adma/" scrolling="no" allowfullscreen height="500" width="100%"></iframe> 

I was able to use similar logic to allow a zombie who has spotted the player to use a sphere trace to find nearby zombies and broadcast the player's position as a location to investigate.

*Broadcast player position:*
<iframe src="https://blueprintue.com/render/-9ahkawg/" scrolling="no" allowfullscreen height="500" width="100%"></iframe>

*AI blueprint*
<iframe src="https://blueprintue.com/render/v5ba9_ga/" scrolling="no" allowfullscreen height="500" width="100%"></iframe>

*Final behaviour tree:*

<img alt="Final Behaviour Tree" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/image-2.png?token=GHSAT0AAAAAADELVC76MINSO76ZRXXEXAVY2BQR6ZA"/>

<img alt="alt text" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/ScreenRecording2025-05-23101152-ezgif.com-video-to-gif-converter.gif?token=GHSAT0AAAAAADELVC76QVKOISV7FWVEY6DM2BQR77Q"/>

<img alt="alt text" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/ScreenRecording2025-05-23100751-ezgif.com-video-to-gif-converter.gif?token=GHSAT0AAAAAADELVC77GCKIASBQIFGJW6S22BQSAZA"/>



### Autofocusing and Atmospheric Effects
In the level, I adjust the exponential height fog to render volumetric fog and increased the density. I also added a HDRI backdrop to change the feel of the environment, edited the post process volume to add some subtle camera effects and to adjust the exposure of the scene to better fit the feel we wanted in the game. I watched the following video to understand these effects and inspire the final look of the scene.

<iframe width="560" height="315" src="https://www.youtube.com/embed/fBosP7fVJug?si=C4T5xkBi3pSoiDLp" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

I added an autofocusing system so that the game could have a strong depth of field effect, which works to enhance the atmosphere and to draw the player's attention to the models and textures made by the artists. The system works by making a line trace every 0.2 seconds which returns the distance from the camera to the first object that the line trace hits. The camera focus distance is then adjusted to match. I followed a video tutorial on setting up the autofocus system.

I encountered a problem where depth of field system functions correctly when moving to focus on a closer object. However, when the focus shifts to an object which is further away, there is no gradual transition.
After testing the issue in different scenarios, I found that the problem was generally caused when there was a big difference in the original to the target focus distance. This showed that the issue was not that the transition was not happening, but that it was happening too quickly. Therefore, in order to fix the issue, I was able to limit the maximum focus distance so that it was never transitioning too far. This made the effect look much smoother.

another issue I encountered was that the camera was not focusing on enemies, to fix this I had to ensure that the trace hit the collision of the zombies. This produced better results but I observed that because the collision did not match the mesh of the zombies, the focus was slightly off. The solution for this was to use the mesh of the zombies rather than the capsule collider to calculate the distance for the depth of field.

<iframe width="560" height="315" src="https://www.youtube.com/embed/TvXJdDSHzro?si=3FJHMuZ97PH3QEKt" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<img alt="trace fail" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/ScreenRecording2025-05-02124714-ezgif.com-video-to-gif-converter.gif?token=GHSAT0AAAAAADELVC76RWLWWMEL5O4WVRMM2BQSDBA">

<img alt="trace partial success" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/ScreenRecording2025-05-02124923-ezgif.com-video-to-gif-converter.gif?token=GHSAT0AAAAAADELVC76BOJMJI6Y2CZFREBQ2BQSDBQ">

<img alt="trace partial success" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/ScreenRecording2025-05-02125553-ezgif.com-video-to-gif-converter.gif?token=GHSAT0AAAAAADELVC76NID45WOGNIOEPGWW2BQSDCA">

### Interactions
I created a mechanic which allows items to be interacted with, the purpose of this is to allow players to investigate certain items which will contain information about the game world which is not important to the gameplay, but adds environmental storytelling for players who are interested in learning the backstory and additional information about the game. The effect uses the line trace created by the depth of field system to check if the item that the player is looking at is able to be interacted with, then applies an outline material to the object if it is. To create the outline material, I followed the following tutorial:

<iframe width="560" height="315" src="https://www.youtube.com/embed/rGqlReFObYQ?si=FgYwc6mj9f51My-i" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Then when the player presses the interact key, the item is lifted to be in front of the player and rotated to face them using position and rotation lerps. The player is then able to rotate the item in the air using the mouse, meaning they are able to view it from whatever angle they want to. while the item is being interacted with, the player movement and rotation is locked to avoid any issues, then when the player presses the interact key again the item is returned to its original position and rotation. 

<img alt="Item Inspection" src="https://raw.githubusercontent.com/Harry-Dillamore/InteractiveNarritives-Group4/refs/heads/main/ScreenRecording2025-05-23084631-ezgif.com-video-to-gif-converter.gif?token=GHSAT0AAAAAADELVC76QIQILBN7R5I7BPMI2BQSFCQ">

Final blueprint for interactions:
<iframe src="https://blueprintue.com/render/rf5j5rny/" scrolling="no" allowfullscreen height="500" width="100%"></iframe> 

### Other Features and Tasks
There are also a number of smaller mechanics and features that I implemented during the project, particularly during the last week where it was apparent that features that had previously been delegated to others were not going to be implemented unless I took them up.

#### Audio
The team member that claimed they would take care of the audio did not show up for the majority of the project. So I found some free sound effects to put into the game where I could, but was unable to do this for everything due to time constraints and the other responsibilities I had in the project.

#### Menu
I made a main menu using widgets which allows the player to start the game, view the controls or credits, or quit the game. This menu is displayed when the game is first opened. The menu is also supposed to show when the player reaches an ending of the game, after the cutscene is played - however, because the cutscenes were not able to be put into the game in time, I was not able to implement this. (How To Create A Main Menu System In Unreal Engine 4 | UE4 Tutorial, 2022)

#### Zombie and Player animations
After the zombies and player models were rigged by Izzy, I was able to download Mixamo animations which I then used to create animation blueprints which check the speed of the owner and apply appropriate animations to the model. As well as creating anim montages which were used for the various attacks. This is something I have next to no experience in prior to this project, so it was a great skill to learn. 

#### Compass
When finding out how wide of a map we were going to have, it was suggested that we use a compass or minimap to help the player navigate to points of interest. So I followed a tutorial on creating the compass widget and adding components to actors which make them show up on the compass. (Unreal Engine 5 Tutorial -  Compass Part 1: UI, 2023)

#### Fixing Meshes
The buildings that we received from the artists had messy collision that meant the player was not able to walk inside them properly, I was able to clean up the collision and use the complex collision instead of simple to allow the player to navigate the interiors better.

#### NPC Idle Animations
I found that none of the NPCs had idle animations, and no one had plans to add them so I found some idle animations on Mixamo that I could apply to the skeletons. However, I could not figure out what skeleton had been used on one of the NPCs so rather than spending too long on it, I moved on to tasks that were of a higher priority.

## Outcomes
Itch.io link: https://harry-dillamore.itch.io/alcopocolypse

GitHub link: https://github.com/Harry-Dillamore/InteractiveNarritives-Group4

## Critical Reflection

### Positives
Throughout this project I was doing many things that I have never learnt before, and I will be able to take a lot of new skills into the next project I work on. This was specifically things such as creating animation blueprints for characters based on speed and other factors, and using widgets to create the main menu and compass in the game. While they were not as successful in this project as I would have liked, I believe I will be able to develop these skills more in future projects.
Our team started off very well, with a wide variety of ideas for the game, followed by solid research completed by each member of the group. The team leader also set us a deadline for the research to be completed, which helped encourage progress to be made immediately. 

#### Negatives
Moving into the development of the game, we started to have issues where people had slightly different ideas of what exactly the game would be and what the timeline for development was. Personally, I think I could have done a better job at explaining to the team what I was working on at any given time and getting our work put together much more frequently so that it did not become a job for the final weeks - in which a number of the team were unable to be as involved as planned due to illness and various commitments. This lead to me being largely responsible for polishing the game and getting it to a point where it could be played and I did not have enough time to include all the planned features. Some of the mechanics I had put time into were also left largely unused in the final product due to me having to work on different areas of the game towards the end of the project.
For example, item interactions were planned to be a method for environmental storytelling where the player could inspect items which contained hints to the narrative of the game and deeper story elements. And while the mechanic was fully functioning, communication between the group had not been good enough so we did not have any item models which would serve this purpose.

To avoid similar issues in future group projects, I will take on more responsibility for keeping everyone updated on each other's progress and when they are planning to complete work, as well as when they will be unavailable. This would allow for more collaboration throughout the project, which would help to improve the quality of work produced. 

## Bibliography
AI Perception in Unreal Engine | Unreal Engine 5.5 Documentation | Epic Developer Community (s.d.) At: https://dev.epicgames.com/documentation/en-us/unreal-engine/ai-perception-in-unreal-engine (Accessed  29/04/2025).

Automatic Focusing Depth Of Field In Unreal Engine 5 (Tutorial) (2023) At: https://www.youtube.com/watch?v=TvXJdDSHzro (Accessed  01/05/2025).

Clicker (2025) At: https://thelastofus.fandom.com/wiki/Clicker (Accessed  29/04/2025).

Fix Missing Textures in Mesh Import UE5.4 Unreal Engine (2024) At: https://www.youtube.com/watch?v=cputwFvy4ZU (Accessed  21/05/2025).

How To Create A Main Menu System In Unreal Engine 4 | UE4 Tutorial (2022) At: https://www.youtube.com/watch?v=oIytjMKNYbU (Accessed  22/05/2025).

How To Create A Melee Combat System in Unreal Engine | Full Tutorial Course (2023) At: https://www.youtube.com/watch?v=DC7XkWXAKoE (Accessed  30/04/2025).

How To Distract An Enemy With Noise | AI Hearing - Unreal Engine 4 Tutorial (2021) At: https://www.youtube.com/watch?v=w0t75DdkazU (Accessed  29/04/2025).

How To Highlight An Object With An Outline In Unreal Engine 5 (Tutorial) (2022) At: https://www.youtube.com/watch?v=rGqlReFObYQ (Accessed  23/05/2025).

How To Punch An AI With Reaction Animations - Unreal Engine 4 Tutorial (2021) At: https://www.youtube.com/watch?v=nk85XLLnlCo (Accessed  02/05/2025).

Make an Atmospheric Environment in Unreal Engine 5 (Beginner PCG) (2024) At: https://www.youtube.com/watch?v=fBosP7fVJug (Accessed  01/05/2025).

Marvel’s Spider-Man (2018) 

Runner (2025) At: https://thelastofus.fandom.com/wiki/Runner (Accessed  29/04/2025).

Survival Game - Behavior Trees & AI Senses (Section 3) (s.d.) At: https://www.tomlooman.com/unreal-engine-cpp-survival-sample-game/section-three/ (Accessed  29/04/2025).

The Last of Us (2013) At: https://www.playstation.com/en-us/the-last-of-us/

Unreal Engine 5 Tutorial -  Compass Part 1: UI (2023) At: https://www.youtube.com/watch?v=o-pgOvQlI6I (Accessed  13/05/2025).

Unreal Engine 5 Tutorial - AI Part 3: Perception System (2022) At: https://www.youtube.com/watch?v=bx7taRBjJgM (Accessed  01/05/2025).

### Declared Assets
- Not So Scary Zombie Pack - Mixamo (s.d.) At: https://www.mixamo.com/#/?page=1&query=zombie&type=Motion%2CMotionPack (Accessed  23/05/2025).
- Locomotion Pack - Mixamo (s.d.) At: https://www.mixamo.com/#/?page=1&query=zombie&type=Motion%2CMotionPack (Accessed  23/05/2025).
- Clicking Large Stones Together 1.wav by F.M.Audio (s.d.) At: https://freesound.org/people/F.M.Audio/sounds/570526/ (Accessed  23/05/2025).
- Dirtwater - Mountain Man (2023) At: https://www.youtube.com/watch?v=ubWmmOd9Wy0 (Accessed  23/05/2025).
- Footsteps by deleted_user_5093904 (s.d.) At: https://freesound.org/people/deleted_user_5093904/sounds/268758/ (Accessed  23/05/2025).
- Hit_Hurt7.wav by n_audioman (s.d.) At: https://freesound.org/people/n_audioman/sounds/273563/ (Accessed  23/05/2025).
- Light, Retro Impact Noise by IndyTheCringeMaster (s.d.) At: https://freesound.org/people/IndyTheCringeMaster/sounds/777559/ (Accessed  23/05/2025).



