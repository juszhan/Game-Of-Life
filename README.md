# Conway's Game Of Life

The [Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life) is a famous example of how complex patterns can emerge from simple rules.


### Rules

Start with a (random) grid where each cell has two possible states: live or dead.

For each discrete time interval, update the board based on the following rules:
1. Any live cell with two or three live neighbours survives.
2. Any dead cell with three live neighbours becomes a live cell.
3. All other live cells die in the next generation. Similarly, all other dead cells stay dead.

### Implementation

In principle, the board is infinitely large as a finite board could cause undesired behaviour around the edges. Instead of regarding the cells outside of the boundary as dead, this implementation stitches the opposite edges together i.e. a [toroidal](https://en.wikipedia.org/wiki/Torus) array.

### Visualization

![80x80 grid, 180 iterations](animation.gif)