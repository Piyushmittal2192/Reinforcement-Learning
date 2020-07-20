# Basics of RL
-----------------------------------------
### Explore Expolit Deliemma
#### Slot Machine Example 

Whenever we go to casino and play slotmachines, we want to win a big. But we don't know which machine gives maximum return. We either look at people who are already playing or we play ourself on different machines to evalute best machine.
i.e. we calculate a statistical value called "Win Ratio" that defines how many times we won from a machine. In order to calculate this ratio, we first have to play or observe the game for n number of times. But, the question is, what is optimal value of "n". We can't always keep on playing or observing to idenitfy the best slot machine. Therefore comes the Explore Exploit Deliemma. <br>
We need balance between number of trials we play to collect data and maximise the earnings. i.e. Maximise the winning with minimum number of attempts to collect the data. Expliot the environment via minimum exploration.

<b>Greedy Algorithm</b> : Take action for local optimal solution to reach global optimal. <br>
<b>Epsilon-Greedy</b> : Associate a small probability(epsilon) of taking something random actions (non-greedy). epsilon is usually 5% or 10%.
  - Explore if win rate is less than epsilon
  - Exploit if win rate is greater than epsilon

<b> Upper Bound Confidence </b>: Probabilty of error being bigger than a very large number is smaller and Prob of error being bigger than very small number is larger. error = sample_mean - true mean  


### MDP : a discrete time stochastic control process
- Returns : sum of future rewards
- Value : expected sum of future rewards
- Belman Equation : this allows us to solve for value function and to create agent that behaves optimally
- State Space : Set of all possible states
  - state does not need to be single obsevation at one time. we can take multiple obervations as one set and call it a state
- Action Space : Set of all possible actions
- Episode : each iteration of a game from start to terminal state of game.
- Terminal State : End of game.
- Non episodic tasks : Controlling room temperature 
- Environment - is the world in which agent lives in.
- Policy : it is function that Maps state to action ( agents brain ). it always leads to winning state.
  - Policy can be pre-defined function, an euqation or a neural network.
  - can be probabilistic or deterministic
    - deterministic : a = π(s) # π is function that takes a state as argument and returns action
    - probabilistic : π(a|s)  # π is probability distribution over action a given state s

### Markov chain: for discrete events
### Markov Process : for continous events

#### Markov Property : First order Markov Assumption
- Forget about any sequence greater than len 2
- p(st|st-1, st-2, st-3,,,,,s1) = p(st | st-1) # i.e. state at time t only depends on state at time t-1

#### State Transition Matrix
- probability of moving from state i to state j i.e. i->j 
- assumption this probabilty will remain same irreseptive of time. i.e. no matter what prob of going from state i to j will remain same always.
- p(state(t) = j | state(t-1) = i) = count(i->j)/ count(i)
- Single Transition or step of MDP Representation = {s, a, r, s'}

  
   

  
