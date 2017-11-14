# EE4c16 - Behavioral Cloning Lab

## Overview

This lab is based on Udacity's [self driving car
simulator](https://github.com/udacity/self-driving-car-sim), which is
a nice testbed for training autonomous car using Convolutional Neural
Networks.

## Udacity Self Driving Car

[Simulated Self Driving Car Project Demo](images/screenshot.jpg)

## Dependencies

1. You can install all dependencies by running one of the following commands

    You need a [anaconda](https://www.continuum.io/downloads) or
    [miniconda](https://conda.io/miniconda.html) to use the
    environment setting.

	[[images/anaconda-start.jpg|alt=screenshot]]


    ```python
    # Use TensorFlow without GPU (for the CADLAb machines)
    conda env create -f environments.yml

    # Use TensorFlow with GPU (on your own computer)
    conda env create -f environment-gpu.yml
    ```

	This will take a while, so in the meantime, go a play with the
	similator.

 2. Download our modified Udacity's self driving car simulator:

*  [win64](https://drive.google.com/file/d/1vs_AbhXxPVL1fjCbRiKItR0U432ANRyh)
*  [linux64](https://drive.google.com/file/d/1ABdmMtDHMl_bRSTyDyH2zqdURkzzl93y)
*  [OSX](https://drive.google.com/open?id=1qqt_Q8pZqQFpvn9xHRMc002ABq-tQQDK)


### To train the model

1. Start up the Udacity self-driving simulator, choose a scene and press the Training Mode button.

2. Then press `R key` and select the **data** folder, where our training images and CSV will be stored.

3. Press R again to start recording and R to stop recording. Let the processing of video complete.

4. You should do somewhere between 1 and 5 laps of the simulated road track.

5. The run the following command:

    ```python
    python model-mix.py
    ```

This will generate a file `model-<epoch>.h5` whenever the performance in the epoch is better than the previous best.  For example, the first epoch will generate a file called `model-000.h5`.

### Run the pretrained model

Once you have trained a model, we'll run the Autonomous Mode. 

Download the ZIP of this repo open a terminal in that folder.

In the simulator, choose a the *lake* scene and press the Autonomous
Mode button. Then, in the terminal window, run the model as follows:

```python
python drive.py model-mix.h5
```




## Vote of Thanks

NVIDIA's paper: [End to End Learning for Self-Driving Cars](http://images.nvidia.com/content/tegra/automotive/images/2016/solutions/pdf/end-to-end-dl-using-px.pdf) for the inspiration and model structure.

[Siraj Raval](https://github.com/llsourcell) & [naokishibuya](https://github.com/naokishibuya) for the knowledge and code help.



