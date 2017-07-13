# ARfit: Multivariate Autoregressive Model Fitting

This repository contains a collection of Matlab modules for 

- estimating parameters of multivariate autoregressive (AR) models,
- diagnostic checking of fitted AR models, and
- analyzing eigenmodes of fitted AR models.

The algorithms implemented in ARfit are described in the following papers, which should be referenced if you use ARfit in publications:

A. Neumaier and T. Schneider, 2001: [Estimation of parameters and eigenmodes of multivariate autoregressive models.](http://dx.doi.org/10.1145/382043.382304) ACM Trans. Math. Softw., 27, 27-57.

T. Schneider and A. Neumaier, 2001: Algorithm 808: [ARfit – A Matlab package for the estimation of parameters and eigenmodes of multivariate autoregressive models.](http://dx.doi.org/10.1145/382043.382316) ACM Trans. Math. Softw., 27, 58-65.

ARfit includes support for multiple realizations (trials) of time series and can estimate parameters of multivariate AR models taking all available realizations into account.


# Installation

The program package consists of several Matlab modules. To install the programs, download the package into a directory that is accessible by Matlab. 

Starting Matlab and invoking Matlab's online help function

```
help filename
```

calls up detailed information on the purpose and the calling syntax of the module filename.m. The script ardem.m demonstrates the basic features of the modules contained in ARfit.


# Module Descriptions

| Module                                | Description                                                                         						|
|-------------------------              | ----------------------------------------------------------------------------------- 						|
| [CHANGES](CHANGES)                    | Recent significant changes of the programs                                          						|
| [acf.m](acf.m)                  	| Plots the sample autocorrelation function of a univariate time series (using XCORR from the Matlab Signal Processing Toolbox)	|                                               | [adjph.m](adjph.m) 			| Multiplies a complex vector by a phase factor such that the real part and the imaginary part of the vector are orthogonal and the norm of the real part is greater than or equal to the norm of the imaginary part. ADJPH is required by ARMODE to normalize the eigenmodes of an AR model			|
| [arconf.m](arconf.m)			| Computes approximate confidence intervals for the AR model coefficients 							|
| [ardem.m](ardem.m)			| Demonstrates the use of modules contained in the ARfit package								|
| [arfit.m](arfit.m)			| Stepwise selection of the order of an AR model and least squares estimation of AR model parameters                        	|	
| [armode.m](armode.m)			| Eigendecomposition of AR model. For a fitted AR model, ARMODE computes eigenmodes and their associated oscillation periods and damping times, as well as approximate confidence intervals for the eigenmodes, periods, and damping times									|
| [arord.m](arord.m)			| Computes approximate order selection criteria for a sequence of AR models. ARORD is required by ARFIT				|
| [arqr.m](arqr.m) 			| QR factorization for least squares estimation of AR model parameters. ARQR is required by ARFIT				|
| [arres.m](arres.m)			| Diagnostic checking of the residuals of a fitted model. Computes the time series of residuals. The modified multivariate portmanteau statistic of Li & McLeod (1981) is used to test the residuals for uncorrelatedness											|
| [arsim.m](arsim.m)			| Simulation of AR processes													|
| [tquant.m](tquant.m)			| Quantiles of Student’s t distribution. (TQUANT is required by ARCONF and ARMODE in the construction of confidence intervals.) |