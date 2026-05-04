# NFL Fantasy Performance Predictor

## Overview
This project develops a neural network to predict NFL players’ fantasy points for upcoming seasons using historical statistics. Fantasy football requires accurate projections for informed draft and lineup decisions, and traditional methods often fail to capture complex interactions between player stats and team context.

---

## How It Works
The model is a fully connected feed-forward neural network implemented in TensorFlow/Keras. Input features include passing, rushing, and receiving stats, player age, usage trends, injury history, and position (one-hot encoded). The network uses two hidden layers with ReLU activation and dropout for regularization, and outputs a single numeric value representing projected fantasy points. The model is trained using backpropagation with the Adam optimizer and evaluated using Mean Absolute Error (MAE) and R-squared metrics. Read this [report](Report.pdf) for an in-depth analysis on the model.  

### 1. Feed-Forward Network
The model is a **Feed-Forward Neural Network**. This simply means information flows in one strict direction:
* **Input:** It takes in raw player stats (like past performance or matchups).
* **Processing:** It passes that data through "hidden layers" where the heavy lifting happens.
* **Output:** It delivers the final prediction.

### 2. How a Digital "Neuron" Works
The model is made of tiny processing units called **neurons**, inspired by the human brain.
* **Weights:** The model assigns "importance" to different stats. For example, recent form might be weighted more heavily than stats from three years ago.
* **Activation:** Just like a real brain cell "fires" when it gets enough stimulation, these digital neurons only pass information forward if the data is significant enough.

### 3. Learning from Mistakes
The model doesn't start out smart; it learns through trial and error:
* **The Error:** After making a prediction, the model compares its guess to the **actual** fantasy points scored.
* **The Adjustment:** It looks back at its work to see which weights were responsible for the error.
* **The Optimization:** It tweaks those weights to make the prediction more accurate the next time.

---

 By stacking many layers of these neurons, the model can move beyond simple averages to spot complex, hidden patterns that a human might miss.

## Data
The dataset includes NFL player statistics from 1990 to 2024, sourced from Kaggle and Pro Football Reference. Data preprocessing includes cleaning, removing incomplete records, standardizing features, and encoding categorical variables to ensure compatibility with the neural network.

## Why This Project
Fantasy performance depends on nonlinear and interacting factors that simple linear models cannot capture. By leveraging neural networks, this project produces accurate, generalizable projections to assist fans in making better strategic decisions during fantasy drafts, enhancing engagement and competitiveness.
