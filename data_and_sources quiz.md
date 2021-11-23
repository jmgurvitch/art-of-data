# Name: Justin Gurvitch
Please respond to the following questions. _Show your work_ if applicable, and be as _explicit_ as possible in your answers.

1. In the following snippet of code, label the name of the variable and the name of the class. Use this example to explain what an object is in the context of memory.
    ```py
    p1 = Point(2,3)
    ```
    
    In this snippet, the variable `p1` holds an object of class `Point`, meaning that there is a variable `p1` of Class point whose x and y values (assuming that `Point` refers to Cartesian points) are the inputs 2 and 3, respectively. In terms of memory, an object is something that occupies memory that a computer may later have to call upon. Because the computer has stored information about the class, which functions as a blueprint to create data entities with specific characteristics--objects--`p1` is an object of class `Point` that is called upon by the user to create a variable with the parameters of `Point`.
    
2. A researcher is conducting a survey on favorite sports and encodes each sport with a number. For example, 1=Archery, 2=Boxing, 3=Curling, and so on. They average these numbers to get 2.3 and conclude that on average, people's favorite sport is boxing on ice. Why is this incorrect?

     The researcher has assigned a numerical value to each sport for the sake of making the data computable, but this data is still not ordinal. When we try to take the mean of non-ordinal data, it has no useful meaning at all. Rather than using the mean, we should use the mode, which by definition will tell us the most frequently selected sport and thus the majority of respondents' favorite sport.

3. A researcher is conducting a study on vegetarian diets. They stand in front of a build-your-own-salad restaurant and survey people who enter. Identify the population, and explain why this is not a great sample.

    Because the researcher is conducting a study on vegetarian diets but neglects to specify which vegetarians they are studying, the best we can do is assume that the population is all vegetarians. And because the researcher surveys people who enter but neglects to specify whether they confirm that the respondents are vegetarian or not, we cannot assume that the sample is not all people who enter the restaurant. As the patrons of a build-your-own-salad restaurant must be willing to eat a principally vegetable-based meal, the chances that the share of vegetarian respondents is higher than it would be at different restaurant type is high, to be sure; even so, there are plenty of meat eaters who eat salads. As a result, the sample would include non-vegetarians but extraploate its results to vegetarians only.

4. A researcher wants to study the population of all New York City residents. What is a feasible sample frame, and what biases might this sample frame be prone to?

    Suppose a list of NYC households is available. The researcher could randomly choose a set number of households from each of the city's regions--Upper East Side, Williamsburg, West Village, etc--and contact each one to request an interview with all available members of the household. This would make the sample frame the randomly chosen set of NYC residents who live in a home. Unfortunately, this sample frame excludes the city's substantial homeless population by definition. Additionally, it is entirely possible that more residents of one neighborhood (and the definition of "neighborhood" is very subjective as well, I will add) elect to be interviewed than do residents of another neighborhood, decreasing the study's ability to accurately represent the entire NYC population.

5. A scientist conducted an observational study on mental health and calculated that the correlation between recreational drug use and depression is 0.83. Why can't they conclude that recreational drug use causes depression?

    An observational study is necessarily correlative regardless of the observed relationship between variables. Because it documents what occurs without external interference, such as the perscription of a medicine to half of the study's participants, the researchers cannot confirm that changes in one factor change another--after all, nothing was deliberately changed. 
