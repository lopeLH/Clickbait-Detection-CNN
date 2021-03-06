# Clickbait-Detection-CNN

This repo provides the trained CNN model for clickbait-like headline detection presented in [1]. Essentially, a shallow CNN is trained on Word2Vec embeddings to generate a 100-dimensional representation where clickbaits and legitimate headlines are separated in terms of the Euclidean distance. This representation is used by a simple distance-based clasifier to detect clickbaits at test time. 

![model overview](https://github.com/lopeLH/Clickbait-Detection-CNN/blob/master/repo-images/model.png)

The model was trained using Chakraborty's et al. dataset [2]. To use the model you have to [download](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit?usp=sharing) Google's Word2Vec pretrained embeddings [3]. Using these pre-trained embeddings makes the model very robust against synonymy. This is, sentences using different words with similar meaning will have a similar representation in the embedding space:
<p align="center">
<img src="https://github.com/lopeLH/Clickbait-Detection-CNN/blob/master/repo-images/embed.PNG" width="550" height="365" />
</p>

As explained in the paper, since the CNN acts as a representation generator, the classification model can learn over-time by incorporating new labelled samples to the database of the distance-based classifer, and additionally by fine-tuning the CNN when enought new samples are available.

[1] [López-Sánchez, D., Herrero, J. R., Arrieta, A. G., & Corchado, J. M. (2017). Hybridizing metric learning and case-based reasoning for adaptable clickbait detection. Applied Intelligence, 1-16.
](https://link.springer.com/content/pdf/10.1007/s10489-017-1109-7.pdf)

[2] https://github.com/bhargaviparanjape/clickbait/

[3] https://code.google.com/archive/p/word2vec/
