# nPuzzle
A program to solve the classic nPuzzle with A* pathfinding, 4 choices of heurstics, greedy, multiplier and uniform options 

This project done in collaboration with Liam Dehaudt at 42.

## Features
* Command line options
  `-v` turn on visualizer
  `-g` Greedy mode (does not give shortest solution)
  `-u` Finding solution through uniform random walk (why?!)
  `-m` Multiplier (non-admissible metric with larger weight towards greedy, works fast and well in most cases for finding non-optimal solution)
  * Heurstics (all admissible):
    -manhattan (classic taxi-cab metric)
    -max (take max different of virtical and horizontal)
    -atomic (counts number of tiles misplaced)
    -linear comflict (taxi-cap plus 2*number of reversed pairs)

## Compiling and running
Run `make`. An executable will compile. Currently only tested on OS X.

Run with `./nPuzzle "Filename"`. A collection of sample puzzles files can be found in `/boards` folder.
Or use python script puzzle_generator.py:


![alt text](https://github.com/conanwu777/nPuzzle/blob/master/1.png)
