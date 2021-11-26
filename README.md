# react-interview-questions

babel vs webpack-
Babel is simply a translator, who translates your 'fancy' (ES6+) JS code into 'not-so-fancy' (ES5) ones that browser (front-end) or Node.js (back-end) understands.
webpack can collect all your inline CSS styles in your Javascript files and bundle them into one.

virtual dom vs shadow dom-
virtual dom- copy of the real DOM
shadow DOM refers to the ability of the browser to include a subtree of DOM elements into the rendering of a document, but not into the main document DOM tree.

real dom vs virtual dom-
real dom-
Can directly update HTML.	
Creates a new DOM if element updates.
 virtual dom- 
Can’t directly update HTML.
Updates the JSX if element updates.

controlled vs uncontrolled componnet-
A Controlled Component is one that takes its current value through props and notifies changes through callbacks like onChange.
ny prop value of the component is either from the parent component or from the store (as in case of redux).
// Controlled:
<input type="text" value={value} onChange={handleChange} />
They do not maintain their own state.
Data is controlled by the parent component.
They take in the current values through props and then notify the changes via callbacks.

A Uncontrolled Component is one that stores its own state internally, and you query the DOM using a ref to find its current value when you need it. 
This is a bit more like traditional HTML. The component value can be taken from the state of the component depending upon the event handling.
// Uncontrolled:
<input type="text" defaultValue="foo" ref={inputRef} />
// Use `inputRef.current.value` to read the current value of <input>
They maintain their own state
Data is controlled by the DOM.
Refs are used to get their current values

React lifecycle methods?
parent to child component data send?
passing(sharing) data between componnents for communication ?
React hooks?
pure functions?
Non-pure functions, e.g., Date.now() or Math.random() ?
prop drilling (redux / context api - solution to avoid this) ?

higher order compoinent?
pure components?
error boundaries?
axios - rest apis?
redux store?
children component ?

//General way
render() {    
    return(
        <MyInput onChange={this.handleChange.bind(this) } />
    );
}
//With Arrow Function
render() {  
    return(
        <MyInput onChange={ (e) => this.handleOnChange(e) } />
    );
}

List some of the cases when you should use Refs?
Following are the cases when refs should be used:
When you need to manage focus, select text or media playback
To trigger imperative animations
Integrate with third-party DOM libraries

features of React? 
It uses the virtual DOM instead of the real DOM.
It uses server-side rendering.
It follows uni-directional data flow or data binding

What is JSX?
purpose of render() in React.
State vs props
Statefull vs stateless component

https://www.edureka.co/blog/interview-questions/react-interview-questions/
https://github.com/sudheerj/reactjs-interview-questions
https://www.ordinarycoders.com/blog/article/react-projects-github
https://reactjs.org/docs/getting-started.html    // official site

https://iq.js.org/questions/react/how-to-create-props-proxy-for-hoc-component
It is very popular nowadays because of the react framework community. In react we have a built-in server-side hydration feature. 
By using this we can easily achieve this kind of rendering. The RenderToString method helps you in that.

 <pre>
 React basic course
Fundamentals of React
Hello React
Requirements
Setting up a React Project
Meet the React Component
React JSX
Lists in React
Meet another React Component
React Component Instantiation
ReactDOM
React Component Definition (Advanced)
Handler Function in JSX
React Props
React State
Callback Handlers in JSX
Lifting State in React
React Controlled Components
Props Handling (Advanced)
React Side-Effects
React Custom Hooks (Advanced)
React Fragments
Reusable React Component
React Component Composition
Imperative React
Inline Handler in JSX
React Asynchronous Data
React Conditional Rendering
React Advanced State
React Impossible States
Data Fetching with React
Data Re-Fetching in React
Memoized Handler in React (Advanced)
Explicit Data Fetching with React
Third-Party Libraries in React
Async/Await in React (Advanced)
Forms in React
React's Legacy
React Class Components
React Class Components: State
Imperative React
Styling in React
CSS in React
CSS Modules in React
Styled Components in React
SVGs in React
React Maintenance
Performance in React (Advanced)
TypeScript in React
Unit Testing to Integration Testing
React Project Structure
Real World React (Advanced)
Sorting
Reverse Sort
Remember Last Searches
Paginated Fetch
Deploying a React Application
Build Process
Deploy to Firebase
</pre>
