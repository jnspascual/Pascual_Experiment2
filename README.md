**EXPERIMENT 2: NUMERICAL PYTHON (NUMPY)**

Jasmine Nicole S. Pascual

2ECE-B

September 2, 2024

**I. Intended Learning Outcomes:**
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a Numpy library

**Instructions:**
Write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter notebook in the dedicated submission bin.

**NORMALIZATION PROBLEM**

import numpy as np #Access the NumPy library

x = np.random.random((5,5)) #Generate an array with 5 rows and 5 columns containing random numbers
x #Display the random values in the x array

std = np.std(x) #Use the std function to get the standard deviation of the array
std #Display the standard deviation of the array

mean = np.mean(x) #Use the mean function to get the mean of the array
mean #display the mean of the array

data = x #Assign x to data

norm = (data-mean)/std #Use the formula for normalization by subtracting the data and mean then dividing it to the standard deviation

norm #Display the computed norm from the array

np.save('X_normalized.npy', x) #Save the result to the disk


**DIVISIBLE BY 3 PROBLEM**

import numpy as np #Access the NumPy library

x = np.arange(1,101) #Generate an array that contains 100 postive integers
x #Display the array that contains 100 positive integers

squares = x**2 #Square the values in the array
squares #Display the array with squared integers

new = squares.reshape(10,10) #Reshape the array into a 10x10 matrix
new #Display the newly shaped array

divby3 = new[new%3 == 0] #Filter the array to get the integers divisible by 3
divby3 #Display the array with positive integers divisible by 3

np.save('div_by_3.npy', divby3) #Save the result to the disk
