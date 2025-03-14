# Workshop optimization
This mod tries to combat the sluggish opening of the `Portable Workshop`.

As the stash of the workshop grows in size the opening of the workshop becomes slower and slower.  
This mod combats that by not trying to load in the whole stash all at once, but rather do it [Asynchronously](https://en.wikipedia.org/wiki/Asynchrony_(computer_programming)).  
The system will load in `N` (depends on MCM config) amount of items from the stash to your inventory then it will let other scripts run for a set amount of time (depends on MCM config)  
and after this delay it will again load `N` items. Rince and repeat until the whole inventory is loaded.

This results in you having instant access to your workshop no matter how many items are in its stash.  
  
This of course comes with caveats like:  
1. Depending on your system and the MCM configs you set in `Serious workshop optimization` you will still notice hiccups while the inventory is loading. You need to fine tune your MCM settings for your specs/liking. I managed to set it basically unnoticeable (default settings), but agan. That depends on your specs.
2. I had a working `Async` closing too, but since you're able to access your inventory after you close the workshop it looked weird that items kept disappearing (going back to workshop stash) from it.
3. Items not yet loaded are not accessible in the crafting menus (if you're not speedrunning crafting you won't even notice it). If you click on another recipe then click back you will see the updated numbers.

Video showcase of the feature in action: [Showcase video](https://youtu.be/K7zadtMPDpc) (With default MCM configs)

## Installation
This mod overwrites files from `SixSloth's & Veerserif's Hideout Furnitures 2.2.1 GAMMA patch`, so make sure that the priority is set higher than that of the mentioned mod/patch.

## Configurability

**Iteration interval:** Sets the timeout between each cycle of item loading.  
**Iteration size:** Sets how many items are transfered to your inventory from the workshop at once.

**Examples:**  
Iteration interval: 0.3  
Iteration size: 70  
You have 210 items in workshop inventory.

You open the workshop. 70 items will get transfered to your inventory (become available for crafting) then the system waits for 0.3 seconds. After that another 70 items get transferred and become available.  
All items will get transferred to your inventory in 0.9 seconds.

MCM menu:

![image](https://github.com/user-attachments/assets/ba11527e-3518-49f6-b270-1d122b6c59dc)

