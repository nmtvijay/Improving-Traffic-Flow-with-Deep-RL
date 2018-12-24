# Improving-Traffic-Flow-with-Deep-RL

We implement and explore Action specific Recurrent Deep Q networks(ADRQN) and compare them
with Action specific Deep Q networks(ADQN) on a toy problem of traffic flow control. The framework is also an attempt at comparing different action selection exploration strategies in this setting of ADRQNs. 



## Results
![agent playing]()

#### Final Average Speed Comparisons 
|  Network Architecture | Avg Speed (km/hr) | 
|:----------:|:------:|
|  ADQN | 95 |
|  ADRNQ with linear epsilon greedy | 98 |
|  ARDQN with Boltzmann | 88 |
|  ARDQN with variational dropout | 92 |
|  ARDQN with dropouts | 90 |


![network compare](https://github.com/nmtvijay/Improving-Traffic-Flow-with-Deep-RL/blob/master/images/adq_compare.png)
*ADQN against ADRQN wrt average speed achieved*


![policy compare](https://github.com/nmtvijay/Improving-Traffic-Flow-with-Deep-RL/blob/master/images/policy_comparision.png)
*Comparison of different exploration policies on ADRQN*



## Requirements

- Tensorflow

- pygame

- NumPy

- PIL


## Training

Each folder is an implementation with a different exploration strategy. Read their respective ReadMe files for the network architecture and the exploration strategy used.

For each implementation,

```
Set the hyperparameter DL_is_training to True and VISUALENABLED to False in Config.py

python gui.py
```

The hyperparameters can be finetuned in 'Config.py'. The current implementation trains each model for 2000 episodes.


## Testing

```
Set the hyperparameter DL_is_training to False and VISUALENABLED to True in Config.py

python gui.py
```


