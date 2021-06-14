# CubeAI

This is a program that can solve a 2x2 Rubik's cube using a variety of search methods such as Breadth-First Search, Iterative Deepening Search, and A*. The heuristic I chose was the 3D Manhattan distance of the corners and then dividing that value by 4. This provided a pretty good admissible heuristic.

## Usage

`sh run.sh <search_method> <scramble_string>`

`sh run.sh bfs "F R L"`

## Dependencies

- `python 3.9+`

## Results

In all of my testing it appears that IDS explores the most nodes and A* explores the least nodes. A* exploring the least nodes is exactly what we would expect. BFS was the slowest, another expected result. Interestingly, there are cases where my A* implementation was slower than my IDS implementation. This tells me that I could have better utilized A* by applying it to IDS to create a IDA* algorithm, instead of applying A* in BFS. This would have taken the efficiency of the IDS algorithm and combined it with the selection of states of A*. The problem with A* is that it takes a lot of time to insert the state in the best position. Another way I could have made A* better was if I had come up with a better heuristic.
