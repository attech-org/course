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

  console.log(generateString(111));

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
    let result = 'id, name, salary, country';
    for (let i = 0; i < 100; i++) {
      result += `\n${generateString(6)}, Agent 00${i}, ${randomNumber(100, 5000)}, UA`
    }
    return result;
  }
  console.log(generateCSV());
  ```
</details>

<!-- string/array methods -->
1. Count "e" letters in provided string (case-sensitive).
2. Count ["a", "e", "o"] letters in provided string (case-sensitive).
<!-- string/array methods + object -->
3. Calculate final balance based on provided transactions history.
4. Convert provided CSV formatted string to array of objects and calculate average salary. (new line symbol in JS is `\n`)