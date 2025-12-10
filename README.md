# Advent Of Code 2025

Update private input module with: `git submodule update --init --remote --recursive`

* [Day 1](Day01.ipynb). Part 1 was trivial, Part 2 can be easily solved with brute force, but doing it elegantly with modular algebra required some more thinking... (the fact that this year we'll only get 12 days of puzzles might imply the difficult level will ramp up very quickly!)

* [Day 2](Day02.ipynb). `regexp` FTW!

* [Day 3](Day03.ipynb). Quick and dirty solution for Part 1, more refined greedy sequence search for Part 2 (that can also solve Part 1).

* [Day 4](Day04.ipynb). First map of 2025 (and first visualisation)! Solved with `numpy` array operations (I could probably speed this up by using a dictionary of positions and neighbors instead of the full map, but it's fast enough if I simply ignore the empty positions).

* [Day 5](Day05.ipynb). Overlapping intervals. Part 2 is very similar to AOC 2016 Day 20, I almost entirely recycled that code to prune and merge the overlapping intervals.

* [Day 6](Day06.ipynb). Matrix rotation and flipping with `numpy`. Part 2 was fun, using string to reconstitue values after rotation, catching str->int conversion to deal with empty lines.

* [Day 7](Day07.ipynb). Another map! Used `set()` for part 1 to deal with overlapping beams, moved to `defaultdict(int)` in part 2 to count beams in same position (it's lanternfish day!). The two solutions could easily be integrated, but ehi it's Sunday morning ;-)

* [Day 8](Day08.ipynb). First really challenging day. Things learned: objects in dictionary and list are references, can be updated on the fly; result of set operations are new set, thus update of original container needed. `list.remove()` is pretty convenient (while not necessarely the most efficient approach)

* [Day 9](Day09.ipynb). Hardest day so far. Part 1 was trivial, Part 2 required to handle various edge cases and a peculiar input! Used a combination of ray casting and edge crossing detection.

* [Day 10](Day10.ipynb). BFS and bitwise XOR operation for Part 1. I initially thought I could adapt my BFS solution for Part 2, but while it works for the example, even with pruning the solution space is still too large for the full input. Thinking more carefully, I tried a mathematical approach (Part 2 is effectively a linear system with constraints), using `scipy.optimize.milp` to solve (MILP = Mixed-Integer Linear Programming). Most of the complexity was in properly encoding the constraints (integer non-negative solutions, minimal sum). Part 2 result was initially wrong by 1 becouse of a @$%^& rounding error when casting result to int! Definitely harder than yesterday, but in a different way (required more mathematical thinking and knowledge of specialized tools).