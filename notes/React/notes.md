# React

#### Fast Refresh
Fast refresh is a React feature integrated into Next.js that allows you live reload the browser page while maintaining temporary client-side state when you save changes to a file. It's enabled by default in all Next.js applications on 9.4 or newer. With Fast Refresh enabled, most edits should be visible within a second

In general, Fast Refresh works with React 16.10 or later.

#### What is json-server?
json-server is a simple, lightweight tool that allows you to create a fake REST API quickly. It's ideal for prototyping, mock data, or testing front-end applications without needing a full backend.

With json-server, you can:

Create a RESTful API from a JSON file.
Perform CRUD (Create, Read, Update, Delete) operations.
Use query parameters to filter, sort, and paginate data.

``` bash
json-server --watch db.json --port 5000
```

#### prop-types
Its a JS library to validate the porps that get passed into your component
If someone passes down the incorrect kind of value ( number instead of boolean), a warning will appear in console
Used to be very popular. Now typescript does almost the samething

#### To install tailwaind in create-react-app project

```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

## Hooks
![useEffect](./images/useEffect.png)

![useEffect2](./images/useEffect2.png)

useEffect shouldn't return anything except a function (which is used for cleanup)

![useEffectreturnfunc](./images/useEffect-return-func.png)

```js
// clearing eventlistener through useEffect

import { useState, useEffect } from "react";

function App() {
  const [counter, setCounter] = useState(0);

  useEffect(() => {
    function listener() {
      console.log(counter);
    }
    document.body.addEventListener("click", listener);

    return () => {
      document.body.removeEventListener("click", listener);
    };


  }, [counter]);

  return (
    <div>
      <button onClick={() => setCounter(counter + 1)}>+ Increment</button>
      <div>Count: {counter}</div>
    </div>
  );
}

export default App;

```

#### UseCallback

- Its a hook to help you tell React that your function isn't actually changing over time
- Fixes bugs around useEffect and other similar situations
- Follows similar conventions as useEffect

![useEffect eslint callback](./images/useEffect_elist_callback.png)

##### why is app making endless stream of requests ?
Everytime we fetch data, we udate state. When we re-render a new versio of ```fetchImages``` is created. The ```useEffect``` function runs again because it sees an element in its dependncy array has changed.

useCallback hook can be used to stop here, wrap fetch function in useCallback to fix this useCallback(fetchImages,[]) and then use it to call instead of fetchImages

#### Componen vs page in react
A component is a resuasble react comonent that show s a handlful of elements
A Page is still a react component. Not intended to be reused


### Design System process
There are a total of 8 steps involved in this
![Design process](./images/design_system_process.png)

#### Functional way of updating state
![functionanl_state_update](./images/functionanl_state_update.png)

### Event capturing & bubbling

In web development, event capture and event bubbling are two phases of how events propagate through the DOM (Document Object Model). These concepts are part of the event flow mechanism, which describes how events travel through the DOM hierarchy when a user interacts with an element.

#### Event Flow Phases
##### Event Capturing Phase
Also called the "trickling phase".
Events propagate from the root element down to the target element.
In this phase, parent elements get a chance to handle the event before the target element is reached.
##### Target Phase
The event reaches the target element.
If an event listener is attached to the target element, it will be executed during this phase.
##### Event Bubbling Phase
Events propagate from the target element up to the root element.
In this phase, parent elements get a chance to handle the event after the target element has processed it.

![event_capturing_bubbling](./images/event_capturing_bubbling.jpg)

### useRef
Allows a component to get a reference to a DOM element that it creates
Mostly it holds ref to DOM elements, but can also hold a value

- creates a ref to component by calling useRef, 
- assign ref to a JSX element as a prop called ref
- access that DOM element with ref.current


#### Standard browser behaviour
When the browser loads a new HTML doc, all existing JS variables and code is dumped


### Naviagation in React

![navigation_in_react](./images/navigation_in_react.png)


window.location = xxxx 
The above causes a full page refresh

window.history.pushState({}, '','/dropdown')
Updates the address bar but doesn't cause a refresh


window emits a 'popstate' event if the user current url was added by 'pushState'

### Navigation Libraries

- React Router
- Wouter
- Reach-location
- Reach-Router


#### useReducer

![useReducer](./images/useReducer.png)