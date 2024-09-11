Welcome! This repository consists of codes in python programming language that were made to accomplish the second assesment/experiment in my course ECE2112.

The given problems for Experiment #2 are the following:

## 1.) Normalization Problem 
Normalize a 5x5 Random Matrix and Save it Normalization Problem: Normalization is one of the most basic preprocessing techniques in data analytics. This involves centering and scaling process. Centering means subtracting the data from the mean and scaling means dividing with its standard deviation. Mathematically, normalization can be expressed as: 𝑍 =(𝑋 − 𝑥̅) / 𝜎 In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and.std() calls. In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized ndarray as X_normalized.npy

The code below is based on my analysis on the given problem:
This Python script generates a 5x5 matrix of random numbers, normalizes it using the formula `(X - mean) / std`, and then saves the normalized matrix to a `.npy` file.

```python
import numpy as np                          # Import numpy to access the numpy library
X = np.random.random((5, 5))                # Create a 5x5 array with random numbers
normalizedX = (X - np.mean(X)) / np.std(X)  # Normalize the array using (X - mean) / std

np.save("X_normalized.npy", normalizedX)    # Save the normalized matrix to a file

# Print the normalized matrix
print(normalizedX)

```
## 2.) Divisible by 3 Problem :
Create the following 10 x 10 ndarray, Which are the squares of the first 100 positive integers. From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

The code below performs the following tasks:
1. Creates an array with numbers from 1 to 100.
2. Squares each number and reshapes the array into a 10x10 matrix.
3. Extracts elements that are divisible by 3 and saves them in a `.npy` file.

```python
# Import numpy to access the numpy library
import numpy as np                           

# Create an array with elements that are numbers from 1 to 100
a = np.arange(1, 101, 1)

# Square all the elements in the array and reshape it to a 10x10 matrix
b = np.square(a).reshape((10, 10))

# Print the 10x10 matrix of squared numbers
print(b)

# Extract the elements divisible by 3
c = b[b % 3 == 0]

# Save the elements divisible by 3 into a file
np.save("div_by_3.npy", c)

# Print the elements divisible by 3
print("The elements divisible by 3 are:")
print(c)
```


