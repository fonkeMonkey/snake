# Snake Game Spec

## Overview
A classic Snake game playable in the browser using HTML5 Canvas and vanilla JavaScript.

## Gameplay
- The player controls a snake that moves continuously in one direction
- Arrow keys (or WASD) change the snake's direction
- The snake grows by one segment each time it eats food
- Food spawns at a random empty cell after being eaten
- The game ends when the snake hits a wall or its own body

## Win/Lose Conditions
- **Game Over**: Snake collides with wall or itself
- **Score**: Increments by 10 for each food eaten
- **High Score**: Tracked in localStorage and displayed

## Visual Design
- Dark background grid
- Green snake with a slightly lighter head
- Red food item
- Score displayed at top
- Game Over overlay with final score and restart button

## Controls
- Arrow keys or WASD to change direction
- No 180-degree reversals (can't go directly backwards)
- Enter or Space to restart after game over

## Technical Details
- Canvas size: 400x400px
- Grid: 20x20 cells (20px each)
- Initial speed: 150ms per tick
- Speed increases slightly every 5 foods eaten
- Single HTML file (index.html) with embedded CSS and JS
