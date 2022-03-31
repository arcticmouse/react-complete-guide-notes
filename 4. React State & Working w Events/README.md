## Listening to events & working with event handlers

Reacting to a button click in expenseitem.js

We have full access too all nativeDOM events

Add event listeners on the JSX element itself, as function

Can be created inline, or called by name. Former adds too much login in JSX

End triggered/attached to event listener function with 'Handler'


## How component functions are executed

To use the functions we have to call them

Using components in JSX code means React is aware of them as functions, executes all code in there, and so on recursively

It does this when the app is initially rendered. How to tell React that something has changed and needs to be re-rendered?


## Working With State

On click we want the title to change, regular variables changing DOES NOT trigger the change

We need to include a named import funciton 'useState' from react

Than, inside of component function include useState(), which is a react hook. These always begine with 'use' and must always be called inside a component function

useState wants a variable, and returns access to the special variable & a function which lets us call to assign a new value to the variable. Returned is an array with value itself and the updating function, the later when called will trigger and update

You need state to set and change values that are reflected in the UI

Now we want to call state updating function when the event (click) happens


## Closer look at 'useState' hook

useState registeres some state for the component in which it is called, for a SPECIFIC INSTANCE.

When state changes, only that specific instance of that component function's state is re-evaluated.

When we update state we do it in a function, not assigning value with the equal sign. We never see the var itself, React manages it for us.

We always get a brand new snapshot of the state when the component function re-executes. Does that mean we over ride with props? React keeps track of the first call to useState! It can detect it is not an initializing change and then give us the updated state.


## Adding Form Inputs

Add new components to our project, Current components are about showing info. 

New component will return a div with a form inside.

Then we need to gather the input values when a value changes, then on submit take the values and combine them into a new expense object.


## Listening to User Input

Get and store in the input - need to add listeners to listen for changes. Add htem on the element which gets the listener. 

The onChange just POINTS (not CALLS) to the handler.

We pass the function to React, along with the event object (default to JS)


## Working with Multiple States

We want to store the input value so that later when the form is submitted we can use the value, then combine all input values into an object when the form is submitted.

Can call useState more than once


## Using One State Instead (and what's better)

Normal to use multiple states, but can also put in the same state. Is your preference on what to do.

Using one state, make an object. Then when you update a property have to update all three otherwise it will be lost. Have to manually copy in existing values of non-updated props, and can
use spread operator to do this.

individual state slices is more common but ultimately both are ok. 


## Updating State that depends on the previous state



## Handling Form Submission

If a button, esp with type submit, is pressed the form executes a function

Add an event handler to the form to override the default browser form behavior, and in that
immediatly do event.preventDefault

Then save all the entered data in a new object expenseData to use later. For now we will just console log it.

Then clear data in input form fields when the form is submitted


## Adding Two Way Binding

How to clear the inputs?

Because we stored them in state we can implement two way binding, that listens and passes back into the input

Add value property to each input field, and then bind it to it's state var

Then after saving the submitted data in call the set* functions to set them to empty strings


## Child to parent component communication (bottom up)

We actually need to send the form data to the App.js to go into the ExpenseItem list!

Sending down can be done with props, but to do it bottom up - we can create our own event props and pass a function from parent to child, then call the funciton inside the component with data as parameter

1. Add onSaveExpenseData prop to NewExpense component, and dont add parentheses just point at the function that is being passed

2. Use that function inside ExpenseForm component now

*Trick is we pass around a pointer at a function*

We get props in ExpenseForm, so add props to the params of the component, then instead of console logging the expenseData in submitHandler, execute the passed function with expenseData as the argument

Then do the same for NewExpense -> App


## Lifting the state up