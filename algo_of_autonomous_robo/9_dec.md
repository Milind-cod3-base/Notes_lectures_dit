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


