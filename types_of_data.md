# Different Types of Data

## CS Types of Data
We've talked about different types of data before when thinking about writing code. Let's review what *type* means in the context of computer science.

1. What are some different types of data you've worked with? _Hint: what's a class?_

A class is a user-defined blueprint or prototype from which objects are created. Classes provide a means of bundling data and functionality together. Creating a new class creates a new type of object, allowing new instances of that type to be made.

3. What happens if you try to average a list of strings?

Assuming that average means arithmetic/geometric average, it will not work because we are trying to perform a string-incompatible function on a string.

5. Why is a variable's type important?

A variable's type determines the values that the variable can have and the operations that can be performed on it.


## Statistical Types of Data
In statistics, a variable's type means something different compared to what we've seen in computer science.

1. What is a statistical variable, and how is it different from a computer science variable?
2. Why is a statistical variable's type important?

### Vocabulary
I encourage you to search online for these answers! Try to respond in your own words.
1. What is the difference between a **quantitative** and a **qualitative** variable?

Quantitative data expresses some quantity (value). Qualitative data is usually written and is non numerical (description).

3. What is the difference between a **discrete** and a **continuous** variable? Are these quantitative or qualitative?

A set of data is said to be continuous if the values belonging to the set can take on any value within a finite or infinite interval. A set of data is said to be discrete if the values belonging to the set are distinct and separate.

5. What is the difference between a **nominal** and an **ordinal** variable? Are these quantitative or qualitative?

Data whose possible values have an inherent order but can be both quantitative or qualitative. For example, data that is the natural numbers has an inherent order because 1 comes before 2, 2 before 3, etc. Another example is a feedback survey from “not satisfied” to “very satisfied,” where there is a defined order of the options. In contrast, nominal data is unordered and quantitative. For example, a short-answer response question where you type in a sentence. If you typed in a number, it would still be ordinal because any number you input has an order in the scheme of numbers.

7. What is a qualitative variable that's not **categorical**?

A short-response answer is qualitative but not categorical because everyone can say something unique. Categorical data is discrete data that has a specific number of possible values.

### Application
1. A researcher is studying children’s favorite colors. They label each color with a number -- for example, they record red as 1, blue as 2, green as 3, and so on. Later on, when they are analyzing their data, they find that the average favorite color is 2.78, and conclude that children like the color blue-green. Discuss the issues that led to this erroneous conclusion.

We assign a numerical value to each color for the sake of coding, but this data is still not ordinal. When we try to take the mean of non-ordinal data, it has no useful meaning at all. Rather than using the mean, we should use the mode: means obscure individuals, whereas modes literally tell you the number of kids for each color. 

3. A researcher is studying student burnout. What questions might they want to ask, and what data would they record? What are possible analyses of this data, and how do those analyses depend on the data types?

We could collect a combination of ordinal data (hours of sleep, test scores) and nominal data (short-answer anecdotes about stress).
