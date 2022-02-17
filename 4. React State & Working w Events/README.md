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


