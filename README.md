# nPuzzle
A program to solve the classic nPuzzle with A* pathfinding, 4 choices of heurstics, greedy, multiplier and uniform options 

This project done in collaboration with Liam Dehaudt at 42.

* Visualizer for a 8-puzzle (3x3) solution process:
![alt text](https://github.com/conanwu777/nPuzzle/blob/master/2.jpg)

* Visualizer for a 48-puzzle (7x7) solution process:
![alt text](https://github.com/conanwu777/nPuzzle/blob/master/3.jpg)

## Features
* Command line options:

  `-v` turn on visualizer

  `-g` Greedy mode (does not give shortest solution)

  `-u` Finding solution through uniform random walk (why?!)

  `-m` Multiplier (non-admissible metric with larger weight towards greedy, works fast and well in most cases for finding non-optimal solution)

* Heurstics (all admissible):
  
  -manhattan (classic taxi-cab metric)
    
  -max (take max different of virtical and horizontal)
    
  -atomic (counts number of tiles misplaced)
    
  -linear comflict (taxi-cap plus 2*number of reversed pairs)

* Visualizer controls:

  `Key 1-4`: switches be
  tween different display images
  
  `Space`: pause/resume display
  
  `-> key`: steps through solving process
 

## Compiling and running
Run `make`. An executable will compile. Currently only tested on OS X.

Run with `./nPuzzle "Filename"`. A collection of sample puzzles files can be found in `/boards` folder.

Or use python script puzzle_generator.py:
```
python puzzle_generator.py 4 > tmp; ./nPuzzle tmp
```
n is the size of board (i.e. n=4 would produce a 4x4 board)

## Algorithm

* able to conclude solvability of the puzzle immediately

* In -m mode with linear conflict metric, a 7*7 puzzle is usually solved within 20 seconds;

Some sample time when solving randomly generated puzzles of size 3-7:
![alt text](https://github.com/conanwu777/nPuzzle/blob/master/1.jpg)
