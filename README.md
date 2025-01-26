# Python-Assignment-7-Numpy-pandas
This  Assignment explains about the Numpy and Pandas in Python
# Exercise 1:Create a numpy array containing the numbers from 1 to 10, and then reshape it to a 2x5 matrix
import numpy as np
a1=np.array([1,2,3,4,5,6,7,8,9,10])
print(a1)
new_array=a1.reshape(2,5)                   #reshape 
print(new_array)
print(new_array.shape)

# Exercise 2:Create a numpy array containing the numbers from 1 to 20, and then extract the elements between the 5th and 15th index. 
array = np.arange(1, 21)
array
extracted_elements = array[5:15]
array, extracted_elements

# Exercise 3:Create a Pandas series with the following data: {'apples': 3, 'bananas': 2, 'oranges': 1}. Then, add a new item to the series with the key 'pears' and the value 4.
import pandas as pd 
fruits = pd.Series({'apples': 3, 'bananas': 2, 'oranges': 1})
print(fruits)
# Adding a new item 'pears' with the value 4
fruits['pears'] = 4
fruits

# Exercise 4:Create a dataframe with the following columns: name, age, and gender. The dataframe should have 10 rows of data.
import pandas as pd
import numpy as np

details= pd.DataFrame({
    'name': ["ajay","arun","sruthi","renju","afsal","sabith","jennifer","akash","kiran","vidhya"],
    'age': [26,25,24,30,45,25,35,25,24,29],
    'gender':["male","male","female","male","male","male","female","male","male","female"]
    },columns=['name','age','gender'])

details.index=[1,2,3,4,5,6,7,8,9,10]
details

# Exercise 5:Add a new column to the data frame created in question 1, called occupation. The values for this column should be Programmer, Manager, and Analyst, corresponding to the rows in the dataframe.
details["Occupation"] = ["Programmer", "Manager", "Analyst","Developer","Senior analyst",
                         "Marketing manager","Junior developer","Programmer","System analyst","Business analyst"]
details

# Exercise 6: Select the rows of the dataframe where the age is greater than or equal to 30.
details["age"]>=30

# Exercise 7:Convert this dataframe to a csv file and read that csv file, finally display the contents.
details.to_csv("final_details.csv")

data=pd.read_csv("final_details.csv")
details
