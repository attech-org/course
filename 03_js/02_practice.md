# Practical tasks for JS

## Level 1

To start solving this level, you should already know JS basics, cycles and functions.

### Symbols counter

1. Create a "countSymbols" function, that will count how much "a" letters contains in provided string.

   ```js
   console.log(countSymbols("Jeremy")); // 0
   console.log(countSymbols("Antony")); // 0
   console.log(countSymbols("Barack Obama")); // 4
   ```

2. Extend a "countSymbols" function, to support custom letter to search. Function receive two arguments: text and element to search in text.

   ```js
   console.log(countSymbols("Jeremy", "e")); // 2
   console.log(countSymbols("Antony", "n")); // 2
   console.log(countSymbols("Antony Smith", "s")); // 0 (because we looking for small "s", but in "Smith" we have big "S")
   ```

3. Extend "countSymbols" to make search not case sensitive.

   ```js
   console.log(countSymbols("Jeremy", "E")); // 2
   console.log(countSymbols("Antony", "n")); // 2
   console.log(countSymbols("Antony Smith", "s")); // 1
   ```

4. Add optional third argument, that will control enable/disable case sensitive search.

   ```js
   console.log(countSymbols("Antony Smith", "s", true)); // 1
   console.log(countSymbols("Antony Smith", "s", false)); // 0
   console.log(countSymbols("Antony Smith", "s")); // 0
   ```

### AntiSpy

1. Create "antiSpy" function that will replace any email address in provided text with "HIDDEN_DATA" string.

   ```js
   const text =
     "If you agree with that, just let me know to obama@mail.us or newpower@gmail.com and I'll reach out as soon as possible.";
   ```

   ```js
   console.log(antiSpy(text)); // "If you agree with that, just let me know to HIDDEN_DATA or HIDDEN_DATA and I'll reach out as soon as possible."
   ```

2. Extend "antiSpy" function with optional second argument, that will be a string used to hide data. If argument not provided, should be used "HIDDEN_DATA" string.

   ```js
   const text =
     "If you agree with that, just let me know to obama@mail.us and I'll reach out as soon as possible.";
   ```

   ```js
   console.log(antiSpy(text)); // "If you agree with that, just let me know to HIDDEN_DATA or HIDDEN_DATA and I'll reach out as soon as possible."
   console.log(antiSpy(text, "MY_MAIL")); // "If you agree with that, just let me know to MY_MAIL or MY_MAIL and I'll reach out as soon as possible."
   console.log(antiSpy(text, "XXXX")); // "If you agree with that, just let me know to XXXX or XXXX and I'll reach out as soon as possible."
   ```

## Level 2

