# NU_MSDS460_Week7_Discussion_Simulation
#The probability an unfair die rolls a number is proportional to that number.  Pick two of these unfair, N-sided die (you choose the N ). and sum the values.  Write a simulation to estimate the mean and the variance of the sum of the dice.

#Code

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
8.669367
4.438026819311004
