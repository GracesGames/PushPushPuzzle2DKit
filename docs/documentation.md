---
Layout: page
title: Documentation
permalink: /documentation/
---

# Documentation

***

### Game

__Main Menu Game Mode__

BP_MainMenuGameMode is the game mode and specifies the BP_MainMenuPlayerController as default controller. It is used as the game mode in the Main Menu map.

__Game Instance__

BP_PushPushPuzzle2DGameInstance is the game instance and handles the initial data (e.g. the levels for the level grid), saving and loading of the save game.

__Push Push Puzzle 2D Game Mode__

BP_PushPushPuzzle2DGameMode is the game mode and handles the current level, score, and level complete actions. It is used as the game mode in the Game map.

__Save Game__

BP_PushPushPuzzle2DSaveGame is the save game and acts as a container for the save data (e.g. time and steps per level).

### Level

__Push Push Puzzle Level__

BP_PushPushPuzzleLevel is used by the Push Push Puzzle 2D Game Mode. It builds the playable level using a TileMap object.
The chosen TileMap is analyzed and used to spawn all the actors (e.g. player start position, box, goal and coin locations).   
Users can easily add new playable rooms by creating new Tile Map objects using drag-and-drop. 

### Objects

__Box__

BP_Box is the box object that can be moved by the player.  
The box has a color and should be moved to the goal location with the matching color to complete the level. 

__Goal__

BP_Goal is the goal location object that has to be filled with a matching color box.

__Coin__

BP_Coin is the coin object that can be picked up by the player.

### Player

__Player__

BP_Player is the player of the game. It handles player input for movement in the four directions.    
It also handles updating the animations/flipbooks while moving.

### PlayerControllers

__BP_MainMenuPlayerController__

Is responsible for creating and interacting with the Main Menu.

__BP_PushPushPuzzle2DPlayerController__
 
Is responsible for creating and interacting with the HUD (HUD changes, Pause Menu and Level Complete screen).

### Widgets

All user interfaces support mobile input.   
Based on the platform the UI is automatically updated.

__HUD__

The BP_HUD is the in-game user interface and shows the player the current amount of steps, time per level and collected coins amount.  
It also defines the level complete screen with the current scores, whether the high score was beat and the option to return to the main menu.
The pause menu user interface is also integrated in the HUD and allows the player to reset the level, continue the game and return to the main menu.

__Main Menu__

BP_MainMenu is the main menu user interface and allows the player to select a level from the level select, show the controls, select their character, clear the save data and quit the game. 

__Level Select Button__

BP_LevelSelectButton is the button used in the level select grid. It defines the level to be loaded and whether the level is unlocked in the UI.