# EE4C16 - Self Driving Car Lab

## Overview

This lab is based on Udacity's [self driving car
simulator](https://github.com/udacity/self-driving-car-sim), which is
a nice testbed for training autonomous car using Convolutional Neural
Networks.

## Udacity Self Driving Car

![Simulated Self Driving Car Project Demo](/images/screenshot.jpg)


## Dependencies

1. Download and extract the ZIP of this repo (download link [here](https://github.com/frcs/EE4C16-self-driving-lab/archive/master.zip))

2. If you are on the Lab machines, start the anaconda prompt

![anaconda](/images/anaconda-start.jpg)

3. then go to the extracted directory and then type:

```bash
conda env create -f environments.yml
```

Then activate the environment. On windows you'll do:
```bash
activate 4c16
```


This will take a while, so in the meantime, go a play with the
similator (see step 4).

If you want to install this on your machine, you will need
[anaconda](https://www.continuum.io/downloads) or
[miniconda](https://conda.io/miniconda.html) to use the
environment setting. If you have a modern GPU, you can even try:

```python
conda env create -f environment-gpu.yml
```

4. Download our modified Udacity's self driving car simulator:

On the Lab machines, you will find a copy on `c:\4c16`. Otherwise you
can download a version for your system here:

*  [win64](https://drive.google.com/file/d/1vs_AbhXxPVL1fjCbRiKItR0U432ANRyh)
*  [linux64](https://drive.google.com/file/d/1ABdmMtDHMl_bRSTyDyH2zqdURkzzl93y)
*  [OSX](https://drive.google.com/open?id=1qqt_Q8pZqQFpvn9xHRMc002ABq-tQQDK)


### Collecting the training data

1. Start up the Udacity self-driving simulator, choose the **lake**
scene and press the Training Mode button.

2. Then press `R key` and select the **data** folder, where your
training images and CSV will be stored.

3. Press R again to start recording and R to stop recording. Let the
processing of video complete.

4. You should do around 1 to 5 laps of the lake track.

5. Zip both `driving_log.csv` file and `IMG` directory into a zip file
called `recordings.zip`. Upload `recordings.zip` to the 
`lab-06` directory of your cluster using the Jupyter notebook.

6. On the cluster, type these commands in the notebook to unzip the file:
```python
!rm -rf IMG
!unzip -o -qq recordings.zip
driving_log = './driving_log.csv'
```

### Train the data

check the jupyter notebook for instructions.


### Run in autonomous mode

1. The run the following command:

```python
python drive.py model-mix.h5
```


## Links

NVIDIA's paper: [End to End Learning for Self-Driving Cars](http://images.nvidia.com/content/tegra/automotive/images/2016/solutions/pdf/end-to-end-dl-using-px.pdf) for the inspiration and model structure.

[Siraj Raval](https://github.com/llsourcell) & [naokishibuya](https://github.com/naokishibuya)



