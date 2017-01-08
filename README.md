# Classifying-Earthquakes

In this project I use TensorFlow and a recurrent neural network to produce a model that can classify two types of 
earthquakes. The data is taken from the 
[UCR Time Series Classification Archive](http://www.cs.ucr.edu/~eamonn/time_series_data/) 
(Yanping Chen, Eamonn Keogh, Bing Hu, Nurjahan Begum, Anthony Bagnall, Abdullah Mueen and Gustavo Batista (2015)). This
work was inspired by Rob Romijners's blog post on 
[LSTM time-series classification](http://robromijnders.github.io/LSTM_tsc/). I credit 
[Understanding LSTM Networks](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) that provided an excellent 
introduction to RNNs and how an LSTM works. I also credit the detailed blog posts 
[Recurrent Neural Networks in Tensorflow I](http://r2rt.com/recurrent-neural-networks-in-tensorflow-i.html),
[Recurrent Neural Networks in Tensorflow II](http://r2rt.com/recurrent-neural-networks-in-tensorflow-ii.html), and the
links there in for providing a good background of how to create an RNN using TensorFlow.

This project is a work in progress. If you find it interesting and would like to contribute I welcome input.

## Installation instructions

### conda
Anaconda can be downloaded from [here](https://docs.continuum.io/anaconda/install). The notebooks in this
repo use Python 3.

Create a conda environment and all required packages, less 
TensorFlow:

`conda create --name tf_python3 python=3 pandas numpy matplotlib jupyter natsort`

Enter conda environment:

`source activate tf_python3`

Install TensorFlow from [here](https://anaconda.org/jjhelmus/tensorflow):

`conda install -c jjhelmus tensorflow=0.10.0rc0`

### pip

Run the following pip command to install all required packages, 
except TensorFlow:

`pip3 install pandas numpy matplotlib jupyter natsort`

Then, install TensorFlow from [here](https://anaconda.org/jjhelmus/tensorflow):

`pip3 install -i https://pypi.anaconda.org/jjhelmus/simple tensorflow`

## Tensorboard

All TensorFlow models are saved in directories with the following format: tmp/logs/run_?? where the question marks
refer to the model run number. To start tensorboard, execute the following command:

`tensorboard --logdir=tmp/logs/run_??`

## Jupyter Slides

This project was originally presented at the San Francisco Python Meetup on November 9th, 2016. The slides associated 
with that talk are found in the Jupyter notebook `Classifying Earthquakes slides.ipynb`. A slightly different version
of that talk was presented at Udacity on January 7th, 2017 and those slides are in the Jupyter notebook 
`Classifying Earthquakes slides - Udacity.ipynb`.

If you download one of these notebooks and would like to compile the slides as html, run the following command:

`jupyter nbconvert Classifying\ Earthquakes\ slides.ipynb --to slides --post serve`
