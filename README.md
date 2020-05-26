# Basics of RL
-----------------------------------------
### Explore Expolit Deliemma
#### Slot Machine Example 

Whenever we go to casino and play slotmachines, we want to win a big. But we don't know which machine gives maximum return. We either look at people who are already playing or we play ourself on different machines to evalute best machine.
i.e. we calculate a statistical value called "Win Ratio" that defines how many times we won from a machine. In order to calculate this ratio, we first have to play or observe the game for n number of times. But, the question is, what is optimal value of "n". We can't always keep on playing or observing to idenitfy the best slot machine. Therefore comes the Explore Exploit Deliemma. <br>
We need balance between number of trials we play to collect data and maximise the earnings. i.e. Maximise the winning with minimum number of attempts to collect the data. Expliot the environment via minimum exploration.

<b>Greedy Algorithm</b> : Take action for local optimal solution to reach global optimal. <br>
<b>Epsilon-Greedy</b> : Associate a small probability(epsilon) of taking something random actions (non-greedy). epsilon is usually 5% or 10%. <br>
  - Explore if win rate is less than epsilon
  - Exploit if win rate is greater than epsilon
  
   

  
