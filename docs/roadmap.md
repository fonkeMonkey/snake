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

## Feature 12: Pause
- Press P or Escape to pause/resume mid-game
- Dim overlay with "PAUSED" text shown while paused

## Feature 13: Power-ups
- Three types: slow time (blue), bonus points (gold), shield (purple)
- Appear randomly for a limited duration, then despawn
- Shield lets snake survive one wall/self collision

## Feature 14: Obstacles
- Static wall segments spawned on the grid as difficulty increases
- More obstacles appear at higher food counts
- Collision with obstacles triggers game over (unless shielded)

## Feature 15: Particle Burst
- Small colored particles explode outward from food on eat
- Particles fade and shrink over ~400ms using requestAnimationFrame

## Feature 16: Countdown Start
- 3-2-1-GO! countdown on the canvas before snake starts moving
- Snake is visible but frozen during countdown

## Feature 17: Theme Selector
- Four color themes: Neon (default), Retro Green, Fire, Ice
- Theme toggle button cycles through options, updates all colors live
- Persists in localStorage

## Feature 18: Local Leaderboard
- Top 5 scores with initials stored in localStorage
- Prompt for initials on game over if score qualifies
- Leaderboard shown on game over screen

## Feature 19: Milestones
- Brief animated message on screen at 50, 100, 200+ point thresholds
- Messages: "Nice!", "On fire!", "Unstoppable!", etc.
- Fades out after 1.5s without interrupting gameplay

## Feature 20: Two-Player Mode
- Two snakes: Player 1 (WASD, green) and Player 2 (arrows, blue)
- Both on same canvas, last alive wins
- Round winner shown on game over overlay

## Feature 21: Speed Burst
- Hold Shift to temporarily boost snake speed (2x)
- Stamina bar shown below canvas; depletes while boosting, recharges when released
- Boost unavailable when stamina is empty

## Feature 22: Ghost Snake
- After each game, save the full move history in localStorage
- On next game, render a semi-transparent ghost replay of the best run
- Ghost doesn't interact with the live snake — purely visual

## Feature 23: Shrink Power-up
- New pink power-up that removes the last 3 segments from the snake
- Useful as an escape when near self-collision
- Briefly animates the segments shrinking away

## Feature 24: Maze Mode
- Toggle-able mode that procedurally generates a maze of wall segments at game start
- Maze is regenerated each new game
- Works with existing walls/wrap toggle

## Feature 25: Combo Multiplier
- Eating food within 3 seconds of the last eat increments a combo counter (x2, x3…)
- Score multiplied by combo value; combo resets after 3s of not eating
- Combo counter displayed prominently, pulses on increment

## Feature 26: Achievements
- 8 in-game achievements (e.g. "First Blood", "Speed Demon", "Untouchable", "Big Eater")
- Unlocked achievements stored in localStorage
- Toast notification appears on unlock; view all on a new Achievements panel

## Feature 27: Screenshake & Juice
- Screen shakes briefly on death
- Snake head squashes/stretches in direction of travel
- Food wobbles in place with a subtle idle animation
