## How React works

In the index.html there is a div by the id 'root'.  In the index.js file we use ReactDOM to find that root element. Then we use that root to render our React components. The components are defined by js functions that return special JSX elements. This is then exported and is what is rendered in the index.js and displayed on the html file at run time.

## Component work and styling

Although JSX looks similar to HTML when adding classes you use className instead of class. This is because JSX uses vanilla javascript syntax. This is one of the few times when the property name in HTML is different from the attribute name in JS.

## Passing data thru 'props'

In any functional component you can accept an argument usually named props.
- Props is a js object
- Contains key value pairs of data
- The key corresponds to the attribute name in jsx
- The value corresponds to the attributes value given

Dynamic expressions are denoted by '{ }'
- This tells React to evaluate the javascript within the brackets
- You can have any js expression within the brackets
- You cannot have any block statements

Use '{ }' to evaluate the attribute values stored in props e.g. { props.text }

---
## Handling Events

### Reminder

Important to remember that all the jsx elements are just react components that come built in. Not to be confused with html elements.

This matters because you can add certain attributes that you could not add with just html.

### onClick()

You can add an 'onClick' prop to any jsx element.
onClick takes a function that will be executed on click.

You can add an anonymous inline function e.g. function () {...}
Or an arrow function e.g. () => {...}
Or you point to another function.

Usually you would want to point to another function that is nested within the functional component.

When pointing to a named function remember note to use parans e.g. onClick={deleteHandler}

This is because the function would execute too early if you put the parantheses

---
## States

Import { useState } from 'react';
- useState is a react hook
- calling useState creates a state that react is aware of.
- it returns an array of two values the state and a method to set that state
	- e.g. [ state, setState ] = useState(false);

After creating a state, you can dynamically render certain components depending on what state you are in e.g. { modalIsOpen && <Modal/> }

---
## Event Props

you can pass functions as props as well.

This is useful because our own custom components don't have any event handlers built in such as onClick.

---
## Routing