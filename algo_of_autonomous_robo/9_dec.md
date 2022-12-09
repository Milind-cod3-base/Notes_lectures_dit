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


now robot is in room 4 (From 0). Now look at the reward matrix, there is one entry of 0 and other is 100. 

Episode 2:  

Episode 3:
now he chose to leave the house

Episode 4: 
room 2 , 

# imag3
room 3, there is something there, but he will behave explorative (greedy) now and not chose the good action


## Homework: code the Q(s,a) update 

### Crawling Robot

2 motors, 2 DOF, uses arms to move the robot, has sensors in bum
afer moving forward, back sensor will check the distance from the wall and gets the reward by increasing the sensor value.

Define 5 position for motor M1 and also for motor m2, eg (0,2) where 0 is M1 pos. and M2 pos. is 1.
this gives total of  25 states (m,n)

Actions can be M1: up, M1: down, M2: up and M2: down
this gives 4 actions

Lets encode or index all these in Q matrix
table contains action as M1+ (up), M1- (down), M2+ (up), M2- (down)

THere is no reward matrix as all of the rewards are coming from a sensor

