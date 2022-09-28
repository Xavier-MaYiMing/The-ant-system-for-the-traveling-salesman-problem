### The ant system for the traveling salesman problem

##### Reference: M. Dorigo, V. Maniezzo, and A. Colorni. Ant System: Optimization by a colony of cooperating agents[J]// IEEE Transactions on Systems, Man, and Cybernetics. 1996 (26): 29-41.

##### Reference: Dorigo M, Birattari M, Stutzle T. Ant colony optimization[J]. IEEE computational intelligence magazine, 2006, 1(4): 28-39.

| Variables   | Meaning                                                      |
| ----------- | ------------------------------------------------------------ |
| alpha       | The importance of pheromone when constructing paths          |
| beta        | The importance of heuristic when constructing paths          |
| rho         | Pheromone evaporation rate                                   |
| pop         | The number of ants                                           |
| iter        | The maximum number of iterations                             |
| city_num    | The number of cities                                         |
| dis         | List, dis\[i\]\[j\] denotes the distance between city i and city j |
| pheromone   | List, pheromone\[i\]\[j\] denotes the pheromone between city i and city j |
| best_path   | The best ever solution in iterations                         |
| best_length | The length of best_path                                      |
| iter_best   | The best solution of each iteration                          |

#### Example

```python
if __name__ == '__main__':
    # Define the parameters
    alpha = 1
    beta = 5
    rho = 0.1
    pop = 20
    iter = 200
    city_num = 30
    min_coord = 0
    max_coord = 100
    coord_x = [random.uniform(min_coord, max_coord) for _ in range(city_num)]
    coord_y = [random.uniform(min_coord, max_coord) for _ in range(city_num)]
    print(main(coord_x, coord_y, pop, iter, alpha, beta, rho, 10))
```

##### Output:

![convergence curve](C:\Users\dell\Desktop\研究生\个人算法主页\The ant system for the traveling salesman problem\convergence curve.png)

![TSP result](C:\Users\dell\Desktop\研究生\个人算法主页\The ant system for the traveling salesman problem\TSP result.png)

```python
{
    'Best tour': [0, 29, 8, 23, 3, 4, 18, 26, 11, 13, 9, 19, 24, 10, 14, 15, 5, 25, 2, 27, 28, 17, 21, 20, 7, 22, 6, 16, 1, 12, 0], 
    'Shortest length': 477.4447833182615,
}
```

