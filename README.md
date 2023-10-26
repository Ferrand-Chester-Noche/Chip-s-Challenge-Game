# Chip-s-Challenge-Game
Recreating the Chip's Challenge Game using Python

## Project Overview

This README provides a technical specification of the "Chip's Challenge Game" project, outlining its core features and requirements.

## Game Requirements

### Map
- **Grid Size:** The game map must consist of a grid with a minimum of 20 rows by 40 columns.
- **Map Loading:** Maps should be loaded from external files.
- **Map Variability:** The system must support at least three distinct maps that players can access upon completing a level.

### Tiles
Various types of tiles must be implemented with specific behaviors:
1. **Starting Tile:** This tile serves as the player's initial position when starting the game.
2. **Passable Tile:** These tiles allow unrestricted player movement and do not impact the character.
3. **Impassable Tile:** These tiles act as obstacles, restricting the character's movement.
4. **Locked Tile:** Locked tiles demand the appropriate key for access. When a player steps on such tiles, the corresponding key must be consumed, and the tile becomes permanently passable. At least two types of keys (Green and Yellow) are required.
5. **Element Tile:** Stepping onto these tiles without the corresponding immunity item in the player's inventory results in the player losing the game. When the player has the right immunity item, they can pass through the tile. The immunity item is discarded upon obtaining a different type of immunity item. At least two types of element tiles (Fire and Water) must be implemented.
6. **Thief Tile:** When a player steps on this tile, all items in their inventory are removed, and they are reset to the Starting Tile.
7. **Slide Tile:** Stepping onto a slide tile forces the player to move in the direction indicated by the tile. For example, a series of right-directed tiles pushes the player to move to the right.
8. **Exit Tile:** To progress to the next level, the player must collect all chips on the map.

### Player
The player component includes several key functionalities:
1. **Inventory Display:** The player's inventory is shown on screen and is updated in real-time whenever the player acquires keys.
2. **Chips Count:** The number of chips collected is prominently displayed on the screen.
3. **Character Movement:** The player must be able to move across the map using either the W/A/S/D keys or the directional pad (Up/Down/Left/Right).
4. **Level Requirements:** The number of chips required to complete the level is displayed on screen.
5. **Immunity Status:** The type of immunity the player currently possesses must be shown on the screen.
