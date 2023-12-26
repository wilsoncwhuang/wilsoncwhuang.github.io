---
layout: post
title: Union Find
categories: [Data Structures and Algorithms]
tags: 
---

<script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

## 1. Introduction
The Union-Find (Disjoint Set Union, DSU) algorithm is used to efficiently keep track of a partition of a set into disjoint subsets.
It has two main operations: <br>
- **Union**: Merge two subsets.
- **Find**: Determine which particular subset the element belongs.

## 2. Operations
### 2.1 Find Operations
**Keep traveling towards the parent until we reach the top (no more parent).**
![2-1](/assets/images/Union Find/2-1.png "2-1")

- Let 1 represent the parent of left group and 3 represents the parent of right group. <br>
	_parent = [1, 1, 1, 3, 3]_ at this point.
- Call _find(x)_, x = 2:
	- _parent[2]_ = 1 and 1 != x then keep traveling x = _parent[x]_ = 1
	- _parent[1]_ = 1 and 1 == x then stop
	
### 2.2 Union Operations
**Merge y subset into x subset by assigning x's parent to y.**
![2-2](/assets/images/Union Find/2-2.png "2-2")
- Call _union(2, 3)_: 
	- Assign 3's parent as 2's parent. _parent = [1, 1, 1, 1, 3]_ at this point.

```python
class UnionFind(object):
	#Initialize with parent[i] = i
	def __init__(self, n):
		self.parent = range(n)
	
	#recursively find element's parent until its parent equal to itself (no parent)
	def find(self, x):
		return self.find(self.parent[x]) if self.parent[x] != x else x
	
	#merge y's subset into x's subset
	def union(self, x, y):
		self.parent[self.find(y)] = self.find(x)
```

## 3 Union Find Algorithms for Set Partition
Suppose we want to find the number of subsets in the following graph.
![3-1](/assets/images/Union Find/3-1.png "3-1")

$$Adj = [\begin{bmatrix}1 & 1 & 1 & 0 & 0\end{bmatrix} \\ \begin{bmatrix}1 & 1 & 1 & 0 & 0\end{bmatrix} \\ \begin{bmatrix}1 & 1 & 1 & 0 & 0\end{bmatrix} \\ \begin{bmatrix}0 & 0 & 0 & 1 & 1\end{bmatrix} \\ \begin{bmatrix}0 & 0 & 0 & 1 & 1\end{bmatrix}] $$

**1. Initialize with _parent[i] = i_.**
![3-2](/assets/images/Union Find/3-2.png "3-2")
$$parent = \begin{bmatrix}0 & 1 & 2 & 3 & 4 \end{bmatrix}$$

**2. Loop through each node to decide whether call union based on connectivity.**

- node = 0: 1 and 2 are connected, so call _union(0, 1)_ and _union(0, 2)_ 
![3-3](/assets/images/Union Find/3-3.png "3-3")
$$parent = \begin{bmatrix}0 & 0 & 2 & 3 & 4 \end{bmatrix}$$
![3-4](/assets/images/Union Find/3-4.png "3-4")
$$parent = \begin{bmatrix}0 & 0 & 0 & 3 & 4 \end{bmatrix}$$

- node = 1: 0 and 2 are connected, so call _union(1, 0)_ and _union(1, 2)_ -> graph remains the same
- node = 2: 0 and 1 are connected, so call _union(2, 0)_ and _union(2, 1)_ -> graph remains the same
- node = 3: 4 is connected, so call _union(3, 4)_
![3-4](/assets/images/Union Find/3-5.png "3-5")
$$parent = \begin{bmatrix}0 & 0 & 0 & 3 & 3 \end{bmatrix}$$
- node = 4: 3 is connected, call _union(4, 3)_ and _union(2, 1)_ -> graph remains the same

**3. Loop through parent array via find function to see which subset the node belongs to.**


```python
def FindSebsetNum(object):
	n = len(Adj)
	uf = UnionFind(n)
	for node_1, row_arr in enumerate(Adj):
		for node_2, connection in enumerate(row_arr):
			if connection == 1:
				uf.union(node_1, node_2)

	return len(set([uf.find(node) for node in uf.parent]))
```