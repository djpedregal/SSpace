# SSpace
SSpace is a MATLAB toolbox for time series modeling and forecasting in a rather flexible and powerful State Space framework. Marco A Villegas and I publisehd a paper on the Journal of Statistical Software ([here](https://www.jstatsoft.org/article/view/v087i05)).

Any potential user that gives it a try would soon realize that it is very easy to use. I would recommend running the demos from beginning to end, since they are conceived as a tutorial that drives the user through the modeling process step by step. People who are not directly interested in State Space modeling may also take advantage of the toolbox, because there are several templates for implementing many sort of usual time series models in a very flexible way. In other words, there is no need to know anything about State Space approaches to exploit fully the toolbox.

[Here](http://blog.uclm.es/diegopedregal/files/2019/05/SSpaceTutorial.pdf) you have also a tutorial.

## Updates:
Here are the main changes to SSpace:

1. Now input 'y' is compulsory, then there is no need to set 'y' every time you set up a model. Example:

   Before:     `m = SSmodel('y', y, 'u', u, 'model', @model);`
   
      Now:     `m = SSmodel(y, 'u', u, 'model', @model);`
2. New **SS** function runs SSmodel, SSestim, SSvalidate and SSsmooth sequentially with the same syntax than SSmodel. This saves a lot of tedious repetitive calls to these functions.
3. New model and template: **SampleSH.m** for seasonal heteroskedasticity. This is an implementation of BSM with dummy seasonality with the possibility of selecting different variances for each seasonal factor (see Proietti, T, 1998, Seasonal Heteroscedasticity and Trends, Journal of Forecasting, VOL. 17, 1-17.



