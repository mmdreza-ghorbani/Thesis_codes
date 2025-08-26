# Thesis: A Spatial Context-Aware Routing System Based on Air Pollution
This repository contains the code for my Master's thesis, defended at the University of Tehran. The thesis presents the design of a spatial context-aware routing system based on air pollution data. The research addresses the significant health issue of air pollution in Tehran, aiming to provide healthier travel routes for individuals with conditions like asthma, which are exacerbated by poor air quality.

The methodology involved several stages:

Air Pollution Prediction: The study first focused on modeling and forecasting PM₁₀ air pollution. The Long Short-Term Memory (LSTM) algorithm was used for time-series prediction of pollution levels.
Spatial Modeling: To create continuous pollution maps from discrete station data, two spatial interpolation methods, Inverse Distance Weighting (IDW) and Ordinary Kriging (OK), were employed and compared. The results indicated that the OK method provided better accuracy for both test data and predicted data.

Asthma Risk Mapping: A map showing the probability of asthma occurrence was created using machine learning models. This model used various inputs, including the pollution map, meteorological data, land use, distance from roads, vegetation cover, and the residential locations of individuals with and without asthma. Three classification algorithms were tested: Multilayer Perceptron (MLP), Convolutional Neural Network (CNN), and Support Vector Machine (SVM).

Context-Aware Routing: The resulting asthma probability map was used to assign weights to Tehran's road network. The Dijkstra algorithm was then implemented to find the optimal route between a specified origin and destination, comparing a standard distance-based route with a healthier route that minimizes exposure to high-risk asthma areas. The healthier route was different from the shortest path, demonstrating the system's effectiveness. The research also identified the best starting points for walking routes to the nearest parks to minimize asthma risk.

In conclusion, the thesis successfully designed and demonstrated a system that predicts air pollution, models health risk zones (specifically for asthma), and uses this information to suggest healthier travel routes. This context-aware approach offers a practical way to mitigate the health impacts of air pollution on vulnerable populations in large cities.
