# Dictionaries
Examine and run the following code:

```py
story = {
  "title": "Invisible Planets",
  "author": "Hao Jingfang",
  "published": 2013
}
```

## Access
1. Describe what information the dictionary named `story` contains.

  Story contains the title string variable, the author string variable, and the published int variable.

3. What does `story['author']` return?

  Hao Jingfang

5. How does Python know that `"Hao Jingfang"` is related to `author`? Where is that relationship defined?

  The key author is defined as "Hao Jingfang"

7. In the line `story['author']`, what does the value in the square brackets represent?

  The value in the square brackets represents a key

9. Write a line of code to print the title of the story.

  print(story["title"])

10. How would you describe the **keys** and **values** of this dictionary?

  The keys of this directory are the labels (title, author, published) given to the variables, and the values are the information stored by the variables.


## Mutation
1. Run this code: `story["words"] = 6359`, and then print `story`. What changes?

  We have added a new key, words, which corresponds to the value 6359.

3. Run this code: `story["title"] = "Folding Beijing"`. What changes?

  The title value changes from "Invisible Planets" to "Folding Beijing"
  
5. Describe what the assignment operator (`=`) does in the context of dictionaries.

  "=" assigns a value to a key.

7. Write a line of code to add the key `"translator"` and value `"Ken Liu"` to `story`.

  Done

9. Run this code: `del story['published']`. What happens?

  The key "published" is removed from the dictionary.
  
11. Write a line of code to change the value of a key `"B48"` to `15` in a dictionary named `classrooms`.
12. Write a line of code to delete the entry with key `"B48"` in a dictionary named `classrooms`.

## Iteration
1. What gets printed in the following snippet of code?
    ```py
    for x in story:
      print(x)
    ```
    
  published
  author
  title
  
  It iterates upward.
  
1. What is a better name for the variable than `x`?
  
  Keys

3. How do we iterate through a dictionary's values?

  ```py
  for k, v in story.items(): #k and v are our placeholders for keys and variables. They can be named anything.
    print(k, v)
  ```
  
  items() takes story and makes a list of tuples, where each element is a key-value pair, such as `('title', 'Invisible Planets')`

5. Explain what is happening in the following snippet of code. Some useful terms are **tuple** and **unpacking**.
    ```py
    for (k,v) in story:
        print(k)
        print(v)
    ```
    We receive the error "too many values to unpack." We must change this into a list of tuples by doing story.items(). Then it prints
    ```published
    2013
    author
    Hao Jingfang
    title
    Invisible Planets```

## Application
1. Write a function `count()` that takes a list of strings as input and outputs a dictionary where each unique string is a key, and its count is the value. For example, `count(["hello", "hello", "world", "hello"])` should return `{"hello": 3, "world": 1}`


  ```py
  
  ```
