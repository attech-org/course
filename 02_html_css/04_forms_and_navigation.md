# Forms and navigation

Create a new repo for this task and publish it to GitHub Pages.

## Task 0
Research next topics:
- Links and navigation (complete tasks inside): https://developer.mozilla.org/ru/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks
- HTML Forms (complete tasks inside): https://developer.mozilla.org/ru/docs/Learn/Forms

## Task 1
Using only HTML and CSS implement form with next requirements:

- no JS
- form styles is optional, so feel free to show your UI/UX skills
- each form input should use proper ["type"](https://www.w3schools.com/html/html_form_input_types.asp)

### Images:

  <details>
    <summary>empty</summary>

    ![empty form](https://user-images.githubusercontent.com/28801003/167963161-ee2b9897-5251-4f73-baf8-2622447305bc.png)

  </details>

  <details>
    <summary>autocomplete</summary>

    ![autocomplete form](https://user-images.githubusercontent.com/28801003/167963343-702b6497-b2b5-4954-8658-23b1c1b8104f.png)

  </details>

  <details>
    <summary>required validation</summary>

    ![required field validation](https://user-images.githubusercontent.com/28801003/167963648-40064ca1-f30c-49f4-91f6-9c3720bf0be6.png)

  </details>

  <details>
    <summary>type validation</summary>

    ![url field validation](https://user-images.githubusercontent.com/28801003/167963527-e17b7845-f478-4279-8b7f-22cbbb23119c.png)

  </details>

## Task 2 

Usually, to improve the UX, such large forms need to be broken into several small forms that are connected to each other in one flow. Create a multi-page form with the same fields and rules, but split across multiple pages.

Use two methods of navigation: [form action](https://www.w3schools.com/tags/att_form_action.asp) – to move forward and [links](https://www.w3schools.com/tags/tag_a.asp) – to move back. In this scenario is expected to throw user data from filled inputs, as [query parameters](https://en.wikipedia.org/wiki/Query_string) to next page as GET request. Pay attention to address bar on example screenshots, to see how it should work.

> NOTE: For better understanding, how form action works, I'd recommend to read about [HTTP requests](https://www.w3schools.com/tags/ref_httpmethods.asp).

### Images:

<details>
  <summary>general</summary>

  ![general](https://user-images.githubusercontent.com/28801003/167972060-5dcea9af-3a5e-42f0-8527-3d82bd9a6c29.png)

</details>

<details>
  <summary>email</summary>

  ![general](https://user-images.githubusercontent.com/28801003/167972086-82eb1156-105e-4b2a-81bd-20e85a232a8c.png)

</details>

<details>
  <summary>students</summary>

  ![general](https://user-images.githubusercontent.com/28801003/167972094-286bda38-55fb-4a61-b975-f789a1fe3ec1.png)

</details>

<details>
  <summary>students (after pressing "COMPLETE")</summary>

  ![student](https://user-images.githubusercontent.com/28801003/167972120-3de406fe-5290-43af-97b0-5cf667dcba84.png)

</details>
