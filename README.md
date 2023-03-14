# TravellingSalesman

Implementation of the Two-Opt algorithm with the Simulated Annealing strategy to solve the travelling salesman problem.

To use it, just create a list of the X/Y locations of each point:

```
us_cities = np.array([
    [6734,1453],[2233,10],[5530,1424],[401,841],[3082,1644], [7608,4458],
    [7573,3716],[7265,1268],[6898,1885],[1112,2049],[5468,2606],[5989,2873],
    [4706,2674],[4612,2035],[6347,2683],[6107,669],[7611,5184],[7462,3590],
    [7732,4723],[5900,3561],[4483,3369],[6101,1110],[5199,2182],[1633,2809],
    [4307,2322],[675,1006],[7555,4819],[7541,3981],[3177,756],[7352,4506],
    [7545,2801],[3245,3305],[6426,3173],[4608,1198],[23,2216],[7248,3779],
    [7762,4595],[7392,2244],[3484,2829],[6271,2135],[4985,140],[1916,1569],
    [7280,4899],[7509,3239],[10,2676],[6807,2993],[5185,3258],[3023,1942]
     ])
```
Convert the list of points to a Route object:

```
cities = points_to_cities(us_cities)
route = Route(cities)
```
And call the solver:

```
route = solver(route, threshold = 10000)
route.plot_route()
route.plot_training()
```

![solved path](https://i.ibb.co/sFcYP4Q/Solved-Path.png)
![training curve](https://i.ibb.co/F3M8Rsy/Training-Time.png)
