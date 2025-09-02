<img width="10" height="15" alt="image" src="https://github.com/user-attachments/assets/7c89457e-6618-4bac-b7c9-4cc2c5d6104f" /># INTRODUCTION TO PYTHON PROGRAMMING
## NORMALIZATION PROBLEM:
Normalization is one of the most basic preprocessing techniques in data analytics. This involves centering and scaling process. Centering means subtracting the data from the mean and scaling means dividing with its standard deviation. Mathematically, normalization can be expressed as:

𝑍 = 𝑋 − 𝑥̅ / 𝜎

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and .std() calls.

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized ndarray as X_normalized.npy

#### MY CODE:
<img width="1281" height="820" alt="image" src="https://github.com/user-attachments/assets/50b38fd9-3829-4979-9c18-c376d886954d" />


#### EXPLANATION:
Step 1:
Import NumPy as np since it is one of the most common Python packages that provides efficient tools for creating arrays and performing mathematical operations.
<img width="1277" height="66" alt="image" src="https://github.com/user-attachments/assets/b1f87f2c-73ab-4be9-bb1e-2ceba1a2fcd4" />


Step 2:
Create a 5x5 array with random values using np.random.rand (5, 5) and assigned it to variable X. This was the most significant part, as it has sample data for applying a normalization process. 
It also printed that array so I could observe the original unprocessed values before normalization.
<img width="1279" height="56" alt="image" src="https://github.com/user-attachments/assets/739f519d-52da-4bb5-9f4e-0b1892139aa4" />


Step 3:
Print the array so we can observe the original unprocessed values before normalization.
<img width="1275" height="188" alt="image" src="https://github.com/user-attachments/assets/bc8dc308-0a78-4c22-b1de-480d167a2f8b" />

Step 4:
Use X.mean() and X.std() to get the array's mean and standard deviation. X.mean() calculates the mean (average) of all the values in the array X and tells us the center of the data — the balance point. 
<img width="1277" height="77" alt="image" src="https://github.com/user-attachments/assets/7645dcbe-7c66-45bc-a6eb-8737898194d8" />

X.std() calculates the standard deviation of the values in X in which measures how spread out the numbers are from the mean. 

This is important because normalization is centering the data by subtracting the mean and scaling it by dividing by the standard deviation. 


Step 5:
Print the mean and standard deviation to have a clearer view of how distributed the numbers are in the array.
<img width="1280" height="185" alt="image" src="https://github.com/user-attachments/assets/839bcc26-3707-46d2-aabc-5cdd1c51715b" />

Step 6:
Normalization for the array according to the relation X_normalized = (X - mean) / std. The part conveys that normalization must be applied within the course of domain knowledge, where every element in the array gets its transformation, so that the data is centered around zero and scaled according to its spread.

The code: X_normalized = (X - mean) / std -- normalizes the array X using the z-score normalization formula, where (X - mean) subtracts the average from every element in X, and / std  divides each shifted value by the standard deviation.
<img width="1280" height="66" alt="image" src="https://github.com/user-attachments/assets/9892f614-3ec5-42b7-88cf-16ffcd7b934e" />

Step 7:
Print the normalized array to see changes
<img width="1276" height="181" alt="image" src="https://github.com/user-attachments/assets/1dd35e49-f38b-4e0d-a97b-7723d6f50b9c" />

Step 8:
<img width="1280" height="67" alt="image" src="https://github.com/user-attachments/assets/2dfe566b-7d86-49be-85a6-923586e72f4b" />
Afterwards, save the normalized array to a file using np.save("X_normalized.npy", X_normalized). This will allow one to save and reuse processed data without having to repeat the normalization process again.

## DIVISIBLE BY 3 PROBLEM:
Create the following 10 x 10 ndarray

<img width="459" height="152" alt="image" src="https://github.com/user-attachments/assets/01ff4531-7933-4850-8dd7-09033808d2f6" />

which are the squares of the first 100 positive integers.

From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

#### MY CODE:
<img width="1279" height="616" alt="image" src="https://github.com/user-attachments/assets/cc9073b9-0403-46a7-82e5-1e46e5b5c997" />

#### EXPLANATION:

Step 1:
Import numpy as np to manipulate arrays and apply mathematical operations efficiently. 
<img width="1279" height="66" alt="image" src="https://github.com/user-attachments/assets/442b1f46-64cc-404d-b6fc-c043de2ca89d" />

Step 2:
Create an array of the first 100 positive integers with np.arange(1, 101) and squared them with ** 2. I reshaped the outcome into a 10x10 ndarray using .reshape(10, 10) and then assigned it to the variable named A.
<img width="1281" height="77" alt="image" src="https://github.com/user-attachments/assets/acec1afb-c373-4287-9ff0-01ec498b6b02" />

Step 3:
Print the array to confirm that it had indeed contained the squares of numbers from 1 to 100 in a 10 x 10 format.
<img width="1278" height="289" alt="image" src="https://github.com/user-attachments/assets/5b8736c9-47c6-4d91-947d-f4455e618442" />


Step 4:
Use A %3==0 to get all the elements from the array A that are divisible by 3. This simply returns all of the values in an array that indicate that they obey that contingency but I stored it in a variable name div_by_3.
<img width="1276" height="73" alt="image" src="https://github.com/user-attachments/assets/ab391cc6-c877-4a91-ae88-aa4f4753ec2c" />

Step 5:
Print the outcome by to see clearly which squarings satisfied the condition.
<img width="1280" height="151" alt="image" src="https://github.com/user-attachments/assets/98dcf47d-a752-4ccf-88e5-6d46cb9291ff" />

Step 6:
Finally, I saved these findings into a div_by_3.npy file with the command np.save("div_by_3.npy", div_by_3). This means that all manipulations can now save or fetch the array without repeating all the computations.
<img width="1278" height="68" alt="image" src="https://github.com/user-attachments/assets/35be300b-68de-46ee-89d0-534c49f7a7c7" />

# -------------------------------- END --------------------------------
