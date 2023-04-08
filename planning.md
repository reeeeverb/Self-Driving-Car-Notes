# Planning
*Local Planning* - path planning that requires the robot to navigate in an uncertain enviornment
*Global Planning* - path planning that uses the start and end points to construct a static map 
*Bug Algorithmn* - loccal path palnning with minimum sensor and a simple algo

## Global Planning Algos
- A\* (A heuristic technique) {1} 
  - mostly used in static enviornments but with some adjustments can be made to work in dynamic
  - FORMULA : f(x) = g(x) + h(x)
      - the goal is to minimize f(x)
      - g(x) is the cost of the path from start to node n
      - h(x) is the heuristic fn that estimates the cost of the cheapest path from n to the goal 
          - most common heursitic fns include:
              - Euclidean distance
              - Manhattan distance
              - Octile distance
  - start at node n and calculate cost fn and traverse to the next node that has the lowest f(n)
    - recursively until a terminal node is reached


## Local Planning Algo
- Potential Field Methodi(Pointbug) {1}{2}
    - Uses physics fundamentals where the bot is attracted to the end point while also being repulsed by any obstacles
    - creates a vector field for artifical forces F(d) = -Uatt(vector) + Urep(vector)
            - read paper {1} for more details


