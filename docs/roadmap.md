# Snake Game Roadmap

## Feature 1: Project Scaffold & Canvas Setup
- Create `index.html` with embedded CSS and JS
- Render a 400x400 canvas with dark grid background
- Define grid constants (20x20 cells, 20px each)

## Feature 2: Snake Rendering & Movement
- Initialize snake as 3-segment array at center
- Game loop using `setInterval` at 150ms
- Snake moves one cell per tick in current direction
- Render snake segments (green), head slightly lighter

## Feature 3: Input & Direction Control
- Arrow keys and WASD change direction
- Prevent 180-degree reversals
- Queue next direction to avoid input drop on fast presses

## Feature 4: Food Spawning & Collision
- Spawn red food at random empty cell
- Detect snake head collision with food → grow snake, increment score, respawn food
- Detect collision with walls and self → trigger game over

## Feature 5: Score Display & Speed Progression
- Show current score and high score at top of canvas
- Speed increases every 5 foods eaten (reduce interval by 5ms, min 60ms)
- Persist high score in localStorage

## Feature 6: Game Over Screen & Restart
- Overlay showing "Game Over", final score, and high score
- Press Enter/Space or click Restart button to reset game state
- Smooth restart without page reload

## Feature 7: Levels / Difficulty Select
- Easy / Medium / Hard options on a start screen before the game begins
- Each difficulty sets a different starting speed and speed increment
- Display current difficulty during play

## Feature 8: Animations
- Brief flash/pulse effect on the canvas when food is eaten
- Death animation: flash the snake red before showing game over overlay

## Feature 9: Sound Effects
- Eat sound: short rising beep using Web Audio API
- Death sound: descending buzz
- No external assets — all synthesized via oscillators

## Feature 10: Mobile Controls
- On-screen D-pad rendered below the canvas
- Touch events mapped to direction changes
- Responsive layout that fits small screens

## Feature 11: Walls Mode Toggle
- Toggle button to switch between "walls kill" and "wrap around" modes
- In wrap mode, snake exits one edge and enters the opposite
- Toggle persists across restarts, visible in the UI
