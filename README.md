# CI2024_lab2

## Approaches used

* Genetic Algorithm: simplest approach that doesn't give us the optimal solution
* EA with inverse mutation + partially mapped crossover: starting from a greedy solution this approach gives with at least 10 000 generations a good result

### Approach with inverse mutation + partially mapped crossover

* Inverse mutation  : selects two random indices and swaps them
* Partially mapped crossover [1]: A portion of one parent string is mapped onto a portion of the other parent string and the remaining information is exchanged. It creates an offspring in the following way: It begins by selecting uniformly at random two cut points along the strings,which represent the parents. The substrings between the cut points are called the mapping sections. Now the mapping section of the first parent is copied into the second offspring, and the mapping section of the second parent is copied into the first offspring. . Then offspring i (i = 1, 2) is filled up by copying the elements of the i th parent.In case, a number is already present in the offspring it is replaced according to the mappings.

## Results
The use of a combination of mutation and crossover resulted to be the best solution, at least in my implementation. Using only the crossover the results weren't satisfactory. On the other hand when adding also the mutation, the resutls improved a lot. For this problem one of the crossovers that interested me the most was the partially mapped crossover, which is oftend indicated as a good option for the tsp problem. Probably an edgge based crossover would have been even betterm in order to mantain the vicinity property of the cities, but I found it tricky to implement it.
In order to achieve an almost optimal result I tried with various configurations reguarding population size, offspring size and number of generations. The best results were obtained using a population and offspring size proportional to the cities used,and a maximum number of generations of 10 000.With even more generations we could have obtained an almost optimal solution, but it would be too time consuming.


## COllaborations
Ideas and suggestions were shared with fellow  [colleague](https://github.com/GioSilve).

## References

* [[1].Partially mapped crossover](https://ictactjournals.in/paper/IJSC_V6_I1_paper_4_pp_1083_1092.pdf)
