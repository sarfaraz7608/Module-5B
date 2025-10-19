# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

## 🧾 Program
```
import numpy as np

# Example 2D NumPy array
arr = np.array([[10, 6,9],
                [9, 5, 4],
                [4, 8, 3]])

# Sort each column in ascending order using axis=0
sorted_arr = np.sort(arr, axis=0)

print("Original array:")
print(arr)
print("\nColumn-wise sorted array:")
print(sorted_arr)
```


## Output
<img width="1920" height="1080" alt="Screenshot 2025-10-19 172111" src="https://github.com/user-attachments/assets/19a8bd85-8767-46e6-9e58-504832b44cbc" />

## Result
Thus To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order has been executed sucessfully.

# # NumPy Program: Find Indices Where Elements in Array x are Greater Than or Equal to Corresponding Elements in Array y

## 🎯 Aim
To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y`.

## 🧠 Algorithm
1. **Import NumPy**: Import the NumPy library.
2. **Define Arrays**: Define two NumPy arrays, `x` and `y`, with the same shape (i.e., same number of elements).
3. **Use Boolean Indexing**: 
   - `x > y` gives a boolean array where elements of `x` are greater than `y`.
   - `x == y` gives a boolean array where elements of `x` are equal to `y`.
4. **Find Indices**: Use `np.where()` to get the indices where the conditions `x >= y` are satisfied.
5. **Print Indices**: Print the indices where the condition holds true.

## 🧾 Program
```
import numpy as np

# Define two arrays x and y of the same shape
x = np.array([1, 3, 5, 7, 9])
y = np.array([2, 3, 4, 8, 7])

# Find indices where elements in x are greater than or equal to elements in y
indices = np.where(x >= y)

print("Indices where x >= y:", indices[0])
```

## Output
<img width="1920" height="1080" alt="Screenshot 2025-10-19 172651" src="https://github.com/user-attachments/assets/081298bd-e85e-42c6-a527-aecb3c5e88b2" />

## Result
Thus To write a Python program using **NumPy** that finds the indices where elements in array `x` are greater than or equal to their corresponding elements in array `y` has been executed sucessfully.

# NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program
```
import numpy as np

# Example original 2D array
arr = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])

# Example new column to insert
new_col = np.array([10, 11, 12])

# Delete the second column (index 1)
arr_deleted = np.delete(arr, 1, axis=1)

# Insert the new column at index 1
arr_updated = np.insert(arr_deleted, 1, new_col, axis=1)

print("Original array:")
print(arr)
print("\nUpdated array after replacing second column:")
print(arr_updated)
```

## Output
<img width="1920" height="1080" alt="Screenshot 2025-10-19 173226" src="https://github.com/user-attachments/assets/08e35849-4c52-4ac8-8aa0-b4a9ab3e7a9c" />

## Result
Thus To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position has been executed sucessfully.


# Pandas Program: Create and Display a DataFrame with Custom Index Labels

## 🎯 Aim

To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows.

---

## 🧠 Algorithm

1. **Import Libraries**: Import the required libraries – `pandas` and `numpy`.
2. **Create Dictionary**: Define a dictionary `exam_data` with keys: `'name'`, `'score'`, `'attempts'`, and `'qualify'`.
3. **Index Labels**: Create a list of custom index labels called `labels`.
4. **Create DataFrame**: Use `pd.DataFrame()` to create the DataFrame by passing the dictionary and index labels.
5. **Display Output**: Display the DataFrame using `print()` or by simply calling the DataFrame variable.

---

## 💻 Program
```
import pandas as pd
import numpy as np

# Define the input dictionary
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}

# Define custom index labels
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

# Create DataFrame with custom index
df = pd.DataFrame(exam_data, index=labels)

# Display DataFrame
print(df)
```

## Output
<img width="1920" height="1080" alt="Screenshot 2025-10-19 173640" src="https://github.com/user-attachments/assets/0c7b2c4b-274d-47ae-8731-af1bf42c519c" />

## Result
Thus To create and display a **DataFrame** using the **Pandas** library in Python from a given dictionary, and apply specific index labels to the rows has been executed sucessfully.

# 🧪 Pandas Program: Join Two DataFrames Along Rows

## 🎯 AIM

To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame.

---

## 🧠 ALGORITHM

1. **Import Libraries**: Import the `pandas` library.
2. **Create First DataFrame**: Use a dictionary to create `student_data1`.
3. **Create Second DataFrame**: Use another dictionary to create `student_data2`.
4. **Concatenate DataFrames**: Use `pd.concat()` with `axis=0` to concatenate both DataFrames row-wise.
5. **Display Result**: Print the new combined DataFrame.

---

## 💻 Program
```
import pandas as pd

# Create first DataFrame
student_data1 = {
    'name': ['Alice', 'Bob', 'Charlie'],
    'age': [24, 27, 22],
    'grade': ['A', 'B', 'C']
}
df1 = pd.DataFrame(student_data1)

# Create second DataFrame
student_data2 = {
    'name': ['David', 'Eva', 'Frank'],
    'age': [23, 26, 28],
    'grade': ['B', 'A', 'C']
}
df2 = pd.DataFrame(student_data2)

# Concatenate DataFrames row-wise (along axis=0)
combined_df = pd.concat([df1, df2], axis=0)

# Display the combined DataFrame
print(combined_df)
```

## Output
<img width="1920" height="1080" alt="Screenshot 2025-10-19 174034" src="https://github.com/user-attachments/assets/348b6b0e-015a-4509-a489-7d81e11527fd" />

## Result
Thus To write a Python program using Pandas to **join two DataFrames along rows** (row-wise concatenation) and assign all data to a new DataFrame has been executed sucessfully.
