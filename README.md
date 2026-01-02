# <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64" width="32" height="32" style="vertical-align: middle; margin-right: 8px;"><rect width="64" height="64" fill="#1a1a1a"/><defs><pattern id="grid" width="8" height="8" patternUnits="userSpaceOnUse"><path d="M 8 0 L 0 0 0 8" fill="none" stroke="#2a2a2a" stroke-width="0.5"/></pattern></defs><rect width="64" height="64" fill="url(#grid)"/><g fill="#4a9eff"><rect x="20" y="20" width="6" height="6" rx="1"/><rect x="28" y="20" width="6" height="6" rx="1"/><rect x="36" y="20" width="6" height="6" rx="1"/><rect x="36" y="28" width="6" height="6" rx="1"/><rect x="28" y="36" width="6" height="6" rx="1"/></g></svg> LIFE

An interactive, customizable implementation of Conway's Game of Life with advanced features.

## Features

- **Customizable Rules**: Create custom cellular automata rules beyond the classic Conway's Game of Life
  - Rule types: neighbor count, cycles unchanged, age, density
  - Conditional logic: fewer than, equal to, more than
  - Separate rule sets for live and dead cells
  - Save and load rule presets (up to 5)

- **Interactive Canvas**
  - Left click to paint/delete cells
  - Right click to delete cells
  - Middle mouse button (or scroll wheel) to pan
  - Scroll wheel to zoom (25% - 800%)
  - Minimap for navigation
  - Cell animations on spawn/death

- **Controls**
  - Play/Pause simulation (Spacebar)
  - Step through generations (Shift+Spacebar)
  - Adjustable speed (0.25x - 1024x)
  - Clear board
  - Save/Load board state (auto-saved to localStorage)

- **Visual Features**
  - Dark theme UI with retro aesthetic
  - Grid overlay
  - Real-time minimap showing cell distribution
  - Smooth animations and transitions
  - Tooltips for all controls

## Usage

Simply open `index.html` in a modern web browser. No build process or dependencies required.

### Keyboard Shortcuts

- `Spacebar`: Play/Pause
- `Shift+Spacebar`: Step one generation
- `Ctrl/Cmd+Spacebar`: Step one generation
- `Alt+Spacebar`: Step one generation

### Mouse Controls

- **Left Click**: Paint cells (or delete if clicking a live cell)
- **Right Click**: Delete cells
- **Middle Mouse Button**: Pan the camera
- **Scroll Wheel**: Zoom in/out

### Creating Custom Rules

1. Click the "+" button next to "Live Cells" or "Dead Cells" to add a rule
2. Select the rule type (neighbors, cycles unchanged, age, or density)
3. Choose the condition (<, =, >)
4. Set the threshold value
5. Rules are evaluated: if a rule matches, the cell changes state

### Presets

Save your custom rule sets as presets for quick access:
- Click the "+" button in the Presets section
- Enter a name for your preset
- Click "Save" on any preset to update it with current rules
- Click "Load" to apply a preset
- Click the "×" button to delete a preset

### Saving/Loading Boards

- Click "Save board" to manually save the current cell pattern
- Click "Load board" to restore the last saved pattern
- Board state auto-saves 2 seconds after the last change
- Board state persists across browser sessions via localStorage

## Technical Details

- Pure HTML/CSS/JavaScript - no dependencies
- Uses Canvas API for rendering
- localStorage for persistence
- Web Audio API for tick sounds
- Responsive design that adapts to window size

## Browser Compatibility

Works best in modern browsers that support:
- Canvas API
- ES6 features (Map, Set, arrow functions)
- localStorage
- Web Audio API

