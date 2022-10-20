#GreedyAlgorithm  #ApproximationAlgorithm
- At each step you pick the locally optimal solution, update if find a better solution, and in the end you’re left with the globally optimal solution.
- Sometimes, perfect is the enemy of good. Sometimes all you need is an algorithm that solves the problem pretty well. 
- This algorithms are easy to write and fast to run, so they make good #ApproximationAlgorithm 
- When calculating the exact solution 
- Algorithms:
	- Pick the item that fullfills maximum the codition (like station that covers the most states)  than haven't been covered yet.
	- It's OK to pick one that convers some states that have been covered already
	- Repeat until all the states are covered
- #DijkstraAlgorithm  is a greedy algorithms
#SetCoveringProblem
```
# A set of states we want to cover
states_needed = set(["mt", "wa", "or", "id", "nv", "ut", "ca", "az"])

# Use has for the list of stations
# key = station, value = set of states it covers
stations = {}
stations["kone"] = set(["id", "nv", "ut"])
stations["ktwo"] = set(["wa", "id", "mt"])
stations["kthree"] = set(["or", "nv", "ca"])
stations["kfour"] = set(["nv", "ut"])
stations["kfive"] = set(["ca", "az"])

# Final set of stations
final_stations = set()

while states_needed:
    best_station = None # pick the one that covers the most uncovered ststes
    covered = set() # a set of all the states the best station covers
    for station, states in stations.items(): # go through every station and pick the best one
        stat_covered = states_needed & states # set intersection
        if len(stat_covered) > len(covered): # when a new station is better than the current best station
            covered = stat_covered # replace
            best_station = station
    states_needed -= covered # update the states needed
    final_stations.add(best_station)
```
- Complexity = $O(n^2)$ compared to O(n!) for exact algorithms