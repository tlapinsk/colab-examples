# Colab Examples
This repository holds neural networks trained in [Google Colab notebooks](https://colab.research.google.com/notebooks/welcome.ipynb#recent=true).

This serves as a side project as I do not have a lot of exposure to Machine Learning or Deep Learning at work. I'll continue filling out the README as this repository grows over the coming months.

If you have any questions, please don't hesitate to reach out at tim.lapinskas@gmail.com. 

P.S. I am also looking for a job, so do reach out if you want to chat! I'm most interested in Product Management positions at this time. If Deep Learning is the core of your product, even better :)

## Deployment Steps
Below outlines steps for running the notebooks in Google Colab. I highly recommend trying out Google Colab before paying for GPU instances in AWS/Azure. They are free to use and in my experience very performant.

Note, that it is also possible to run these locally using Jupyter Notebook. While neither Colab nor your local laptop will see the performance of a stand alone GPU instance (cloud or local), feel free to try out whatever you see fit.

Steps below: 
1. `git clone https://github.com/tlapinsk/colab-examples.git`
2. `cd colab-examples`
3. `cd examples`
4. [Open Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb)
5. Create a new Python3 notebook
6. File > Import > Notebook of your choice
7. Run notebook

When running in a Colab notebook, be sure to back it with a GPU. You can do this via: Edit > Notebook settings > Hardware accelerator > GPU.

You can also try using a [TPU](https://cloud.google.com/tpu/). In my testing, I didn't see a performance increase using a TPU. In fact, the TPU was slower than the GPU backed notebook. I may have to do some more research, but it could possibly be due to CNN training performing better on a GPU. We'll see how a GAN performs on a TPU as well.

## Datasets
Below are links to the datasets I used. They are all public and free to use, so don't hesitate to use them for your own personal projects. Kaggle is a great place to find ML/DL data sets that are pre-labeled. As many know, lableing is time consuming. You may want to consider using AWS Mechanical Turk to outsource your labeling.

- [Animals 10 Dataset](https://www.kaggle.com/alessiocorrado99/animals10/download)
- [Kaggle Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats/data)
- [The MNIST Database](http://yann.lecun.com/exdb/mnist/) or import via Keras using `from keras.datasets import mnist`

## Notebooks
This section includes short descriptions of the notebooks and networks I have trained. It serves as a high level overview of the projects that are included in this repo.

1. [Animals 10](https://www.kaggle.com/alessiocorrado99/animals10)

There are three models trained for the Animals 10 dataset. As the name indicates, it includes 10 classes of animals. The model achieved 96% training accuracy, which is similar to the Cats vs. Dogs model.

The best performing model ([model 4](https://github.com/tlapinsk/colab-examples/blob/master/examples/animals_10_model_4_classifier.ipynb)) achieved 99% accuracy. It may be possible to achieve 99.9% accuracy if trained over more epochs. 

2. [Kaggle Docs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats)

There are 4 models trained for this project. They all include small changes to hyperparameters, overall model design, or other incremental improvements. My best model (`dog_vs_cat_classifier_3`) achieved ~96% training accuracy.

3. [MNIST GAN](https://github.com/tlapinsk/colab-examples/blob/master/examples/gans_1.ipynb)

This model trains a network to create "fake" MNIST images. Shoutout to Wouter Bulten for the [code sample](https://github.com/wouterbulten/deeplearning-resources/blob/master/notebooks/1%20-%20Getting%20started%20with%20Generative%20Adversarial%20Networks%20using%20Keras%20and%20MNIST.ipynb). None of this code is my own for now. I may refactor if needed.

4. [MNIST CNN](https://keras.io/examples/mnist_cnn/)

This was the first project I built in this repository. It is directly pulled from the Keras examples documentation and served as an easy starting point. While rudimentary in nature, it shows you how to easy build a CNN using Keras and gives you an idea of how a neural network is trained.

5. [MNIST Transfer CNN](https://keras.io/examples/mnist_transfer_cnn/)

The second project added to this repo. Again, another simple example pulled from the Keras documentation. It shows how we can train a model on the first 5 MNIST digits (0-4) and transfer over the learned model to the next 5 digits (5-9). 
