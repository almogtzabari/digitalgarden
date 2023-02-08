---
{"dg-publish":true,"permalink":"/notes/a-star-algorithm/","tags":[null]}
---



# A Star Algorithm
![](https://upload.wikimedia.org/wikipedia/commons/c/c2/Astarpathfinding.gif)

>[!info]
>A\* (pronounced "A-star") is a popular algorithm used in computer science for finding the shortest path between two points, such as finding the best path between two locations on a map. It combines the strengths of two other algorithms: Dijkstra's algorithm, which finds the shortest path, and a heuristic algorithm, which allows for an informed guess of the cost to reach the goal, making the search more efficient. A\* works by maintaining a priority queue of nodes to visit, where the priority of each node is based on the sum of its current cost and its estimated cost to reach the goal. This allows the algorithm to prioritize visiting nodes that are more likely to lead to the goal, making the search faster and more efficient. A\* is widely used in various applications, including video game AI, navigation systems, and robotics.

[[Notes/A-Star Algorithm\|A-Star Algorithm]] is an algorithm in the [[Notes/Graph Search Algorithms\|Graph Search Algorithms]] family which finds the shortest path[^1] between `source` and `target` nodes/points **in a large graph**.

This algorithm is good for large graphs because, unlike [[Notes/Breadth-First Search Algorithm\|Breadth-First Search Algorithm]], the next node to examine is chosen based on its distance from the `source` (lower is better, similar to [[Notes/Breadth-First Search Algorithm\|BFS]]) AND its distance to `target` (based on a heuristic function, and also, lower is better).

## Notations
- $g(node) \equiv$ Real distance between `node` and `source`.
- $h^{*}(node) \equiv$ Real distance between `node` and `target`.
- $h(node) \equiv$ Predicted distance between `node` and `target`.
- $f(node) \equiv g(node) + h(node)$ 

## Completeness
[[Notes/A-Star Algorithm\|A-Star Algorithm]] is a complete algorithm[^2] as long as one condition apply: **the heuristic function must always predict a distance that is less than or equal to real distance.** 
In [[Notes/A-Star Algorithm#Notations\|formal notation]]:
$$ \forall node\in nodes:\ h(node) \leq h^{*}(node) $$

## Intuition
- Start from `source` node and continue outwards.
- At each step examine the `node` in the queue with the lowest `f` value (see [[Notes/A-Star Algorithm#Notations\|notations]]).
- Go through `node`'s children and update their `g` value. For each child, if we achieved better `g` value and the child is already in *closed* ==> re-insert to *open* queue (and removed from *closed*).

## Implementation
```python
class Node:
	def __init__(self, data, children):
		self.data = data
		self.children = children

def astar(source, target, h_fn):
	def h(node):
		return h_fn(node, target)
		
	g = {source: 0}
	op = set(source)  # Open
	cl = set()        # Closed

	while len(op) > 0:
		cur = min(op, key=lambda node: g[node]+h(node))
		op.remove(cur)
		cl.add(cur)
		if cur == target:
			return g[cur]

		for child in cur.children:
			if child not in g or g[cur] + 1 < g[child]:
				g[child] = g[cur] + 1  # +1 is the distance/weight
				if child in cl:
					cl.remove(child)
				if child not in op:
				# If child in 'closed' -> return it to 'open'
				# If child was not seen -> insert it to 'open'
					op.add(child)

	# If we got here there's no solution
	return -1
	
```


[^1]: Shortest path means that every edge has a weight of exactly 1 (as opposed to *least-weight* where each edge can have any weight).
[^2]: If there's a solution - the algorithm will find it.