# Advent Of Code 2025

Update private input module with: `git submodule update --init --remote --recursive`

* [Day 1](Day01.ipynb). Part 1 was trivial, Part 2 can be easily solved with brute force, but doing it elegantly with modular algebra required some more thinking... (the fact that this year we'll only get 12 days of puzzles might imply the difficult level will ramp up very quickly!)

* [Day 2](Day02.ipynb). `regexp` FTW!

* [Day 3](Day03.ipynb). Quick and dirty solution for Part 1, more refined greedy sequence search for Part 2 (that can also solve Part 1).

* [Day 4](Day04.ipynb). First map of 2025 (and first visualisation)! Solved with `numpy` array operations (I could probably speed this up by using a dictionary of positions and neighbors instead of the full map, but it's fast enough if I simply ignore the empty positions).