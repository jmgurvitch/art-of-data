# Reading Files
Download `favorite_colors.csv` and put it in a folder named `datasets` in your Art of Data folder.

## Model A
1. What does `csv` stand for?

  Comma-separated values

3. What information does `favorite_colors.csv` contain?

  The grade of the respondent and their favorite color


## Model B
Examine and run the following snippet of code.
```py
with open("datasets/favorite_colors.csv", "r") as f:
  print(f)
```

1. What is printed when you run this code?

  `<_io.TextIOWrapper name='favorite_colors.csv' mode='r' encoding='UTF-8'>`

3. Explain the syntax of the `open()` function.

  It takes the path and filename of the file and then specifies whether we are reading or writing the file.

5. Explain what you would need to change if you wanted to _write_ to the file.

  ```py
  with open("datasets/favorite_colors.csv", "w") as f:
  print(f)
  ```

7. Explain why `open()` is called inside a **`with` statement**.

  `open` opens a connection to a desired file, and when we have received the information we want, so that we don't have to manually close the connection, we put it inside of a 'with block' in the code, which will close our connection to the file as soon as we exit the 'with block' in the code.
  

## Model C
Examine and run the following snippet of code.
```py
import csv
with open("datasets/favorite_colors.csv", "r") as f:
  data = csv.reader(f)
  for row in data:
    print(row)
```

1. What **module** is being imported? Link to the official documentation for this module.

  A .csv file is a module in python, so we are importing a csv module.
  https://docs.python.org/3/library/csv.html

3. What does `csv.reader()` return?

  

5. What is printed when you run this code?

  

7. Explain how to interpret the for-loop and `row` in terms of the `csv` file.

  


## Model D
Examine and run the following snippet of code.
```py
import csv
with open("datasets/favorite_colors.csv", "r") as f:
  data = csv.DictReader(f)
  for row in data:
    print(row)
```

1. What does `csv.DictReader()` return, and how is this different from `csv.reader()`?
1. What is printed when you run this code?
1. Explain how to interpret the for-loop and `row` in terms of the `csv` file.

## Application
Write a Python file to analyze `favorite_colors.csv` and create a **nested dictionary** that contains the answers to the following questions:
1. How many students in 9th grade put blue as their favorite color?
1. How many students in total put yellow as their favorite color?
