# CISC489
CISC489 Group Project. Rachel, Adam, Natalie, Dom

## Abstract

The machine learning algorithms chosen for this application proved to be an inaccurate prediction of the UV index for any given day. Linear regression models oversimplified the data and predicted a constant UV index value regardless of the time of year. Because the data represented a bell curve over an entire year, a Gaussian Process Classification was used to model the data. However, similar inaccurate and oversimplified results were obtained.

## Introduction

Machine learning is a relatively new and innovative application of artificial intelligence (AI) that can use data to look for patterns and potentially provide accurate extrapolations without being explicitly coded. Long term exposure to any radiation can cause immediate and sometimes lasting effects to the skin and other organs. In the US, more people are diagnosed with skin cancer each year than all other cancers combined. This application attempts to study daily UV index data from 2006 to 2016 in order to create an accurate prediction of the UV index for any given day within that time range.

## Purpose and Research Question

A more readily available application for formulating feedback and presenting this information to the user is something that we find necessary. Can we create an application that provides an accurate estimation of the UV Index for any calendar day between 2006 and 2016?

## Subjects, Methods, and Analysis

The data used for the application were collected by the National Oceanic and Atmospheric Administration. Data sets from the years 2006-2016 containing the UV index in Dover, DE on each day were imported in order to create a machine learning algorithm predicting UV index based on day. \
Multiple machine learning algorithms were applied to the data in order to determine the most accurate function to fit the data and allow the machine to accurately detect the pattern and predict future data points, including linear regression and neural networks. \
Scikit-learn, a machine learning-based data processing library in Python, was used to apply a set of machine learning algorithms to the data. \
We first attempted importing the DEVELOP national program python package (dnppy), which offered utilities to work with Earth science and remote sensing data. 

## Results

The initial plan for the project involved using Dnppy, a NASA library, to collect current data in real-time in order to make accurate predictions based on current UV indexes. However, the software is only compatible with Python 2, while ArcGIS, the software needed to process the data, uses Python 3, so many errors were encountered when attempting to import Dnppy to ArcGIS, and the already collected NOAA data was selected for the project instead. \
A linear regression model was used on the data, but this model proved to be inaccurate for the data set because the data over time does not demonstrate linear change. Over the course of a single day, UV Index can be modeled linearly, but not for monthly or yearly, where the data resembled a bell curve and multiple bell curves, respectively. \
After the linear regression model, a neural network was also used in an attempt to model the data, but when the predictions were graphed a straight line was given once again. This was likely the same issue as the linear regression. \
Gaussian Process Classification (GPC) was also used to model the data by plotting date against UV index. GPC was expected to be a more successful model than linear regression due to the bell curve shape of the graph, but predictions for future dates were plotted as a straight horizontal line, which is not in line with the expectation given the nonlinear data used for the machine learning algorithm.

![Bell curve distribution observed from yearly UV data.](https://github.com/domgallo/CISC489/blob/master/graph1.png) \
Bell curve distribution observed from yearly UV data

## Conclusions

Linear regression models proved to be too inaccurate of a predictor of the UV index per day. This was perhaps because of the gaussian shape of the data over an entire year. \
The Gaussian Process Classification model was used to better fit the bell curve, but returned a similarly inaccurate set of predictions. \
The pattern exhibited by the data was clear, but a machine learning algorithm to properly fit the data and make reasonable predictions was not found.

## Directions for Future Research

Improvements in the overall machine learning aspect could develop a fully functioning application. Additionally, different factors besides clear sky UV index could be analyzed in order to get a more accurate prediction.\
Other regression models such as Gaussian Process Regression or Isotonic Regression may provide more accurate results than the ones tested in this project and should be attempted. \
The Gaussian Process Classification and Neural Network models should be further analyzed for possible errors hindering the accuracy of predictions as well as optimizations that can be applied to increase accuracy.
