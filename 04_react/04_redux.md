# Redux

## Research
1. Read "getting started" documentation of [redux](https://redux.js.org/introduction/getting-started)

## Level 1

1. Create `<Modal />` component or install and use any package (for example: `react-modal`)
2. Move input component with all related logic inside `<Modal />`
3. Update your logic of creating/updating todo list items, to use redux store instead of react state. After this update you shouldn't have any props, that trows handler functions and todo items between components. Instead all data should be taken from redux store, and all data changing handlers should be changed to redux actions.

## Level 2

1. Add [redux-persist](https://github.com/rt2zz/redux-persist) to project and use it to save store to `localStorage`.
