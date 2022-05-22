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

## Level 3

To start solving this level, you should already know [Level 2](#level-2) + promise, async/await
