# [V1.0.4] Workshop optimization
This mod stops the `Portable Workshop` from moving its stash to player inventory.  
This way the lag upon opening/closing the workbench of the portable workshop is completely eliminated.

## Installation
This mod overwrites some the following mod's files/patches (make sure that the priority is set higher than that of the mentioned mods/patches).  
It's fine to just install with highest priority.

**Mod overwrites:**
- `SixSloth's & Veerserif's Hideout Furnitures 2.2.1 GAMMA patch`
  - File overwritten: `zzz_workshop_return_items.script`
- `286- High-level Toolkits Include Low-level Toolkits - ilrathcxv`
  - File overwritten: `z_monkey_toolkit_workshop.script`
- `141- Fixed Crafting with Multi-Use Items - thisisntmysteamid`
  - File overwritten: `zzz_timsi_ui_workshop`
- Either `Momopate's Barrel Condition Effects Display` or `SERIOUS Weapon Maintain Features 'n fixes` if you have mine installed.
  - Overwrites the monkey patch found in `zzzz_arti_jamming_repairs.script`. NOTE: DOES NOT OVERWRITE FILE. ONLY THE MONKEY PATCH FOUND IN SAID FILE
- `337- QoL Bundle - Utjan`
  - File overwritten: `craft_use_low_cond.script` 
 
**File overwrites:**
- `ui_furniture_workshop.script`
- `ui_workshop.script`

**Monkey patch**
- `z_serious_monkey_ui_debug_launcher.script`: Patches the workshop opening script to include artefact melter too.
- `zzzzz_ui_workshop_repair_patch.script`: Patches weapon part replacement logic.

## Known issue(s)
- Some stacked items: Ammo crafting for example.
   
Let's say I need 3 powder 3 bullet and 3 casing.  
I have 1 of each in player inventory and 2 of each in workshop stash.  
The crafting window will show 3/3 for all items yet all of them will be red as if you don't have enough of them and crafting is not allowed.  
This for now only seems to be affecting ammo crafting. For example in artefact crafting it's fine if you have 1 boar leg in stash and 1 in inventory it will correctly recognize everything.

## Planned
- None

## Changelog
v1.0.0 -> v1.0.1  
- Fixed pocket workshop crash on trying to open it.
- Added extra check for stash object to make sure it is never nil when trying to work with it.

v1.0.1 -> v1.0.2  
- Fixed crash when opening toolkit outside of workshop.
- Arfetact melter is now included in pocket workshop.

v1.0.2 -> v1.0.3  
- Properly severs the connection between the stash and workshop when closing workshop. (In V1.0.2 if you opened the workshop from portable workshop then you would have access to the stash of the last workshop you opened. Even when workshop was opened from inventory.)
- Weapon parts replacement: The gun's replaced parts will be placed in the inventory where the replacement parts came from. (If you have a barrel in stash and replace gun's barrel the old one will go to stash. If you had it in inventory it will go to inventory.)

v1.0.3 -> v1.0.4
- Fixes craft bugs regarding items with condition. (First I thought this had something to do with artefacts, so this is basically a fix for the "Artefact crafting" bug too.)
