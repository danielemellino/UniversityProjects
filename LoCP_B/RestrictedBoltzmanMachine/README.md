# Restricted_Boltzmann_Machines
In this project we use Restricted Boltzmann Machines (RBMs) in order to retrieve original data from the corrupted ones. The data are made up of sequences of 8 bits that can be arranged in different states. We have checked that the more the states the more the number of hidden units to be used, even if the analysed cases are not sufficient to find a general trend in this behaviour: for 4 states, only 2 hidden units are sufficient, while for 5 and 6 states, the minimum number of hidden units for the RBM to work properly is 4. 
The fantasy data from the RBM are generated either normally (beta = 1) or with a higher beta and we plot the score of the RBM as a function of it (q=0.1, q=0.2): in general the lower the temperature (1/beta), the higher the score, as expected, since by reducing the temperature we are actually reducing the noise. 
We then use a stronger corruption for the original data and we check worse results for this case, as expected since with more corrupted data it is more difficult for the RBM to retrieve the original ones from which they have been generated. Finally, we use different kind of data: the first ones are made up of {-1,1} bits (SPIN = True), while the seconds are the same but with 0 bits instead of -1 bits (SPIN = False): the convergence of the RBM weights is faster for the case SPIN = False (plots), while we notice slightly better results for the case SPIN = True as far as both the scores (plots) and the similarity of the results for different seeds (plots) are concerned.