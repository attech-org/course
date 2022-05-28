# Forms in React

In this part we're going to practice with forms in React. In each task, you need to implement the [same logic](#main-task), but using different stack.

### Logic
Create form with validation rules. Validation should be real-time, and show error message immediately, when user enter wrong value. When user press "SEND", data should be shown to console.

Rules:
  - email:
    - required
    - should be valid email
    - should be unique (show this error if value will match with one of addresses: ['admin@test.com', 'hacker@anonim.us'])
  - username:
    - required
    - should contain only small letters, numbers and underscore ("_"). Any other characters not allowed
    - min length: 5 symbols
    - max length: 30 symbols
  - phone number:
    - required
    - should be valid phone number
    - should be based on Ukraine dial code "+380"
  - years old:
    - min value: 18
    - max value: [122](https://en.wikipedia.org/wiki/List_of_the_verified_oldest_people)
  - message
    - required
    - min length: 100 symbols
    - max length: 1000 symbols

Image:
![general](https://user-images.githubusercontent.com/28801003/170842413-591da66a-538c-4706-b7ac-2cd259c2204e.png)

> NOTE: Use [styled-components](https://www.npmjs.com/package/styled-components) as styling tool.

## Task 0

Initialize boilerplate react application using [CRA](https://www.npmjs.com/package/create-react-app). Add routing functionality, and every next task should have separate route.

## Task 1

Create form component `<Task1Form />` on `/forms/task-1` route using pure React component state.

## Task 2

Create form component `<Task2Form />` on `/forms/task-2` route using [react-hook-form](https://www.npmjs.com/package/react-hook-form) and [yup](https://www.npmjs.com/package/yup).

## Task 3

Create form component `<Task3Form />` on `/forms/task-3` route using [formik](https://www.npmjs.com/package/formik) and [joi](https://www.npmjs.com/package/joi).
