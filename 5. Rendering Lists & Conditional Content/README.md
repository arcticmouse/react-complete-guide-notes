## Rendering Lists of Data

Use .map() to transform the object into an array of JSX elements


## Using stateful lists

How to update the expenses array when new data is updated?

Do it in app.js, and use state

Pass a function as an argument to the set function, then return the new array with expenses & prev expenses


## Understanding "Keys"

As it is React doesn't tell the difference between different items

key prop (added to expenseItem component) can be added to any item, built into react to be interpretted as a unique ID


## Outputting conditional content

How to render different content under different conditions
1. can do ternary, long ternary is hard to read so can use the && operator as a JS trick
1. then we have two 'trick' cases so easier to read : ``{filteredExpenses.length === 0 && <p>No expenses found.</p>} ``
1. better yet, put the content into a const and have the logic in the component and not the JSX


## Adding Conditional Return Statements

Add an expenseslist component

Entire content changes so we can do the content change with different logic

Add li tag to Card item to semantically make it better


## Adding a chart

Rendering chart bar components in a chart component

Chart receives data points as props! One chart bar for each data point


## Adding Dynamic Styles

Heights for the chart bars! They should be filled depending on the value/data point they receive

Calculate the percentage and make it a string, as var barFillHeight (in chartbar.js). Style needs an object in JSX, with css properties as the name/key. If CSS name has a dash do camelCase.


## Wrapping it up...

Add a component in /expenses to hold this, and send props down


## Fixing a small bug

Force a number conversion in ExpenseForm.js


        const expenseData = {
            title: enteredTitle,
            amount: enteredAmount,
            date: new Date(enteredDate)
        };


            amount: +enteredAmount,