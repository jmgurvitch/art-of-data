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

  It returns a list of the lines in the .csv file.
  
5. What is printed when you run this code?

  It prints the whole .csv file row by row.

7. Explain how to interpret the for-loop and `row` in terms of the `csv` file.

  It runs through every single row and prints it out.


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

  DictReader() returns a DictReader object where each row of the .csv is an element stored as a dictionary. reader() returns a reader object where each row of the .csv is stored as a list.

3. What is printed when you run this code?

  It prints two key-value pairs for each row in the .csv file of the following format: `{'grade': '11', 'favorite_color': 'blue'}`

5. Explain how to interpret the for-loop and `row` in terms of the `csv` file.

  The for loop runs through every row of the .csv file, taking the first row as the key names and matching up all subsequent rows (values) to their corresponding key names.
  

## Application
Write a Python file to analyze `favorite_colors.csv` and create a **nested dictionary** that contains the answers to the following questions:
1. How many students in 9th grade put blue as their favorite color?
3. How many students in total put yellow as their favorite color?

```py
import csv

def makeNestedDict(filePath):
      with open(filePath, "r") as f:
            data = csv.DictReader(f)
            d = {"total" : {}} #we know that "total" will be there for every nested dict, so we can make it from the get go
            for row in data:
                  if row["grade"] not in d.keys(): #if new grade
                        d[row["grade"]] = {row["favorite_color"] : 1} #make a new dict and set corresponding grade/color entry to 1
                  else: #if we've seen the grade before
                        if row["favorite_color"] not in d[row["grade"]].keys(): #if we haven't seen a certain grade/color combo before (e.g. grade 10 and red)
                              d[row["grade"]][row["favorite_color"]] = 1
                        else:
                              d[row["grade"]][row["favorite_color"]] += 1
      return d

'''d["total"] = {}
for key in list(d.keys())[1]:
      d["total"][key] = 0
      #for grade in d.keys():
            #if grade != "total":
                  #d["total"][key] += d[grade][key]
                  #print(d[grade])'''

print(makeNestedDict("favorite_colors.csv"))
```
