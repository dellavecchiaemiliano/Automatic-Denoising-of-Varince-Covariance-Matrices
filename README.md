# Automatic-Denoising-of-Varince-Covariance-Matrices
This project was developed within the Data-Driven Investment course of the MAFINRISK Master’s program at Bocconi University.
It focuses on improving portfolio construction by implementing a fully automated denoising procedure for the variance–covariance matrix of asset returns, using the Marčenko–Pastur distribution to separate informative from noisy eigenvalues.

Overview

The goal is to mitigate estimation noise in empirical covariance matrices—one of the main causes of portfolio instability in high-dimensional settings.
After fitting the theoretical Marčenko–Pastur probability density function (PDF) to the empirical eigenvalue spectrum, the algorithm identifies and replaces the noisy eigenvalues with their average value, generating a denoised covariance matrix that leads to more stable and realistic portfolio weights.

Main Components 

- Spectral decomposition of the empirical correlation matrix
- Marčenko–Pastur fitting via MSE minimization to determine λ₊ threshold
- Automatic classification of informative vs. noisy eigenvalues
- Reconstruction of a denoised, normalized correlation and covariance matrix
- Portfolio optimization (Global Minimum Variance & Maximum Sharpe Ratio) before and after denoising
- Sensitivity analysis showing the evolution of noisy eigenvalues as the portfolio dimension increases

Key Results

- The denoised covariance matrix significantly improves out-of-sample Sharpe ratios, reducing portfolio variance and instability.
- For the Max Sharpe portfolio, the denoised model achieved a Sharpe Ratio of 0.87 compared to –1.03 in the non-denoised case.
- The sensitivity analysis confirmed that as the number of assets grows, the proportion of noisy eigenvalues increases—validating the importance of spectral denoising for robust portfolio optimization
