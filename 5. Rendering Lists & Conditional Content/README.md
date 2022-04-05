## Rendering Lists of Data

Use .map() to transform the object into an array of JSX elements


## Using stateful lists

How to update the expenses array when new data is updated?

Do it in app.js, and use state

Pass a function as an argument to the set function, then return the new array with expenses & prev expenses


## Understanding "Keys"

As it is React doesn't tell the difference between different items

key prop (added to expenseItem component) can be added to any item, built into react to be interpretted as a unique ID

