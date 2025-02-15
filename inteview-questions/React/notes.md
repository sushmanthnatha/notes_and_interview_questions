# React

from index.html, main.js and main.css will be called,
analyze the bundle
search for alternate libraries/import partial libraries


#### What is code splitting
We can split that code into chunks and only load the chunk needed for the initial page load; the rest are loaded on a need basis. This doesn't reduce the size of your application but divides the React bundle size into chunks which can be lazy loaded as we need them.
It can be configured through webpack or can be done through React.lazy()
Webpack does it through: vendor splitting (node-modules), common module splitting, size based splitting



### what is Reconciliation

Reconciliation is the process React uses to efficiently update the UI when the state or props of a component change.Instead of re-rendering the entire UI, React calculates the difference (diffing) between the old and new virtual DOM and updates only what’s necessary.

#### What is CacheBusting

#### What is Treeshaking
Tree shaking is a term commonly used within a JavaScript context to describe the removal of dead code(unused code/import).

In modern JavaScript applications, we use module bundlers (e.g., webpack or Rollup) to automatically remove dead code when bundling multiple JavaScript files into single files. This is important for preparing code that is production ready, for example with clean structures and minimal file size.

#### What is Minification
Minification is a process in which the bundlers try to minimize the code further by removing Whitespaces, and comments, or shortening the long variable names into smaller names. It can be done using Terser Plugin

#### What is compression
Compression is a technique that is used mostly by servers to compress the assets before serving them over to the network. This makes a whole lot of difference ass such as 70% of your React bundle size can be optimized using this method if your server already not doing them.Widely accepted Algorithms are Gzip, Brotli, and Deflate. Where Gzip is accepted by all browsers 

nowadays. Used for 
✔️ Reducing API response size (JSON, HTML, etc.)
✔️ Minimizing assets (CSS, JS, images)
✔️ Optimizing web performance


Compression Type	Usage
Gzip/Brotli	Compress API responses
JSON Compression	Reduce API payloads
Webpack/Terser	Minify JS & CSS
Sharp/TinyPNG	Optimize images

```
const app = express();

// Enable Gzip compression
app.use(compression());
```


#### What is reconcilation


𝗘𝗿𝗿𝗼𝗿 𝗛𝗮𝗻𝗱𝗹𝗶𝗻𝗴 & 𝗟𝗶𝗳𝗲𝗰𝘆𝗰𝗹𝗲 𝗠𝗲𝘁𝗵𝗼𝗱𝘀
• Can you describe the `componentDidCatch` lifecycle method? 
• In which scenarios do error boundaries not catch errors? 
• What is the behavior of uncaught errors in React 16? 
• What is the proper placement for error boundaries? 
• What is the benefit of component stack trace from an error boundary? 

𝗥𝗲𝗮𝗰𝘁 𝗙𝘂𝗻𝗱𝗮𝗺𝗲𝗻𝘁𝗮𝗹𝘀 & 𝗕𝗲𝘀𝘁 𝗣𝗿𝗮𝗰𝘁𝗶𝗰𝗲𝘀
• What are default props? 
• What is the purpose of the `displayName` class property? 
• What is the browser support for React applications? 
• Does React support all HTML attributes? 
• When do component props default to true? 

𝗣𝗲𝗿𝗳𝗼𝗿𝗺𝗮𝗻𝗰𝗲 & 𝗢𝗽𝘁𝗶𝗺𝗶𝘇𝗮𝘁𝗶𝗼𝗻 
• What is code-splitting? 
• What are Keyed Fragments? 
• What is dynamic import? 
• What are loadable components? 
• What is the Suspense component? 
• What is route-based code splitting? 

𝗘𝘃𝗲𝗻𝘁 𝗛𝗮𝗻𝗱𝗹𝗶𝗻𝗴 & 𝗖𝗼𝗺𝗽𝗼𝗻𝗲𝗻𝘁 𝗕𝗲𝗵𝗮𝘃𝗶𝗼𝗿
• What is Next.js, and what are its major features? 
• How do you pass an event handler to a component? 
• How do you prevent a function from being called multiple times? 
• How does JSX prevent injection attacks? 
• How do you update rendered elements? 
• How do you ensure that props are read-only? 

𝗞𝗲𝘆𝘀, 𝗥𝗲𝗳𝘀 & 𝗦𝘁𝗮𝘁𝗲 𝗠𝗮𝗻𝗮𝗴𝗲𝗺𝗲𝗻𝘁
• What are the conditions to safely use index as a key? 
• Should keys be globally unique? 
• What is the most popular choice for form handling? 
• What are the advantages of Formik over Redux Form? 
• Why is inheritance not required in React? 
• When do you need to use refs? 

𝗔𝗱𝘃𝗮𝗻𝗰𝗲𝗱 𝗥𝗲𝗮𝗰𝘁 𝗖𝗼𝗻𝗰𝗲𝗽𝘁𝘀
• Can you use Web Components in a React application? 
• What is the purpose of the default value in Context? 
• What is the diffing algorithm? 
• What are the rules covered by the diffing algorithm? 

𝗥𝗲𝗻𝗱𝗲𝗿 𝗣𝗿𝗼𝗽𝘀, 𝗪𝗶𝗻𝗱𝗼𝘄𝗶𝗻𝗴 & 𝗝𝗦𝗫 𝗕𝗲𝗵𝗮𝘃𝗶𝗼𝗿
• Does a prop need to be named render for render props? 
• What are the problems of using render props with pure components? 
• What is the windowing technique? 
• How do you print falsy values in JSX? 

These questions cover key areas of React, including performance optimization, component lifecycle, state management, and best practices. 
