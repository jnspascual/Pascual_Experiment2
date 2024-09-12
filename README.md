**EXPERIMENT 2: NUMERICAL PYTHON (NUMPY)**

Jasmine Nicole S. Pascual

2ECE-B

September 2, 2024
##
**I. Intended Learning Outcomes:**
1. To identify the codes and functions incorporated in the Numpy library
2. To be able to apply and use the different codes and functions in creating a Python program using a Numpy library

**Instructions:**
Write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter notebook in the dedicated submission bin.
##
**NORMALIZATION PROBLEM**

Create a random 5x5 ndarray and store it to variable X. Normalize X. Save your normalized ndarray as _X_normalized.npy_.

import numpy as np _#Access the NumPy library_

x = np.random.random((5,5)) _#Generate an array with 5 rows and 5 columns containing random numbers_
x _#Display the random values in the x array_

std = np.std(x) _#Use the std function to get the standard deviation of the array_
std _#Display the standard deviation of the array_

mean = np.mean(x) _#Use the mean function to get the mean of the array_
mean _#Display the mean of the array_

data = x #_Assign x to data_

norm = (data-mean)/std _#Use the formula for normalization by subtracting the data and mean then dividing it to the standard deviation_

norm _#Display the computed norm from the array_

np.save('X_normalized.npy', x) _#Save the result to the disk_

##
**DIVISIBLE BY 3 PROBLEM**

Create a 10x10 array from starting from 1 to 10000 which are the squares of the first 100 positive inteers. From this ndarray, determine all the elements that are divisible by 3. Save the result as _div_by_3_.

import numpy as np _#Access the NumPy library_

x = np.arange(1,101) _#Generate an array that contains 100 postive integers_
x _#Display the array that contains 100 positive integers_

squares = x**2 _#Square the values in the array_
squares _#Display the array with squared integers_

new = squares.reshape(10,10) _#Reshape the array into a 10x10 matrix_
new _#Display the newly shaped array_

divby3 = new[new%3 == 0] _#Filter the array to get the integers divisible by 3_
divby3 _#Display the array with positive integers divisible by 3_

np.save('div_by_3.npy', divby3) _#Save the result to the disk_
