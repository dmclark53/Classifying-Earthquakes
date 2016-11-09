# Classifying-Earthquakes

In this project I use TensorFlow and a recurrent neural network to produce a model that can classify two types of 
earthquakes. The data is taken from the 
[UCR Time Series Classification Archive](http://www.cs.ucr.edu/~eamonn/time_series_data/) 
(Yanping Chen, Eamonn Keogh, Bing Hu, Nurjahan Begum, Anthony Bagnall, Abdullah Mueen and Gustavo Batista (2015)). This
work was inspired by Rob Romijners's blog post on 
[LSTM time-series classification](http://robromijnders.github.io/LSTM_tsc/).

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

To compile the Jupyter slides notebook and display the html output in your browser, run the following command:

`jupyter nbconvert Classifying\ Earthquakes\ slides.ipynb --to slides --post serve`
