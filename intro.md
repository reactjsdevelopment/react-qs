<h1 align="center">React Interview Questions</h1>

> [!NOTE]  
> To add new question check [CONTRIBUTING.md](./CONTRIBUTING.md)

> [!IMPORTANT]  
> Use proper formatting.

### Table of Contents

<details open>
<summary>
Hide/Show table of contents
</summary>

| No. | Questions                                                                                                                                                                                  |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | [What is React?](#what-is-react)                                                                                                                                                           |
| 2   | [What is Redux?](#what-is-redux)                                                                                                                                                           |
| 3   | [Can I dispatch an action in the reducer?](#can-i-dispatch-an-action-in-the-reducer)                                                                                                       |
| 4   | [Can we do async calls in a reducer?](#can-we-do-async-calls-in-a-reducer)                                                                                                                 |
| 5   | [Flux vs Redux](#flux-vs-redux)                                                                                                                                                            |
| 6   | [Thunk vs Saga](#thunk-vs-saga)                                                                                                                                                            |
| 7   | [Reselect library](#reselect-library)                                                                                                                                                      |
| 8   | [Props vs State](#props-vs-state)                                                                                                                                                          |
| 9   | [Controlled vs Uncontrolled Component](#controlled-vs-uncontrolled-component)                                                                                                              |
| 10  | [Prop Drilling](#prop-drilling)                                                                                                                                                            |
| 11  | [Next.js](#nextjs)                                                                                                                                                                         |
| 12  | [A Stateful and Stateless Component](#a-stateful-and-stateless-component)                                                                                                                  |
| 13  | [Higher-Order Components](#higher-order-components)                                                                                                                                        |
| 14  | [Virtual DOM vs Shadow DOM vs Real DOM](#virtual-dom-vs-shadow-dom-vs-real-dom)                                                                                                            |
| 15  | [Hooks](#hooks)                                                                                                                                                                            |
| 16  | [forwardRef](#forwardref)                                                                                                                                                                  |
| 17  | [Custom Hooks](#custom-hooks)                                                                                                                                                              |
| 18  | [Write an HTTP service method to call N requests using Axios (GET method)](#write-an-http-service-method-to-call-n-requests-using-axios-get-method)                                        |
createPortal
</details>


---

1.  ### What is React?

    React (aka React.js or ReactJS) is an **open-source front-end JavaScript library** that is used for building composable user interfaces, especially for single-page applications. It is used for handling view layer for web and mobile apps based on components in a declarative approach.

    React was created by [Jordan Walke](https://github.com/jordwalke), a software engineer working for Facebook. React was first deployed on Facebook's News Feed in 2011 and on Instagram in 2012.

    **[⬆ Back to Top](#table-of-contents)**


1.  ### What is Redux?

    Redux is a **state management library** for JavaScript applications, often used with libraries like React or Angular. It helps manage the state of an application in a predictable way, making it easier to debug and test. Redux follows a unidirectional data flow, where the state is stored in a single immutable store, and changes are made through dispatched actions.

    **[⬆ Back to Top](#table-of-contents)**

2.  ### Can I dispatch an action in the reducer?

    No, you cannot dispatch actions inside a reducer. Reducers are pure functions that take the previous state and an action as arguments and return a new state. They should not have side effects or change the state directly; instead, actions should be dispatched outside of reducers.

    **[⬆ Back to Top](#table-of-contents)**

3.  ### Can we do async calls in a reducer?

    No, reducers should remain pure and synchronous. They should not perform side effects like making API calls. To handle asynchronous logic, middleware like Redux Thunk or Redux Saga is typically used.

    **[⬆ Back to Top](#table-of-contents)**

4.  ### Flux vs Redux

    Flux is an architectural pattern for building client-side web applications, while Redux is a specific implementation of that pattern. Redux simplifies the Flux architecture by using a single store and a more straightforward API for state management.

    **[⬆ Back to Top](#table-of-contents)**

5.  ### Thunk vs Saga

    Thunk and Saga are both middleware for handling asynchronous actions in Redux. Thunk allows you to write action creators that return a function instead of an action, enabling you to dispatch actions conditionally. Redux Saga, on the other hand, uses generator functions to handle complex side effects and is more powerful for managing complex async flows.

    **[⬆ Back to Top](#table-of-contents)**

6.  ### Reselect library

    Reselect is a library used to create memoized selectors in Redux. It helps optimize performance by preventing unnecessary re-renders by only recalculating derived data when the input state changes.

    **[⬆ Back to Top](#table-of-contents)**

7.  ### Props vs State

    Props are used to pass data from parent to child components, while state is used to manage data within a component. Props are immutable and controlled by the parent component, whereas state is mutable and managed within the component itself.

    **[⬆ Back to Top](#table-of-contents)**

8.  ### Controlled vs Uncontrolled Component

    Controlled components are form elements whose value is controlled by React state, while uncontrolled components maintain their own internal state. Controlled components are often preferred for better state management and validation.

    **[⬆ Back to Top](#table-of-contents)**

9.  ### Prop Drilling

    Prop drilling refers to the process of passing data from a parent component to a deeply nested child component through multiple layers of intermediate components. This can lead to code that is hard to maintain and understand. Context API or state management libraries like Redux can help mitigate prop drilling.

    **[⬆ Back to Top](#table-of-contents)**

10. ### Next.js

    Next.js is a React framework that enables server-side rendering, static site generation, and API routes. It simplifies the development of React applications by providing routing and performance optimizations out of the box. Current stable version is Next15.

    **[⬆ Back to Top](#table-of-contents)**

11. ### A Stateful and Stateless Component

    A stateful component manages its own state and lifecycle methods, while a stateless component (also known as a functional component) does not manage its own state and simply receives data through props. Stateful components are typically class components, though functional components can also use hooks to manage state.

    **[⬆ Back to Top](#table-of-contents)**

12. ### Higher-Order Components

    Higher-Order Components (HOCs) are functions that take a component and return a new component. They are used for reusing component logic, such as enhancing components with additional props or behavior.

    **[⬆ Back to Top](#table-of-contents)**

13. ### Virtual DOM vs Shadow DOM vs Real DOM

    The Virtual DOM is a lightweight representation of the actual DOM, used by React to optimize rendering performance. Shadow DOM is a web standard that allows for encapsulating styles and markup in a component, preventing conflicts. Real DOM is the actual representation of the UI in the browser.

    **[⬆ Back to Top](#table-of-contents)**



14. ### Hooks

    React Hooks are functions that allow you to use state and lifecycle features in functional components. Some commonly used hooks include:

  - `useState`: Manages local component state.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React, { useState } from 'react';

      const Counter = () => {
          const [count, setCount] = useState(0);

          return (
              <div>
                  <p>Count: {count}</p>
                  <button onClick={() => setCount(count + 1)}>Increment</button>
              </div>
          );
      };
      ```

      </p>
      </details>

  - `useRef`: useRef is used to create a mutable reference that persists for the full lifetime of the component. It's often used to access a DOM element directly.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React, { useRef } from 'react';

        const InputFocus = () => {
            const inputRef = useRef(null);

            const focusInput = () => {
                if (inputRef.current) {
                    inputRef.current.focus();
                }
            };

            return (
                <div>
                    <input ref={inputRef} type="text" placeholder="Click the button to focus" />
                    <button onClick={focusInput}>Focus Input</button>
                </div>
            );
        };

      ```

      </p>
      </details>

  - `useEffect`: Handles side effects like data fetching and subscriptions.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React, { useState, useEffect } from 'react';

      const DataFetcher = () => {
          const [data, setData] = useState(null);

          useEffect(() => {
              fetch('https://api.example.com/data')
                  .then(response => response.json())
                  .then(data => setData(data));
          }, []); // Empty dependency array means it runs once on mount

          return (
              <div>
                  {data ? <p>Data: {data}</p> : <p>Loading...</p>}
              </div>
          );
      };
      ```

      </p>
      </details>

  - `useMemo`: Memoizes expensive calculations.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React, { useState, useMemo } from 'react';

      const ExpensiveCalculation = ({ number }) => {
          const calculateFactorial = (num) => {
              return num <= 0 ? 1 : num * calculateFactorial(num - 1);
          };

          const factorial = useMemo(() => calculateFactorial(number), [number]);

          return <p>Factorial of {number} is {factorial}</p>;
      };
      ```

      </p>
      </details>

  - `useContext`: Consumes context values.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React, { useContext, createContext } from 'react';

      const ThemeContext = createContext('light');

      const ThemedComponent = () => {
          const theme = useContext(ThemeContext);

          return <div className={theme}>Current theme: {theme}</div>;
      };

      // Usage in App component
      const App = () => (
          <ThemeContext.Provider value="dark">
              <ThemedComponent />
          </ThemeContext.Provider>
      );
      ```

      </p>
      </details>

  - `useReducer`: Manages complex state logic, similar to Redux.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React, { useReducer } from 'react';

      const initialState = { count: 0 };

      const reducer = (state, action) => {
          switch (action.type) {
              case 'increment':
                  return { count: state.count + 1 };
              case 'decrement':
                  return { count: state.count - 1 };
              default:
                  throw new Error();
          }
      };

      const Counter = () => {
          const [state, dispatch] = useReducer(reducer, initialState);

          return (
              <div>
                  <p>Count: {state.count}</p>
                  <button onClick={() => dispatch({ type: 'increment' })}>Increment</button>
                  <button onClick={() => dispatch({ type: 'decrement' })}>Decrement</button>
              </div>
          );
      };
      ```

      </p>
      </details>

 - `useSelector`: is a hook from the React-Redux library that allows you to extract data from the Redux store state.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React from 'react';
      import { useSelector } from 'react-redux';

        const CounterDisplay = () => {
            const count = useSelector((state) => state.counter.value);

            return (
                <div>
                    <p>Count from Redux: {count}</p>
                </div>
            );
        };
      ```

      </p>
      </details>

  - `useCallback`: Memoizes functions to prevent unnecessary re-renders.
      <details><summary>Code</summary>
      <p>

      ```jsx
      import React, { useState, useCallback } from 'react';

      const Button = React.memo(({ onClick }) => {
          console.log('Button rendered');
          return <button onClick={onClick}>Click Me</button>;
      });

      const ParentComponent = () => {
          const [count, setCount] = useState(0);

          const handleClick = useCallback(() => {
              setCount(count + 1);
          }, [count]); // Only recreate the function if count changes

          return (
              <div>
                  <p>Count: {count}</p>
                  <Button onClick={handleClick} />
              </div>
          );
      };

      const UserDetails = ({user, onEdit}) =>{

    const {title, full_name, profile_img} = user;

    return (

        <div className="user-detail-wrapper">

            <img src={profile_img} />

            <h4>{full_name}</h4>

            <p>{title}</p>

        </div>

    )

}

export default React.memo(UserDetails)
      ```

    </p>
    </details>


    **[⬆ Back to Top](#table-of-contents)**

15. ### forwardRef

    `forwardRef` is a React function that allows you to pass a ref through a component to one of its children, enabling parent components to directly interact with the child’s DOM node.

    **[⬆ Back to Top](#table-of-contents)**

16. ### Custom Hooks

    Custom hooks are functions that allow you to extract and reuse stateful logic across multiple components. They can use built-in hooks and can be shared easily among different components.

    ```jsx
    import { useState } from 'react';

    // Custom hook
    const useCounter = (initialValue = 0) => {
        const [count, setCount] = useState(initialValue);

        const increment = () => setCount(count + 1);
        const decrement = () => setCount(count - 1);
        const reset = () => setCount(initialValue);

        return { count, increment, decrement, reset };
    };

    // Component using the custom hook
    const Counter = () => {
        const { count, increment, decrement, reset } = useCounter(0);

        return (
            <div>
                <p>Count: {count}</p>
                <button onClick={increment}>Increment</button>
                <button onClick={decrement}>Decrement</button>
                <button onClick={reset}>Reset</button>
            </div>
        );
    };

    export default Counter;
    ```

    **[⬆ Back to Top](#table-of-contents)**

17. ### Write an HTTP service method to call N requests using Axios (GET method)

    We can create a function that uses `Promise.all` to handle multiple Axios GET requests simultaneously.
    > example:

    ```javascript
    import axios from 'axios';

    const fetchMultipleRequests = async (urls) => {
        try {
            const requests = urls.map(url => axios.get(url));
            const responses = await Promise.all(requests);
            return responses.map(response => response.data);
        } catch (error) {
            console.error('Error fetching data', error);
            throw error;
        }
    };
    ```

    **[⬆ Back to Top](#table-of-contents)**

---

Given a plain React component with no lifecycle customizations,
when does render get called?
Select the best option:
A. When this.setState is called
B. When the component's parent is re-rendered
C. When the component's props changes
D.
A and B
E. All of the above
