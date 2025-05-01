# InteractiveNarritive-Group4
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
### AI
I began implementing 



## Bibliography