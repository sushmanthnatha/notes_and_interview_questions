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
