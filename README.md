## react-interview-questions
```
Redux
Can I dispatch an action in the reducer?
can we do async call in reducer
Flux vs Redux
Thunk vs Saga
Reselect library

props vs state
controlled vs uncontrolled component
prop drilling

nextjs
Next JS is used to create web applications and performs server-side rendering, whereas React JS focuses on rendering towards the DOM. Next JS offers server-side rendering (SSR), whereas Create React App offers client-side rendering, improving the application performance. Next.
nextjs has ability to automatically code-split your application, meaning that each page only loads the necessary JavaScript for that page view. This results in faster page loads and an improved user experience.
features-
File system routing - When you add a file to the page’s directory, it is automatically available as a route. 
Server Side rendering - Next.js supports the rendering of pages on user requests on the server-side by generating a non-interactive HTML, while React uses JSON data and JavaScript instruction to make the page interactive on the client-side.
Static site generator
Image optimization - next/image component
Automatic code splitting
Type script support
API route

A stateful and stateless component
Higher-Order Components

virtual dom vs shadow dom vs real dom
In brief, the virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in memory and synced with the “real” DOM by a library
Virtual DOM	                                                       Shadow DOM
It revolves around solving performance issues.	It revolves around the concept of encapsulation.
It is a complete representation of an actual DOM.	It is not a complete representation of the entire DOM.
It groups together several changes and does a single re-render instead of many small ones.	It adds a subtree of DOM elements into the rendering of a document, instead of adding it to the main document’s DOM tree.
It creates a copy of the whole DOM object.	It creates small pieces of the DOM object having their own, isolated scope.
It does not isolate the DOM.	It isolates the DOM.
It does not help with CSS scoping.	It helps with CSS scoping.

hooks- usestate, useref, useeffect, usememo, usecontext, usereducer, useselector, usecallback
forwardRef
customhooks
```
