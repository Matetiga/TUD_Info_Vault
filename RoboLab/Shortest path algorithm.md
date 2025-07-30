### <span style="color:#00ff04">algorithm:: Disjktra Algorithm</span>

# capaz haya en github?

```python
def disjktra(graph, start):

# Create a list of unvisited nodes

unvisited = list(graph)

# Create a list of visited nodes

visited = []

# Create a list of distances

distances = {}

# Create a list of predecessors

predecessors = {}

# Set the distance for the start node to 0

distances[start] = 0

# Set the distance for all other nodes to infinity

for node in unvisited:

if node != start:

distances[node] = float('inf')

# While the unvisited list is not empty

while unvisited:

# Find the node with the smallest distance

smallest = None

for node in unvisited:

if smallest is None:

smallest = node

elif distances[node] < distances[smallest]:

smallest = node

# For each neighbor of the node

for neighbor in graph[smallest]:

# Calculate the distance to the node

distance = distances[smallest] + graph[smallest][neighbor]

# If the distance is smaller than the current distance

if distance < distances[neighbor]:

# Set the distance to the new distance

distances[neighbor] = distance

# Set the predecessor to the current node

predecessors[neighbor] = smallest

# Move the node to the visited list

unvisited.remove(smallest)

visited.append(smallest)

# Return the list of distances and predecessors

return distances, predecessors
```

```python
def disjktra():

graph = {

'A': {'B': 1, 'C': 4},

'B': {'A': 1, 'C': 2, 'D': 5},

'C': {'A': 4, 'B': 2, 'D': 1},

'D': {'B': 5, 'C': 1}

}

  

start = 'A'

shortest_path = {}

predecessor = {}

  

unseen_nodes = graph

infinity = float('inf')

path = []

  

for node in unseen_nodes:

shortest_path[node] = infinity

shortest_path[start] = 0

  

while unseen_nodes:

min_node = None

for node in unseen_nodes:

if min_node is None:

min_node = node

elif shortest_path[node] < shortest_path[min_node]:

min_node = node

  

for child_node, weight in graph[min_node].items():

if weight + shortest_path[min_node] < shortest_path[child_node]:

shortest_path[child_node] = weight + shortest_path[min_node]

predecessor[child_node] = min_node

unseen_nodes.pop(min_node)

  

current_node = 'D'

while current_node != start:

try:

path.insert(0, current_node)

current_node = predecessor[current_node]

except KeyError:

print('Path is not reachable')

break

path.insert(0, start)

if shortest_path['D'] != infinity:

print('Shortest path is ' + str(shortest_path['D']))

print('And the path is ' + str(path))
```


```python
# get_paths possibility 
# to pack everything in a dictionary
# can this single line be enough

# setdefault(coordinates, {}) returns the value of the key if it exists

# if not, it creates a new key with the value of the second argument "{}"

# .update({direction: valuess}) updates the value of the key "coordinates"

# with a key-value pair

#reached_nodes.setdefault(coordinates, {}).update({direction: values})
```