# Exam JS

<details>
  <summary>helpers</summary>

  ```js
  // https://stackoverflow.com/a/1349426/10253954
  const generateString = (length) => {
    let result = "";
    const characters =
      "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789";
    const charactersLength = characters.length;
    for (var i = 0; i < length; i++) {
      result += characters.charAt(Math.floor(Math.random() * charactersLength));
    }
    return result;
  }

  console.log(generateString(300));

  const randomNumber = (min, max) => Math.floor(Math.random() * (max - min) + min);

  const generateTransactionsHistory = (length) => {
    const result = [];
    for (let i = 0; i < length; i++) {
      result.push({
        id: generateString(6),
        amount: randomNumber(-1000, 1000),
        currency: "UAH",
      })
    }
    return result;
  }
  console.log(generateTransactionsHistory(50));

  const generateCSV = () => {
    let result = 'id, name, payment, country';
    for (let i = 0; i < 100; i++) {
      result += `\n${generateString(6)}, Agent 00${randomNumber(0, 9)}, ${randomNumber(100, 5000)}, UA`
    }
    return result;
  }
  console.log(generateCSV());
  ```
</details>


### Ticket #1
<!-- string/array methods -->
1. Count "e" letters in provided string (case-sensitive).
2. Count ["a", "e", "o"] letters in provided string (case-sensitive).
<!-- string/array methods + object -->
3. Calculate final balance based on provided transactions history, using "amount" property.
4. Convert provided CSV formatted string to array of objects and calculate average payment. (new line symbol in JS is `\n`)


### Ticket #2
<!-- string/array methods -->
1. Count all letters in provided string ignoring "x" symbol (case-sensitive).
2. Count sum of position numbers of all "r" letter in provided string (case-sensitive).
<!-- string/array methods + object -->
3. Calculate total expenses based on provided transactions history, using "amount" property.
4. Convert provided CSV formatted string to array of objects, calculate total payments for each Agent and find biggest sum. (new line symbol in JS is `\n`)
