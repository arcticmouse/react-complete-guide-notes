## Exports & Imports (Modules)

### 'default exports', only one

const person = {
    name: 'Max
}

export default person


import person from './person.js'

### two different exports with alias so 'named exports'

export const clean = () => {...}
export const baseData = 10;


import { baseData } from './utility.js'
import { clean } from './utility.js'

---or---

import * as bundled form './utility.js'

then... bundled.baseData, bundled.clean, refer to as JS object


## Classes, Properties & Methods

Properties like "variables attached to classes/objects"

Methods like "functions attached to classes/objects"


## Spread & Rest operators

Same syntax `...`

### Spread 
split up array element OR object properties

### Rest
merge a list of function arguments into an array


## Destructuring
Easily extract single array elements or object properties and store them in variables

### Array
[a, b] = ['Hello', 'Max']

console.log(a) // Hello

console.log(b) // Max


### Object
{name} = {name: 'Max', age:28}

console.log(name) // Max

console.log(age) // undefined


## Reference and Primitive Types
Objects and arrays are reference types. If you reassign, you copy the pointer not the value.