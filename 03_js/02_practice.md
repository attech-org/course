# Practical tasks for JS

<!-- ## Mock data

<details>
  <summary>users</summary>

  ```
  const users = [
    {
      "_id": "1",
      "name": "Ryu",
      "health": 45,
      "attack": 4,
      "defense": 3,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/ryu-hdstance.gif"
    },
    {
      "_id": "2",
      "name": "Dhalsim",
      "health": 60,
      "attack": 3,
      "defense": 1,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/dhalsim-hdstance.gif"
    },
    {
      "_id": "3",
      "name": "Guile",
      "health": 45,
      "attack": 4,
      "defense": 3,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/guile-hdstance.gif"
    },
    {
      "_id": "4",
      "name": "Zangief",
      "health": 60,
      "attack": 4,
      "defense": 1,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/zangief-hdstance.gif"
    },
    {
      "_id": "5",
      "name": "Ken",
      "health": 45,
      "attack": 3,
      "defense": 4,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/ken-hdstance.gif"
    },
    {
      "_id": "6",
      "name": "Bison",
      "health": 45,
      "attack": 5,
      "defense": 4,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/bison-hdstance.gif"
    },
    {
      "_id": "7",
      "name": "Chun-Li",
      "health": 40,
      "attack": 3,
      "defense": 8,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/chunli-hdstance.gif"
    },
    {
      "_id": "8",
      "name": "Blanka",
      "health": 80,
      "attack": 8,
      "defense": 2,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/blanka-hdstance.gif"
    },
    {
      "_id": "9",
      "name": "E.Honda",
      "health": 50,
      "attack": 5,
      "defense": 5,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/ehonda-hdstance.gif"
    },
    {
      "_id": "10",
      "name": "Balrog",
      "health": 55,
      "attack": 4,
      "defense": 6,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/balrog-hdstance.gif"
    },
    {
      "_id": "11",
      "name": "Vega",
      "health": 50,
      "attack": 4,
      "defense": 7,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/vega-hdstance.gif"
    },
    {
      "_id": "12",
      "name": "Sagat",
      "health": 55,
      "attack": 4,
      "defense": 6,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/sagat-hdstance.gif"
    },
    {
      "_id": "13",
      "name": "Cammy",
      "health": 45,
      "attack": 4,
      "defense": 7,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/cammy-hdstance.gif"
    },
    {
      "_id": "14",
      "name": "Fei Long",
      "health": 80,
      "attack": 2,
      "defense": 3,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/feilong-hdstance.gif"
    },
    {
      "_id": "15",
      "name": "Dee Jay",
      "health": 50,
      "attack": 5,
      "defense": 5,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/deejay-hdstance.gif"
    },
    {
      "_id": "16",
      "name": "T.Hawk",
      "health": 60,
      "attack": 5,
      "defense": 3,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/thawk-hdstance.gif"
    },
    {
      "_id": "17",
      "name": "Akuma",
      "health": 70,
      "attack": 5,
      "defense": 5,
      "source": "http://www.fightersgeneration.com/np5/char/ssf2hd/akuma-hdstance.gif"
    }
  ]
  ```
</details> -->

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
   console.log(students); // order: Max, Deny, Alex
   console.log(teachers); // order: Tommy, Rafat, Lora
   ```

2. Create a function `sortBy` that will sort by provided as a second argument key. Adding support by "name" is optional, but very appreciated. Pay attention, that sorting by numbers works a bit different from sorting by string. Good thing to research.

   ```js
   console.log(students, "age"); // order: Max, Deny, Alex
   console.log(teachers, "experience"); // order: Rafat, Tommy, Lora
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
   console.log(teachers, skillsInfo); // order: Lora, Tommy, Rafat
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

## Level 3

To start solving this level, you should already know [Level 2](#level-2) + promise, async/await