To start solving this level, you should already know [Level 1](#level-1) + objects, arrays

### Text builder

1. Create a function `postBuilder` that will receive two arguments: object with values, and text. This function should help to fill text in templates. Logic should calculate the WINNER based on score. If game results is draft - WINNER value should be "both teams".

   ```js
   const template = "%TEAM_A% vs %TEAM_B% game score is %SCORE%. Fans of %WINNER% already started celebrating on the streets of the %GAME_CITY%, %GAME_COUNTRY%".
   ```

   ```js
   console.log(
     postBuilder(template, {
       teamAGameScore: 2,
       teamBGameScore: 0,
       teamA: "Barcelona FC",
       teamB: "Inter Milan",
       city: "Milan",
       country: "Italy",
     })
   ); // "Barcelona FC vs Inter Milan game score is 2:0. Fans of Barcelona FC are already started celebrating on the streets of the Milan, Italy."
   console.log(
     postBuilder(template, {
       teamAGameScore: 0,
       teamBGameScore: 3,
       teamA: "Barcelona FC",
       teamB: "Inter Milan",
       city: "Milan",
       country: "Italy",
     })
   ); // "Barcelona FC vs Inter Milan game score is 0:3. Fans of Inter Milan are already started celebrating on the streets of the Milan, Italy."
   console.log(
     postBuilder(template, {
       teamAGameScore: 0,
       teamBGameScore: 0,
       teamA: "Barcelona FC",
       teamB: "Inter Milan",
       city: "Milan",
       country: "Italy",
     })
   ); // "Barcelona FC vs Inter Milan game score is 0:0. Fans of both teams are already started celebrating on the streets of the Milan, Italy."
   ```

### Sorting

1. Create a function `sortByAge` that will sort array of object based on "age" key.

   ```js
   const students = [
     { name: "Alex", age: 27 },
     { name: "Deny", age: 25 },
     { name: "Max", age: 20 },
   ];
   const teachers = [
     { name: "Tommy", age: 33, experience: 10, skillsId: 1 },
     { name: "Lora", age: 44, experience: 12, skillsId: 2 },
     { name: "Rafat", age: 35, experience: 3, skillsId: 3 },
   ];
   ```

   ```js
   console.log(sortByAge(students)); // order: Max, Deny, Alex
   console.log(sortByAge(teachers)); // order: Tommy, Rafat, Lora
   ```

2. Create a function `sortBy` that will sort by provided as a second argument key. Adding support by "name" is optional, but very appreciated. Pay attention, that sorting by numbers works a bit different from sorting by string. Good thing to research.

   ```js
   console.log(sortBy(students, "age")); // order: Max, Deny, Alex
   console.log(sortBy(teachers, "experience")); // order: Rafat, Tommy, Lora
   ```

3. Create a function `sortBySkills` that will sort by values from another array. Function should take two arguments, match skills data from one array to another using id, and sort teachers based on count of skills. Lora has "skillsId" equal 2, and it match with `["chemistry", "physics", "math", "english"]`, and it means, that she has 4 skills.

   ```js
   const skillsInfo = [
     {
       id: 1,
       items: ["math", "english"],
     },
     {
       id: 2,
       items: ["chemistry", "physics", "math", "english"],
     },
     {
       id: 3,
       items: ["chemistry"],
     },
   ];
   ```

   ```js
   console.log(sortBySkills(teachers, skillsInfo)); // order: Lora, Tommy, Rafat
   ```

### God-mode

1. Create a constructor `World` that will have next keys and methods:

   - `planetName` - string with planet name
   - `species` - array with all supported species
   - `creatures` - array of all created items
   - `changePlanetName(newName)` - method that change "planetName"
   - `create(data)` - method that create a new "creature" with provided data and push it to "creatures" list. If data contain a new "specie", that's not exist in "species", it should be added.
   - `countPopulation()` - method that return object with all species as keys, and their count as values

   ```js
   const home = new World();
   home.changePlanetName("Earth");
   console.log(home.planetName); // Earth
   console.log(home.species); // []
   console.log(home.creatures); // []
   console.log(home.countPopulation()); // {}
   home.create({
     name: "human",
     specie: "homo sapiens",
   });
   home.create({
     name: "penguin",
     specie: "bird",
   });
   home.create({
     name: "swan",
     specie: "bird",
   });
   console.log(home.species); // ["homo sapiens", "bird"]
   console.log(home.creatures); // [{ name: "human", specie: "homo sapiens" }, { name: "penguin", ...
   console.log(home.countPopulation()); // { "homo sapiens": 1, bird: 2 }
   ```

> P.S: Don't blame me for namings, I know that "homo sapiens" and "bird" it's not specie =)

### Aggregation

1. Create a function `aggregate` that extends data in array of objects by ids.

    ```js
    const users = [
      {
        id: '8o71g807b09hvd09h1',
        firstName: 'John',
        lastName: 'Smith'
      },
      {
        id: '9we8rn4e98161684s9',
        firstName: 'Marcus',
        lastName: 'Davis'
      },
      {
        id: '78y78t4ygd984y5c16',
        firstName: 'Anna',
        lastName: 'Rogers'
      }
    ];

    const banks = [
      {
        id: '8s7b4s87d4s7e7ee',
        name: 'PrivatBank',
        country: 'Ukraine'
      },
      {
        id: 'df87ndre78r7ee13',
        name: 'UniversalBank',
        country: 'Ukraine'
      },
      {
        id: '28741hfhdfddsaaa',
        name: 'Revolut',
        country: 'UK'
      },
    ];

    const currencies = [
      {
        id: '127122v2',
        short: 'UAH',
        full: 'Ukrainian Hryvnya'
      },
      {
        id: '914184g4',
        short: 'USD',
        full: 'United States Dollar'
      },
      {
        id: '1981vgd4',
        short: 'EUR',
        full: 'Euro'
      },
    ];

    const payments = [
      {
        id: 1,
        sender: {
          userId: '8o71g807b09hvd09h1',
          bankId: 'df87ndre78r7ee13',
          currencyId: '1981vgd4'
        },
        receiver: {
          userId: '9we8rn4e98161684s9',
          bankId: '8s7b4s87d4s7e7ee',
          currencyId: '127122v2'
        }
      },
      {
        id: 2,
        sender: {
          userId: '78y78t4ygd984y5c16',
          bankId: '28741hfhdfddsaaa',
          currencyId: '127122v2'
        },
        receiver: {
          userId: '9we8rn4e98161684s9',
          bankId: '28741hfhdfddsaaa',
          currencyId: '127122v2'
        }
      },
    ]
    ```

    ```js
   aggregate(payments, users, banks, currencies); // should return array of payments objects with extended data from related arrays

   // example of result payment object:
   // {
   //     id: 1,
   //     sender: {
   //       userId: '8o71g807b09hvd09h1',
   //       userData: {
   //         id: '8o71g807b09hvd09h1',
   //         firstName: 'John',
   //         lastName: 'Smith'
   //       },
   //       bankId: 'df87ndre78r7ee13',
   //       bankData: {
   //         id: 'df87ndre78r7ee13',
   //         name: 'UniversalBank',
   //         country: 'Ukraine'
   //       },
   //       currencyId: '1981vgd4',
   //       currencyData: {
   //         id: '1981vgd4',
   //         short: 'EUR',
   //         full: 'Euro'
   //       }
   //     },
   //     ...
   // }
   ```

