# NFL Fantasy Performance Predictor

## Overview
This project develops a neural network to predict NFL players’ fantasy points for upcoming seasons using historical statistics. Fantasy football requires accurate projections for informed draft and lineup decisions, and traditional methods often fail to capture complex interactions between player stats and team context.

## How It Works
The model is a fully connected feed-forward neural network implemented in TensorFlow/Keras. Input features include passing, rushing, and receiving stats, player age, usage trends, injury history, and position (one-hot encoded). The network uses two hidden layers with ReLU activation and dropout for regularization, and outputs a single numeric value representing projected fantasy points. The model is trained using backpropagation with the Adam optimizer and evaluated using Mean Absolute Error (MAE) and R-squared metrics. Read this [report](Report.pdf) for an in-depth analysis on the model.

## Data
The dataset includes NFL player statistics from 1990 to 2024, sourced from Kaggle and Pro Football Reference. Data preprocessing includes cleaning, removing incomplete records, standardizing features, and encoding categorical variables to ensure compatibility with the neural network.

## Why This Project
Fantasy performance depends on nonlinear and interacting factors that simple linear models cannot capture. By leveraging neural networks, this project produces accurate, generalizable projections to assist fans in making better strategic decisions during fantasy drafts, enhancing engagement and competitiveness.
