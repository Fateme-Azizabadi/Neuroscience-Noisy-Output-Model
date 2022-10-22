# Neuroscience-Noisy Output Model

**Neuroscience-Noisy-Output-Model**

The basis of this model is the LIF model. In the LIF model, when the excitatory input enters, the membrane voltage increases, and when the inhibitory input enters, the membrane voltage decreases. The dynamics of this model is as follows:

 ![](https://github.com/Fateme-Azizabadi/Neuroscience-Noisy-Output-Model/blob/main/Images/Eq1.png)


Neurons return to their resting potential after spiking and have a refractory period. Considering that such cases do not exist in the dynamics of the LIF model, we must implement them manually. To reset the neuron voltage to the resting voltage, we consider a rest voltage and a peak, and every time the neuron voltage reaches the peak value, we manually reset it to the rest value. Also, in this model, the neuron spikes when the voltage reaches a threshold value. However, in the real world, this threshold is not fixed; for a neuron, each spike occurs at different voltages. It can be assumed that this threshold is determined randomly in each spike to model this phenomenon. In this example, we consider the cumulative distribution (CDF) of this phenomenon to be a logistic function:

 ![](https://github.com/Fateme-Azizabadi/Neuroscience-Noisy-Output-Model/blob/main/Images/Eq2.png)

**Note that if we keep the threshold voltage fixed, we have precisely simulated the LIF model, but by taking probabilities of the threshold, we have simulated the Noisy output model.**




 ![](https://github.com/Fateme-Azizabadi/Neuroscience-Noisy-Output-Model/blob/main/Images/Output.png)








 
 
