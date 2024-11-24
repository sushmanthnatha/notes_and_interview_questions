# React

#### Fast Refresh
Fast refresh is a React feature integrated into Next.js that allows you live reload the browser page while maintaining temporary client-side state when you save changes to a file. It's enabled by default in all Next.js applications on 9.4 or newer. With Fast Refresh enabled, most edits should be visible within a second

In general, Fast Refresh works with React 16.10 or later.

### What is json-server?
json-server is a simple, lightweight tool that allows you to create a fake REST API quickly. It's ideal for prototyping, mock data, or testing front-end applications without needing a full backend.

With json-server, you can:

Create a RESTful API from a JSON file.
Perform CRUD (Create, Read, Update, Delete) operations.
Use query parameters to filter, sort, and paginate data.

``` bash
json-server --watch db.json --port 5000
```