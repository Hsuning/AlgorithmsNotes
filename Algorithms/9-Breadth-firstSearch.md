#Breadth-firstSearch #BFS
- Use: #Graphs, unweighted
- #GreedyAlgorithm 
- Check if there is a path from A to B and find the shortest path from A to B
	- Write a checkers AI that calculates the fewest moves to victory
	- Write a spell checker (fewest edits from your misspelling to a real word—for example, READED -> READER is one edit)
	- Find the doctor closest to you in your network
- It’s not necessarily the fastest path. It’s the shortest path, because it has the least number of segments. For cheapest path, see  #WeightedGraphs #DijkstraAlgorithm 
- Algorithms: 
	1.  Model the problem as a #Graphs .
	2. Solve the problem with can we get there in 1, 2, 3, 4, ... steps
	3. Search in a queue : start with first-degree nodes then second then third
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