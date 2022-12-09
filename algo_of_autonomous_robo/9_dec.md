# Compare monte carlo estimation and TD estimation

mc: we do full episode and then update estimated values.

error : initial vs - real return Gt

for alpha mc update: we multiply error with alpha ()

update rule for MC is: V(S) <- V(S) + a . (Gt - V(s)) [error] and alpha is step size.

# table pic is in phone and also in the lecture 5 RL colab notebook.

TD(0): 

reward: is the change between elapsed time between state to state

### add picture


(e=0.1 means, 10% of the moves will be random {greedy epsilon})


### room question, 5 rooms with robot navigation, which room leads to which and what is the reward from room to room
reward is 100 when going out of the house, when moving room to room
represent rooms into graph format


Reward matrix: from 0 to 4, one possible action is allowed and hence reward is 0. Other rewards must be -1 as it is not allowed
# add image
similiarly, from 2 we can go to room 5 (reward 100) and go to room 
# add image

Q-matrix:
tells how good is the actions related to states
initialise all 6x6 matrix with 0 (all elements)
it also represents the policy. if agent is in state 4, he can check the row and see and select the best action.

agent will have a starting state and he hass to decide where to go. 

lets update Q value of State action pair -> Q(S,A)  update

Episode 1:

we know the update rule 
# (add image)

|S(state): 0|
A(action): 4
R(reward): 0
S'(new state): 4

then update Q
new Q = 0 + 0.5 (0 + 0.9 x 0 - 0) = 0

# image


