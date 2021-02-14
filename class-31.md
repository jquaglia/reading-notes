# Class 01

## Review, Research and Discussion

1. **_Describe (in plain English) what `Array.map()` does._**

    - An `array` is a group of things.

    - `.map()` is a method (function) that takes the array it is called on, executes some sort of logic or (callback function) on each of the items in the array and returns a new array with new items.

    - [More info on `Array.map()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

1. **_Describe (in plain English) what `Array.reduce()` does._**

    - `.reduce()` is a method also executed on an array.

    - Like `.map()`, it executes some logic or (callback function) on each of the items in the array.

    - `.reduce()` has something called an accumulator though which is a value remembered across each iteration through the array. (something remembered as the callback function does the logic on each thing in the array)

    - The final return of `.reduce()` becomes the value of the accumulator

    - While the value of accumulator is itself a single thing, the single thing may be something with many things inside (such as another array)

    - [More info on `Array.reduce()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

1. **_Provide code snippets showing how to use `superagent()` to fetch data from a URL and log the result._**

    - _With normal Promise `.then()` syntax_

        - First you will add this line to the top of your js file

        ```javascript
        const superagent = require('superagent');
        ```

        - Then you will want to use superagent to call the API

        ```javascript
        function getPokemonData() {
          superagent.get('https://pokeapi.co/api/v2/pokemon?limit=3/')
            .then(results => {
              console.log(results.body)
            })
            .catch(err => console.error(err));
        };
        
        getPokemonData();
        ```

        - Data comes back in `results.body` and the word results is `banana` (it can be whatever word you choose)

        - Also best practice to have a `.catch()` on the end in case you get any errors

        - This is what comes back from that result:

        ```json
        {
          "count": 1118,
          "next": "https://pokeapi.co/api/v2/pokemon?offset=3&limit=3",
          "previous": null,
          "results": [
              {
                "name": "bulbasaur",
                "url": "https://pokeapi.co/api/v2/pokemon/1/"
              },
              {
                "name": "ivysaur",
                "url": "https://pokeapi.co/api/v2/pokemon/2/"
              },
              {
                "name": "venusaur",
                "url": "https://pokeapi.co/api/v2/pokemon/3/"
              }
          ]
      }
      ```

    - Again with `async` / `await` syntax

        - Again the first thing you will need to do is add this line to the top of your js file

        ```javascript
        const superagent = require('superagent');
        ```

        - Then you will make the API call again this time using different syntax

        ```javascript
        async function getPokemonData() {
          const results = await superagent.get('https://pokeapi.co/api/v2/pokemon?limit=3/');
          console.log(results.body);
        }

        getPokemonData();
        ```

        - You get back the same results:

        ```json
        {
          "count": 1118,
          "next": "https://pokeapi.co/api/v2/pokemon?offset=3&limit=3",
          "previous": null,
          "results": [
              {
                "name": "bulbasaur",
                "url": "https://pokeapi.co/api/v2/pokemon/1/"
              },
              {
                "name": "ivysaur",
                "url": "https://pokeapi.co/api/v2/pokemon/2/"
              },
              {
                "name": "venusaur",
                "url": "https://pokeapi.co/api/v2/pokemon/3/"
              }
          ]
      }
      ```

1. **_Explain `promises` as though you were mentoring a Code 301 level student._**

    - A promise is something returned from asynchronus code while waiting for the code to execute.

    - For example, in the `superagent` API call above, superagent sends out to that url to get info.

    - This takes a long time compared to executing the rest of the code.

    - Instead of waiting for all of the info to come back from the API before moving on, a `promise` is returned first.

    - This lets js to go through and get as many things done in the code as possible before the `promise` is returned with actual info.

    - This speeds up the process of running the code.

    - The `promise` is a proxy for a value not yet known when the promise is created.

    - [More about `Promises`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)

1. **_Are all callback functions considered to be Asynchronous? Why or Why Not?_**

    - No.

    - For example, the callback used by `Array.filter()` is not asynchronous. This is because it is completed right there when run.

    - The way to know which callbacks are asynchronous vs synchronous is from reading the docs/getting to use them more.

    - Typically callbacks involving requests for external resources are asynchronous and others may or may not be. (need to read docs)

[back to README](README.md)
