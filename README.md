# LLM_Understanding_of_Culture

### Pipeline
* Get sentence data using the Master_data_maker.ipynb file (Sentence_Datasets contains the results of this file, data selected from OSCAR corpus)
* Use clustering_cosine_distances.ipynb to get word embeddings from the sentence data and cluster them using k-means clustering, as well as calculate cosine distances.
* comparison_clusters.ipynb can also be used to compare clusters of different words on the same graph.
* Mean_dist_analysis.ipynb can be used to calculate the mean cosine distances for categories of words (the data here included is for bert-base as presented in the paper)
* Use MLM_MRR.ipynb on the sentence data to get masked token predictions and calculate a MRR score and mean retrieval per word for every value of k (number of predictions)
* Use top_k_Masking.ipynb to produce vocabulary lists of the most commonly predicted guesses across all the sentence data per word. The results of this are included in Results/MLM_Results
* Use Analysing_masked_data.ipynb to look at the results of MLM_MRR.ipyb including the means per token volume and means per word type, creating graphs. 


### Notes
* The OSCAR files used to get the sentence data (therefore the input for the 'Master_data_maker.ipynb') files are not included, but can be found on HuggingFace
* It is only the pickle files for the results presented in the paper that are included here (more can be produced using clustering_cosine_distances.ipynb)
* The results folder contains the masked language modelling results pre-saved so the MLM_MRR.ipynb file does not have to be re-run before using Analysing_masked_data.ipynb. 
* Culturally_restricted_words.csv is the full list of culturally-restricted loanwords from my research.