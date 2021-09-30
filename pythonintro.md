# Python Introduction (or Review)
You can access the `Python shell` by running `python3` in your terminal!  
I also recommend making a `sandbox.py` to test and check your answers.

1. How do you initialize a variable in Python?
   
   var = some_initial_value
   
2. How does Python distinguish between different variable types?
   
   Python determines the variable type as it goes; any variable can be any type, but if it walks like an int and talks like an int, for example, then it's an int.
   
3. Does Python check variable types **statically** or **dynamically**?
   
   Python checks variable types dynamically: the type of the variable is determined only during runtime.
   
4. What happens if you run a Python script and there is a bug?
   
   It will run until it hits the error and then halt.
   
5. Convert the following snippet into one line:
    ```py
    if (a and not b):
      return False
    else:
      return True
    ```
    
    ```py
    return(not(a or b))
    ```
1. Explain the difference between `range(1,10)` and `range(1,10,2)`.
   
   range is range(start, stop, step), where an undefined step defaults to 1, so the first expression generates a sequence from 1-10 with step 1, while the second generates the same sequence with step 2. 
   
2. Convert the following for-loop into a while-loop:
    ```py
    for i in range(2, 20, 3):
      print(i)
    ```
    ```py
    i = 2
    while(i <= 20):
       print(i)
       i+=3
    ``` 
      
    ### Write the following functions.
1. `add(x,y)` returns the sum of `x` and `y`

   ```py
   def add(x,y)
      return (x + y)
   ```

3. `larger(x,y)` returns the larger number

   ```py
   def larger(x,y):
         if(x>y):
            return x
         elif(x<y):
            return y
         else:
            return "they are equal"
   ```

5. `xor(a,b)` returns whether _exactly_ one input is True

   ```py
   def xor(a,b):
      return(a + b == 1)
   #True = 1 and False = 0, so the sum of one True and one False 1 + 0 = 1
   ```

7. `hello(n)` prints `"hello"` _n_ times
   
   ```py
   def hello(n):
      print(n*"hello \n")
   ```

9. `fraction(n)` prints the float representations of `1/2, 1/3, 1/4 ... 1/n`

   ```py
   def fraction(n):
      for n in range(2, n):
         frac = 1/(float(n))
         print(str(frac))
   ```

11. `factorial(n)` returns the factorial of _n_ (written as `n!`)

   ```py
   def factorial(n):
      total = 1
      for i in range(n+1):
         total *= i
      return total
   ```
      or
    
   ```py
   def factorial(n)
      if n == 0 or n == 1:
         return 1
      else:
         return n * factorial(n-1)
   ```

13. `stars(n)` prints a right triangle of stars with height and base _n_  
    ex: `stars(3)` should print:
    ```
    *
    **
    ***
    ```

   ```py
   def stars(n):
      for n in range(1,n+1):
         print(n*"*")
   ```
   
