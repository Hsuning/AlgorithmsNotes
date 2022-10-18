#Breadth-firstSearch #BFS
- Use: #Graphs 
- Check if there is a path from A to B. 
- Shortest-path problem: “What’s the shortest path to go to X?”. Find the shortest distance between two things. Compared to fastest-path problem.
	- Write a checkers AI that calculates the fewest moves to victory
	- Write a spell checker (fewest edits from your misspelling to a real word—for example, READED -> READER is one edit)
	- Find the doctor closest to you in your network
- It’s not necessarily the fastest path. It’s the shortest path, because it has the least number of segments. #WeightedGraphs #DijkstraAlgorithm 
- Algorithms: 
	1.  Model the problem as a #Graphs .
	2. Solve the problem using breadth-first search: can we get there in 1, 2, 3, 4, ... steps
		- Is there a path from node A to node B ? (Is there a mango seller in your network?)
		- What is the shortest path from node A to node B? (Who is the closest mango seller?)
	3. Search in a queue : first-degree then second then third
- Complexitiy: O(V+E) (V for number of vertices, E for number of edges).
```
from collections import deque

# Use dictionary to create graph
graph = {}
graph['you'] = ['alice', 'bob', 'claire'] 
graph['bob'] = ['anuj', 'peggy'] 
graph['alice'] = ['peggy'] 
graph['claire'] = ['thom', 'jonny'] 
graph['anuj'] = []
graph['peggy'] = []
graph['thom'] = []
graph['jonny'] = []

# Define what you want to search?
# Ex name ends with letter m
def name_ends_with_m(name):
    if name.endswith("m"):
        return True
    return False


def break_first_search(graph, who):
    seach_queue = deque(graph[who]) #create a queue and add all the first-degree elements to search
    
    # Store name that you have already searched before to prevent duplicate search
    searched = set()
    
    # While there is at least an element in queue
    while seach_queue:
        # Dequeue the first in element
        name = seach_queue.popleft()
        if name not in searched: # if not searched before
            if name_ends_with_m(name): # Check whether the name ens with "m"
                return True, name 
            else:
                seach_queue += graph[name]
                searched.add(name)
    return False, None

break_first_search(graph, "you")
```