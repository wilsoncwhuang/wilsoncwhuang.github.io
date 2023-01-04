---
layout: post
title: All-to-all Shortest Path Algorithms Implementation
categories: Work-Demo
tags: C++
---

## Introduction
This is the individual final project of a graduate level course at National Cheng Kung University that I took in my junior year.
In this project, I implemented six different all-to-all shortest path algorithms with C++ to compare its complexity for different network structures.

The test networks (totally 6x3x3x3=162 networks) consist of following parameters:
<div id=parameters markdown="1">
- ***n(nodes)***: 100, 400, 800, 1600, 3200, 6400
- ***m(arcs)***: 4*n, 16*n, n*(n-1)/4
- ***seed***: 1, 10, 100
- ***(c_min,c_max)***: (1,1000), (1000,10000), (1,100000)
</div>

## Algorithms
The six all-to-all shortest path algorithms are:
1. ***Algebraic Floyd Warshall algorithm*** -FWA
2. ***Geographic Floyd Warshall algorithm*** -FWG
3. ***Bellman Ford's FIFO algorithm*** -BF
4. ***Dijkstra's algorithm (deque data structure)*** -DIKD
5. ***Dijkstra's algorithm (binary heap data structure)*** -DIKH
6. ***Dial's algorithm*** -PAPE
	
## Results
You can find the code, instructions, and output result here: <a href="https://github.com/wilsoncwhuang/All-to-all-shortest-path-algorithms-implementation">https://github.com/wilsoncwhuang/All-to-all-shortest-path-algorithms-implementation</a>

The output files show that BF and PAPE are the most efficent, while FWA and FWG are the most inefficient. Moreover, Dijkstra's algorithm perform better when data is store in binary heap.
This result corresponds to the complexity of each algorithm.


<style>
#parameters{
	margin: 5px 0px 5px;
}

p{
	text-align: justify;
}

</style>