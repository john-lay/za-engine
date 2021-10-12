# za-engine
A GB Studio project to test features for Zelda's Adventure

Supporting a fork of `gb-studio/v2beta` https://github.com/john-lay/gb-studio/tree/feature/zeldasAdventureHud

## Features
- [x] Display a HUD consisting of a rupee counter and hearts remaining
- [ ] Enhance the game with Audio + sound effects
- [x] Zelda maintains horizonal position when navigating east and west (and vertical position for north/south)
- [ ] Unique spell animations should work on any screen
- [ ] Animate water and lamp tiles
- [x] Implement a save feature
- [ ] Implement atk/def logic for Zelda and enemies
- [x] Show all weapons/treasures over 2 inventory screens
- [x] Show collected celestial signs on inventory screen
- [ ] Show Zelda's position in an overworld minimap

## Debug Controls
As the fork of GB Studio involves modifying in game variables, a feature to modify them has been created.
GB Studio Global variables (`$00`) start some where around [0xCC40](https://github.com/chrismaltby/gb-studio/issues/540). Because the location is defined at compile time, pointers have to be updated if there's significant change to the engine. To allow visual identification in a debugger such as [BGB](https://bgb.bircd.org/) the following script edits these variables:

- `select` prints the current value of the variables
- `start` selects the next variable (see below)
- `B` decrements the selected variable
- `A` increments the selected variable
                            
The variables list is as follows (and circles back to the start):

1. Old health
2. Health
3. Old Max hearts
4. Max hearts
5. Old rupees
6. Rupees
