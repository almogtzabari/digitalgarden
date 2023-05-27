---
{"dg-publish":true,"dg-path":"Breadth-First Search Algorithm.md","permalink":"/breadth-first-search-algorithm/","tags":[null]}
---



# Breadth-First Search
![](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/BFS-Algorithm_Search_Way.gif/330px-BFS-Algorithm_Search_Way.gif)

[[Notes/Breadth-First Search Algorithm\|BFS]] is an algorithm to find the shortest path[^1] between `source` and `target` nodes/points.

## Intuition
- Start from the `source` and continue outwards.
- At each step `i`, scan all nodes that their distance from the `source` is exactly `i`. 
- Stop when reaching the `target` node.

## Implementation
```python
class Node:
	def __init__(self, data, children):
		self.data = data
		self.children = children
		
def bfs(source, target):
	if source == target:
		return 0

	visited = set()
	from collections import deque
	q = deque()
	q.append((source, 0))

	while len(q) > 0:
		cur_node, cur_dist = q.popleft()
		visited.add(cur_node)

		for child in cur_node.children:
			if child == target:
				return cur_dist + 1

			if child not in visited:
				q.append((child, cur_dist+1))

	# If we got here there's no solution
	return -1
```

[^1]: Shortest path means that every edge has a weight of exactly 1 (as opposed to *least-weight* where each edge can have any weight).