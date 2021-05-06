# Prediction and analysis of COVID-19 using epidemic models

This project shows an overview about the SIR and SEIR model and it compares both the model and results that SEIR models work good when Compared to SIR

# Models Used 
SIR Model (Susceptible-Infectious-Recovery)
SEIR Model (Susceptible-Exposed-Infectious-Recovery)

# Required libraries
import pandas
import numpy 
import seaborn 
import odeint

# Steps 
STEP 1- you can collect the datasets from Kaggle (covid_19_india.csv ,State wise Testing Details.csv , countries-aggregated.csv)
STEP 2- Load the datasets that you have downloaded
STEP 3- Use the SIR Equation 
            def deriv(y, t, N, beta, gamma):
            S, I, R = y
            dSdt = -beta * S * I / N
            dIdt = beta * S * I / N - gamma * I
            dRdt = gamma * I
            return dSdt, dIdt, dRdt
        And integrate this over the time grid. Similar to SEIR model
