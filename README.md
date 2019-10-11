# Colab Examples
This repository will hold neural networks trained in [Google Colab notebooks](https://colab.research.google.com/notebooks/welcome.ipynb#recent=true).

It serves as a side project as I don't have much exposure to Machine Learning or Deep Learning at work. I'll continue filling out the README as this repository grows.

If you have any questions, please don't hesitate to reach out at tim.lapinskas@gmail.com. 

P.S. I am also looking for a job :) so do reach out!

## Deployment Steps
Below outlines steps for running the Jupyter Notebooks in Google Colab. Note that it is also possible to run these locally using Jupyter Notebook. While neither Colab nor your local laptop will see the performance of a stand alone GPU instance (cloud or local), feel free to try out whatever you see fit.

Steps below: 
1. `git clone https://github.com/tlapinsk/colab-examples.git`
2. `cd colab-examples`
3. `cd examples`
4. [Open Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb)
5. Create a new Python3 notebook
6. File > Import > Notebook of your choice
7. Run notebook

## Datasets
Below are links to the datasets used in this repository. They are all public and free to use - so don't hesitate to use them for your own personal projects!

- [Kaggle Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats/data)
- [The MNIST Database](http://yann.lecun.com/exdb/mnist/) or import via Keras using `from keras.datasets import mnist`

## Notebooks
This section includes short descriptions of the notebooks that I have created. It serves as a high level overview of the projects that are included in this repo.

1. [Kaggle Docs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats)

There are 4 models trained for this project. They all include small changes to hyperparameters, overall model design, or other incremental improvements. My best model (`dog_vs_cat_classifier_3`) achieved ~96% training accuracy.

2. [MNIST CNN](https://keras.io/examples/mnist_cnn/)

This was the first project I built in this repository. It is directly pulled from the Keras examples documentation and served as an easy starting point. While rudimentary in nature, it shows you how to easy build a CNN using Keras and gives you an idea of how a neural network is trained.

3. [MNIST Transfer CNN](https://keras.io/examples/mnist_transfer_cnn/)

The second project added to this repo. Again, another simple example pulled from the Keras documentation. It shows how we can train a model on 5 MNIST digits (0-4) and transfer over the learned model to the next 5 digits (5-9). 