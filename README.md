Generalized LGD proof

see jaya ~apd10/ for DATA links

python3 run.py --config ./train_configs/susy/train_orig.500.4.yml

python3 run.py --config ./train_configs/higgs/train_orig.500.4.yml


Papers:
1) Locality sensitive batch selection for triplet network: We have demonstrated a locality-sensitive minibatching method, LSB, which utilises locality information to inform selection of minibatches for training a triplet network. The networks trained using LSB obtained better accuracy than random minibatching methods on our evaluation task, suggesting that locality-sensitive minibatches are a better starting point for further active learning approaches. A drawback of the suggested approach is its reliance on identifying an appropriate number of projections to split the space. We plan to automate this in future. Overall, we have also shown that the method by which to obtain a minibatch for triplet mining is an important concern
 or the training of triplet networks. The value that is added by LSB is indicative of how important a batching strategy is andemphasises the need for this as a design consideration when training a triplet network. In the future we plan to extend our approach by integrating these active learning approaches and performing a comparison between locality-sensitive batching and minibatching methods.

2) ONLINE BATCH SELECTION FOR FASTER TRAINING OF NEURAL NETWORKS: While the common approach to deal with the stochasticity involved in training of deep learning
networks considers a post-processing of the gradient information incoming from batches of the
dataset, we propose to control the source of this information, the batch itself. More specifically, we
suggest to more frequently select training datapoints with the greatest contribution to the objective
function. The probability of each datapoint to be selected is decreasing with the rank of its latest
known loss value. Thus, the selection itself is invariant to rank-preserving transformation of the loss
function.
Our experiments demonstrated that online batch selection speeds up the convergence of the state-
of-the-art DNN training methods AdaDelta and Adam by a factor of about 5. We also envision that a tighter coupling of learning approaches and batch selection would allow to provide additional
speedups; for instance, one should properly link learning rates and batch size, arguably, two sides
of the same coin. The increase of the batch size over time seems to be promising to deal with the
noise involved in gradient estimation when approaching the optimum (see theoretical investigations
by Friedlander & Schmidt (2012); Babanezhad et al. (2015) and section 10.2 in the supplementary
material).
This paper provides only an initial study of possible online batch selection strategies. More ad-
vanced approaches might involve not only objective function values but also some additional indica-
tors, such as gradient amplitudes, datapoint features/classes, and similarity to other datapoints. The
selection then may consider not only the training objective function but also some proxies to the
generalization capabilities of the network.
Overall, we showed that even simple batch selection mechanisms can lead to a substantial perfor-
mance improvement. We hope that this finding will attract attention to this underexplored approach
for speeding up the training of neural networks
