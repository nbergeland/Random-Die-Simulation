# Random Die Simulation

## Purpose and Scope
The Random Die Simulation repository provides a Monte Carlo simulation system for modeling the behavior of biased dice. Specifically, it simulates rolling two unfair N-sided dice where the probability of rolling a number is proportional to that number. The primary purpose is to estimate the mean and variance of the sum of these two biased dice rolls through statistical sampling.

## System Components
The Random Die Simulation consists of several key components working together to perform the statistical simulation:

### Figure 1: Key Components of the Random Die Simulation System

#Code

```
import numpy as np
import matplotlib.pyplot as plt
import random
N = 6
num_simulations = 1000000
die_roll = list(range(1,N+1))
def roll(N, bias_list):
    return random. choices (die_roll, weights=bias_list, k=1) [-1]
probability_list = [1/21, 2/21, 3/21, 4/21, 5/21, 6/21]
sum_of_dice = []
for i in range (num_simulations):
    sum_of_dice.append (roll(N, probability_list) + roll(N, probability_list))
mean = np.mean (sum_of_dice)
variance = np.var(sum_of_dice)
plt.hist (sum_of_dice, color = 'purple', alpha = 0.7)
plt.show()
![image](https://user-images.githubusercontent.com/55772476/168692449-07935b43-addf-49b8-88c5-292d161f6e93.png)
print(mean)
print(variance)
```
8.669367
4.438026819311004
