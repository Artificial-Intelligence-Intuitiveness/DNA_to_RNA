Currently there are two separate autoencoders created in this project:

1) DNA-data AE can compress the given gene expression values obtained from biological microarrays twice (32 dimensions to 16). Also this model can be useful to find anomaly values and detect unusual behavior of the genes.
2) RNA-data convolutional AE works with data obtained from RNAseq experiments. Due to the complex structure of the data (and because a simple AE didn't work well in this case:) it has been transformed: every value in the 32-dimensional input vector is presented as a 20-digit binary number, i.e. every input vector is given to the network as a 20x32 pixel binary image. As result this AE is able to compress the input data twice and also may be useful for detecting anomalies.

The main goal of this project is to create an autoencoder which could predict the results of an experiment using results of an experiment based on another platfrom but using the same biological samples. This is necessary because RNAseq is getting more and more popular as a way to obtain genetic information. It's more accurate, but it's also more expensive than microarrays.