## Level 3

To start solving this level, you should already know [Level 2](#level-2) + promise, async/await

### Pizzeria

>NOTE: To count time of function run, you can use `console.time(NAME)` and `console.timeEnd(NAME)`. For example:
>```js
>console.time('myFunction');
>
>myFunction()
>   .then(() => {
>     console.timeEnd('myFunction'); // myFunction: 13055.76904296875 ms
>   })
>```

1. Create `pizzaCooking` async function, that will receive two arguments: "pizzaName" - name of pizza and "ovenTime" number of milliseconds that need to bake a pizza. Function should wait for "ovenTime" milliseconds to resolve. Use only Promise API, without async/await syntax.

   ```js
   pizzaCooking("margarita", 5400).then((message) => console.log(message)); // (should resolve in 5.4s) margarita is done
   pizzaCooking("diabola", 3200).then((message) => console.log(message)); // (should resolve in 3.2s) diabola is done
   ```

2. Create `idealKitchen` async function, that will receive one argument with array of pizza orders, and using `pizzaCooking` function from previous step for baking pizzas from order. For this task you have unlimited ovens, that means infinite count of pizzas can be baked in parallel. The `idealKitchen` function should resolve when all pizzas is done, and should return array of messages "PIZZA_NAME is done". Use only Promise API, without `async/await` syntax.

   ```js
   const orders = [
     { name: "margarita", ovenTime: 5400 },
     { name: "diabola", ovenTime: 3200 },
     { name: "peperoni", ovenTime: 2500 },
   ];
   ```

   ```js
   // should resolve in 5.4s, because all pizzas bakes in parallel, and time shouldn't add up
   // oven1: margarita ======> 5.4
   // oven2: diabola   ===> 3.2
   // oven3: peperoni  ==> 2.5
   idealKitchen(orders).then((messages) => console.log(messages)); // ['margarita is done', 'diabola is done', 'peperoni is done']
   ```

3. As you know, nothing is ideal, so let's create `realKitchen` async function. It should do the same thing as `idealKitchen`, like receiving orders, and resolve when all pizzas is done, but with one limitation. Second argument "ovensCount" will say how much pizzas can bake at time. Imagine it as a real kitchen with real ovens. For example, you have 10 orders and 2 ovens, so it means that you can break orders between ovens to bake all orders faster. For this task feel free to use `async/await` instead of pure Promise API.

   ```js
   const orders = [
     { name: "margarita", ovenTime: 5400 },
     { name: "bbq", ovenTime: 1800 },
     { name: "bbq", ovenTime: 1800 },
     { name: "margarita", ovenTime: 5400 },
     { name: "diabola", ovenTime: 3200 },
     { name: "peperoni", ovenTime: 2500 },
     { name: "margarita", ovenTime: 5400 },
     { name: "hawaiian", ovenTime: 2000 },
     { name: "bbq", ovenTime: 1800 },
     { name: "seafood", ovenTime: 2100 },
     { name: "peperoni", ovenTime: 2500 },
   ];
   ```

   ```js
   // should resolve in max 24.4s, because we can bake only 2 pizzas in parallel
   // oven1: margarita ======5.4=> margarita ======5.4=> diabola ===3.2=> ...
   // oven2: bbq ==1.8=> peperoni ===2.5=> seafood ==2.1=> ...
   realKitchen(orders, 2).then((messages) => console.log(messages)); // ['margarita is done', ...]
   ```

4. Try to improve `realKitchen` function with smarter algorithm, that baking order in fastest way. Let's call this function `chiefKitchen`. Tip: think how to split orders between ovens to have a balance. For this task feel free to use `async/await` instead of pure Promise API.

    ```js
    const orders = [
      { name: "margarita", ovenTime: 5400 },
      { name: "bbq", ovenTime: 1800 },
      { name: "bbq", ovenTime: 1800 },
      { name: "margarita", ovenTime: 5400 },
      { name: "diabola", ovenTime: 3200 },
      { name: "peperoni", ovenTime: 2500 },
      { name: "margarita", ovenTime: 5400 },
      { name: "hawaiian", ovenTime: 2000 },
      { name: "bbq", ovenTime: 1800 },
      { name: "seafood", ovenTime: 2100 },
      { name: "peperoni", ovenTime: 2500 },
    ];
    ```

    ```js
    // should resolve in max 16.9s
    realKitchen(orders, 2).then((messages) => console.log(messages)); // ['margarita is done', ...]
    ```
