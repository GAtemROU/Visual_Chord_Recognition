# Visual Chord Recogintion
Project was done by two students Tymur Mykhalievskyi and Alexander Kuehn as part of the course High-Level Computer Vision at the University of Saarland.

## Introduction
Music recognition has been a long-standing problem.
While most solutions focus on audio, visual data can be
a valuable resource for describing music, especially in the
case of classical instruments like the guitar, piano, or harp.
Our approach centers on utilizing visual data exclusively
to address this problem.

## Goal
The main goal of the project was to recognize 14 different chords: 7 major and 7 minor.
## Methodology
This classification problem is approached using Convolutional Neural Networks with multiple stages of transfer learning.

Several pretrained models have been considered to find the best fit to the data.

The concept of transfer learning is not new, it is simply to take pretrained network and apply it on our problem. 
What was different in our case is that training on the whole data lead to 20% less accuracy comparing to making an intermidiate step in the middle. This step is to firstly train network and less diverse data and then switch to the whole problem. This led to 20% improvement on validation data.
## Results
Our final model gets 90%+ accuracy on the simple test created from the images of same person we had during training and 60% on the hard test which was created from the completely unseen data.

Check the project slides as well as the final `report.pdf` for more information.
## Real time classification
See `src/demo_webcam.ipynb` that can be run to start real time recognition using a webcamera.
