# [V1.0.1] Workshop optimization
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
 
**File overwrites:**
- `ui_furniture_workshop.script`
- `ui_workshop.script`

## Known issue(s)
- None

## Planned
- None

## Changelog
v1.0.0 -> v1.0.1  
- Fixed pocket workshop crash on trying to open it.
- Added extra check for stash object to make sure it is never nil when trying to work with it.
