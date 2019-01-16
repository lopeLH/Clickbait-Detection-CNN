# Clickbait-Detection-CNN

This repo provides the trained CNN model for clickbait-like headline detection presented in [1]. Essentially, a shallow CNN is trained on Word2Vec embeddings to generate a 100-dimensional representation where clickbaits and legitimate headlines are separated in terms of the Euclidean distance. This representation is used by a simple distance-based clasifier to detect clickbaits at test time. 


As explained in the paper, since the CNN acts as a representation generator, the classification model can learn over-time by incorporating new labelled samples to the database of the distance-based classifer, and additionally by fine-tuning the CNN when enought new sambles are available.

[1] [López-Sánchez, D., Herrero, J. R., Arrieta, A. G., & Corchado, J. M. (2017). Hybridizing metric learning and case-based reasoning for adaptable clickbait detection. Applied Intelligence, 1-16.
](https://link.springer.com/content/pdf/10.1007/s10489-017-1109-7.pdf)
