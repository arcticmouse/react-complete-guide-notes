## Components
Individual reusable with seperated concerns building blocks composed together into an interface

Smaller pieces = easier to maintain

Reusable: dont repeat yourself

Seperation of concerns: dont do too many things in one and the same place(function)

Just a JS function!


## React Code Written In A Declarative Way

Define the desired target state and under which conditions it should be reused & React determines which elements actual JS DOM updates


## CODE LINKS

use node@16, via symlink

[ON GITHUB](https://github.com/academind/react-complete-guide-code/tree/03-react-basics-working-with-components/code)


## 01 project

index.js first file to execute
- imports reactDOM feature from react
- render method takes 2 parameters, 
    - APP component, imported from the app.js file
    - the html DOM element APP will be loaded into
    - HTML is in /public


APP component imported
- just a function
- returns HTML code in a JS file
    - this is actually JSX


## JSX

HTML code inside JX

stands for JS XML


## How React Works

Define desired end state in the return, React generates it behind the scenes


## Building First Custom Component

Put new components into own file

App will be the root component. Other components will be nested in App or in other components.

We want to build a component tree!

App is rendered, and the others will be imported via App

### ExpenseItem.js

Common convention is to camel case component file names & use for the function to be exported name. 

File name tells us what type of logic lives inside of file.

Export default ExpenseItem bc it is the only item being exported from this file.

Import it into App.js, and use in a tag with an upper case character.

Lower case elements = built in elements

Upper case elements = defined by a developer element


## More complex JSX code

in ExpenseItem.js

Only 1 root element allowed per a return!

A simple work around to wrapping it in an opening and closing div. Can wrap in brackets to signify it is one statement.


## Adding Basic Styling

CSS for the component has same name and is same place as the component file, and import into the component file


## Outputting Dynamic Data & Working w Expressions in JSX

can create variables in the funciton like normal JS. 

include in jsx between curly braces; 

can also include JS functions.


## Passing Data via 'props'

can just c/p <ExpenseItem></ExpenseItem> in app.js :p

also use parameters and 'props'

set properties (props) of our own custom components

we have expenseDate, etc. these should be in App. and App passes the data to ExpenseItem as parameters

The parameters is an object received with all parameters as **properties** aka **props**, in k-v pairs


## Adding normal JS logic to components

Props can be logic stuff too... for instance our date is pretty ugly

Better practice and cleaner code to not have this in the JSX, but in variables/const


## Splitting Components into Multiple Components

Split app into smaller building blocks where each component is focused on one core task.

Each component is small and managable

There is no hard rule, but bc we have helper constants in the expense item with date so will split out the date component