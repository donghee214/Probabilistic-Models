# Probabilistic-Models
Approximate &amp; Exact Inferencing Using Bayes Nets

Given an noisy input of the distance to a target(ghost) extract likely positions:

Exact Inference:
- OBSERVATION: The agent will update its beliefs depending on the noisy reading per action
- TIME: The agent deducts unreasonable outliers by knowing the legal actions of the ghost(1 movement and wall placements)
- The agent will finally choose the greedy action (closest Manhattan distance to the target)

Approximate Inference:
- Similar deduction except using particle filtering
- Each particle(sample) represents a ghost
- The particles are just a position representation of the process given a distribution and lots and LOTS of sampling. 
- OBSERVATION + TIME: Each particle is evenly distributed and as the beliefs update in the same manner as the exact inferencing, the         particles are distributed accordingly 

Joint Distribution:
- Now some ghosts will act relative to the position of other ghost, some try to isolate themselves from other ghosts
- All ghost are no longer independent, they are only conditionally independent
- Using a dynamic Bayes Net improve the distribution of particles to better accurately process the noisy input
