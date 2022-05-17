This repository contains code and paper for near optimal bidirectional A* algorithm for consistent heuristics, which I made in Februrary 2021.
The novelty is the datastructure that computes $\min_{a\in A, b\in B} \max(a_x+b_x, a_y+b_y)$ with amortized time complexity of $O(\log(|A|+|B|))$ in the following situation. 
1. initial state starts with $A=\{(0,0)\}, B=\{0,0\}$.
2. one can remove a pareto-frontiner node in $A$ and replace it with nodes with greater or equal $x,y$
3. one can remove a pareto-frontiner node in $B$ and replace it with nodes with greater or equal $x,y$

This algorithm was able to solve distance 80 positions of 15-puzzle using manhattan distance heuristic. 