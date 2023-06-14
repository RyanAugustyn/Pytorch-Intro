# Pytorch-Intro

Following along to Daniel Bourke's https://www.youtube.com/watch?v=Z_ikDlimN6A.

Machine learning (ml) is turning data into numbers and finding patterns. Where traditional programming turns inputs/rules into outputs, ML turns inputs/outputs into a set of rules.

ML is useful for complex problems where you can't think of all the rules, i.e. every variable in identifying photos of food.

ML is subset of AI, Deep Learning(DL) is subset of ML. Use ML on structured data (rows/columns-algorithm such as XGBoost useful here), DL better for unstructured data(neural network useful here)

From Google ML Handbook: "If you can build a simple rule-based system that doesn't require machine learning, do that."

DL good for: having long lists of rules, continually changing environments, insights with large amts of data

DL bad for: when you need explainability of models (too complex to understand), when the traditional approach is better, when errors are unacceptable (outputs aren't always predictable), or when you have small amounts of data (in most cases)

Common algorithms for both:
ML: random forest, gradient boosted models, Naive Bayes, nearest neighbour, support vector machine, etc
DL: neural networks I(fully connected nn, convolutional nn, recurrent nn), transformer, etc

Neural network: numerical encoding (turn inputs into numbers) called the input layer, learns representations (paterns, features, weights) called the hidden layer(s), representation outputs or the output layer, all of which can produce human readable outputs.

Each layer is usually a combination of linear and/or non-linear functions

Three types of learning: supervised, unsupervised, and transfer
