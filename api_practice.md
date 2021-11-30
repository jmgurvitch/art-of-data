# API Practice
Let's clean up the `pokemon_mess.csv` with code this time. We're going to use a Pokemon API.

## Accessing the API
1. Look at [this documentation for the Pokemon API](https://pokeapi.co/docs/v2#pokemon). What is the baseurl and endpoint?

 The baseurl is https://pokeapi.co/api/v2/pokemon/ and the endpoint is the name of the Pokemon that you append to the end of the baseurl.

2. What is the url for getting information for `steelix`? What happens if you try `Steelix`?

 https://pokeapi.co/api/v2/pokemon/steelix is the url. If we try https://pokeapi.co/api/v2/pokemon/Steelix, the API says that the data is "not found" because it stores the data for steelix only at the address with a lowercase s.

## Setup
1. Write a `Pokemon` class that encapsulates all the information you need to clean the csv. The `__str__` method should return the corresponding clean line of the csv.

 ```py
 class Pokemon:
    def __init__(self, id, name, height, weight, type1, type2):
        self.id = id
        self.name = name
        self.height = height
        self.weight = weight
        self.type1 = type1
        self.type2 = type2

    def __str__(self):
        return f"{self.id},{self.name},{self.height},{self.weight},{self.type1},{self.type2}"
```

## Cleanup
Write a Python file that outputs a `pokemon.csv`, which is a clean version of `pokemon_mess.csv`.

Some steps that might help are:
 - reading in the `pokemon_mess.csv`
 - using the name from that data to query the API
 - using the API data to construct `Pokemon` objects
 - using the `__str__` method to print the correct csv

If your program works as intended, the following terminal command should produce the clean csv:  
`python3 clean_pokemon.py > pokemon.csv`
