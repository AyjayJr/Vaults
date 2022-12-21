## How React works

In the index.html there is a div by the id 'root'.  In the index.js file we use ReactDOM to find that root element. Then we use that root to render our React components. The components are defined by js functions that return special JSX elements. This is then exported and is what is rendered in the index.js and displayed on the html file at run time.

## Component work and styling

Although JSX looks similar to HTML when adding classes you use className instead of class. This is because JSX uses vanilla javascript syntax. This is one of the few times when the property name in HTML is different from the attribute name in JS.