# House Price Prediction Using a Neural Network (PyTorch)


This project aims to predict house prices using multiple features such as area, bedrooms, bathrooms, parking spaces, and more. A simple feed-forward neural network (implemented in PyTorch) is used to predict house prices based on both numerical and categorical data. Data preprocessing includes scaling, normalization, and handling outliers.


1)Dataset

The dataset contains several features about houses, including:

#Numerical Features:

-Area
-Number of bedrooms
-Number of bathrooms
-Number of stories
-Parking spaces

#Categorical Features:

-Main road access
-Guest room availability
-Basement availability
-Hot water heating availability
-Air conditioning availability
-Preferred area
-Furnishing status
-The target variable is the house price.

2)Install need libraries

--> pip install pandas numpy scikit-learn seaborn pytorch matplotlib


3)Project Structure

*Data Preprocessing*:
_____________________

-Outlier Detection: Applied Inter-Quartile Range (IQR) method to detect and remove outliers in house prices.
-Normalization: Scaled the price feature using MinMaxScaler to ensure it falls between 0 and 1.
-One-Hot Encoding: Categorical features are one-hot encoded for compatibility with the neural network.
-Scaling: Numerical features are scaled using StandardScaler.

*Model Architecture*:
_____________________

A simple neural network with the following characteristics:

-Input Layer: Matches the number of features (after one-hot encoding).
-Output Layer: One neuron to predict the house price.

*Training*:
___________

The model is trained using the Mean Squared Error (MSE) loss function and optimized using the Adam optimizer. The training process runs for 1000 epochs, during which:

-Training and validation losses are tracked.
-R² score is calculated after each epoch to measure performance (R² = 0.77).

*Evaluation*:
_____________

After training, the model is evaluated on the validation set. The following plots are provided:

-Training vs. Validation Loss: Visualizes the model's performance over time.
-Actual vs. Predicted Prices: A scatter plot comparing actual and predicted prices.
-Actual and Predicted Prices: Displays the actual and predicted prices for each data point in the validation set.


