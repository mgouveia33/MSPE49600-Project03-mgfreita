# MSPE 49600 Project 03: RBF and Neural Network Modeling
Author: Maico Freitas

Course: MSPE 49600, Data Analytics for Motorsports

Project: Project 3 — Radial Basis Function and Neural Network Modeling


This project compares Gaussian radial basis function (RBF) and quadratic models for mean Sector 3 time, with RBF hyperparameters optimization through leave one out cross validation (LOOCV).  The project also compares ReLU and tanh multilayer perceptrons (MLPs) and a quadratic reference model on simulated lap-time data.

**Datasets**
- ims_setup_project02.csv — setup inputs and Sector 3 lap-time observations for the RBF and quadratic analysis.
- simulated_laptime_data.csv — 100 simulated observations with fuel load, tire age, and lap time for the MLP analysis.

**Run the project**

The dependencies are listed in the requirements.txt 

Install the listed dependencies with:

python -m pip install -r requirements.txt

Place the two CSV datasets beside the notebook and Python export.
Run mgfreita_pr03_notebook.ipynb


**Main results**

For the IMS setup data, LOOCV selected an RBF width of approximately sigma = 0.652057 and regularization lambda = 1e-8 (the notebook display this small positive value as 0.0 when rounded). The quadratic model had the lowest LOOCV RMSE (about 0.0265 s) and test RMSE (about 0.0259 s) among the compared IMS models, so it is the recommended predictor for this split.

For the simulated lap-time data, the tanh MLP had the lowest test RMSE (about 0.2073 s), compared with about 0.5598 s for the ReLU MLP and 0.5906 s for the quadratic reference.
