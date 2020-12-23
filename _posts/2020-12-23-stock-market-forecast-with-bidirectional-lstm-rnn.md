---
layout: inner
position: left
title: 'Stock Market Forecast'
date: 2020-12-23 12:00:00
categories: personal-project
tags: JavaScript AngularJS API Sass
featured_image: '/img/posts/01-weekly-prediction-regulartimes.png'
project_link: 'https://github.com/ianyu93/stock-market-forecast.git'
button_icon: 'github'
button_text: 'Visit Project'
lead_text: 'Alonger-term stock market forecast with Bidrectional LSTM RNN as the first step towards my goal of building an asset allocator optimizer.'
---

## **OBJECTIVE**
The objective of this project is to design a predictive model that captures the overall
macro environment and forecasts the Standard and Poor's 500 Index with relatively good
precision and, more importantly, capturing the **rate of change in a longer timeframe**.
The model will be part of the Long-Term Asset Allocator that allocates portfolio resources
between major markets, which requires the long-term forecast of rate of change to build.
We will be creating a Weekly Predictor, Semi-Monthly Predictor, and Monthly Predictor to
explore how far in timeframe can we forecast.

## **CONTEXT** 
A large number of stock market predictive models on the web are confined within the
equity world, turning a blind eye to the interaction between major markets, namely stock,
bond, commodity, and currency. As a result, they predict only up to 5-trading days or a
binary classification of price up or down in 30 days. These models are inherently risky
and often not actionable. Our model instead would be using data from the four major
markets and forecasts up to 20 trading days, based on Intermarket Analysis methodology,
and will be replicated to different major markets to build an Asset Allocator.
Asset allocation is based on the concept of [Modern Portfolio Theory](https://www.investopedia.com/terms/m/modernportfoliotheory.asp), which seeks [Efficient
Frontier](https://www.investopedia.com/terms/e/efficientfrontier.asp). 

<div style="text-align:center">
<img src="https://www.guidedchoice.com/wp-content/uploads/2017/07/mpt-image-2.jpg" hieght=500 width=500 >

*Image source: [guidedchoice.com](https://www.guidedchoice.com/video/dr-harry-markowitz-father-of-modern-portfolio-theory/)*</div>

By forecasting long-term rate of change, one could capture Expected Return and
Expected Volatility of different major markets, which is further complicated by covariance
between the markets, one would be able to find optimal weightings to long-term
allocation of resources to different markets that minimizes risk while maximizing return.