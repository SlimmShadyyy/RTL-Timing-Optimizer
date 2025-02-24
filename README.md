# AI Algorithm to Predict Combinational Logic Depth (C++)

This repository contains the C++ implementation of an AI algorithm to predict the combinational logic depth of signals in RTL modules using the MLpack library.

## Requirements
- C++ compiler (e.g., g++, clang)
- MLpack library (install using instructions below)

## Installation
1. Install MLpack:
   ```bash
   sudo apt-get install libmlpack-dev

## Clone the Repository
git clone https://github.com/SlimmShadyyy/RTL-Timing-Optimizer.git
cd rtl-depth-prediction-cpp

## Compilation
g++ -std=c++11 -o predict_depth predict_depth.cpp -lmlpack -larmadillo

## Usage
Place your RTL dataset in a CSV file (e.g., rtl_dataset.csv).
Run the compiled program:
./predict_depth
The program will output the predicted combinational depth and evaluation metrics.

## Dataset Format
The dataset should be in CSV format with the following columns:
fan_in: Fan-in of the signal.
fan_out: Fan-out of the signal.
num_gates: Number of logic gates in the path.
nested_conditions: Depth of nested conditional statements.
combinational_depth: Target variable (combinational depth).

## Model
The trained model is saved as combinational_depth_predictor.bin.

## Evaluation
Mean Absolute Error (MAE): [Value]
