# Exploring neural activations in fMRI data with self-organizing map
Project for Brainhack Vienna, 18-20 September 2016

Haoting Wang




A self-organizing map (SOM) is an artificial neural network using unsupervised training to visualize high-dimensional data onto a lower dimensional map. It’s map-like hidden layer includes several nodes, and each node has a weighted vector of the same size of the input space. The input data is mapped to the most similar node, called the best matching unit (BMU), according to their features.  When the training is completed, the BMUs with similar features will be close to each other.  A trained SOM is visualized by the unified distance matrix, or U-matrix, which represents the Euclidean distance between the node neighborhood on a 2-D map. 

There are a few reasons that I would like to apply SOM on neuroimaging and neuropsychological data. The input space is capable of including multiple features and the map is multi-dimensional. Neuroimaging and behavioral data can potentially be fed to the map simultaneously in map training. SOM is capable of handling large datasets, therefore it can be applied to low level raw data or group level data The result is easy to visualize and interpret. A trained map is not computationally heavy to conduct further analysis on, such as retraining the map, clustering and multi-map comparison. 

The datasets I will be using in this project are the resting state and mind wandering data collected at University of York, under the direction of Dr. Jonny Smallwood and Prof. Beth Jefferies. The first dataset includes 157 participants with both resting state fMRI and offline Multi-Dimensional Experience Sampling (MDES) reports. The second dataset is a small subset of the participants from the former set doing online MDES in the scanner. 

The two datasets are both dedicated to examine the underlying neural mechanism of mind-wandering in Default Mode Network (DMN), and I would love to continue investigating this question. In a recent BrainHack project in Paris, collaborating with Dr. Danilo Bzdok, we conducted a sparse canonical correlation analysis (SCCA) to approach this question. We successfully identified the latent components that collectively related neural activity in DMN with spontaneous thought contents. 

For this project, I am using a python based library: SOMPY. I would love to see if the previously found pattern of thoughts and connectivity patterns in DMN can be identified in the second dataset with online MDES. I will train a number of maps to learn the latent components found by SCCA and map the second dataset with online MDES onto those, to see if the latent components emerge in the online task fMRI. Furthermore, I would love to continue explore the general application of SOM on fMRI data or online training in the future. 
