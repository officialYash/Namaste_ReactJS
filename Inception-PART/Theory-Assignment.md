# `Learn React With Yash 👨‍💻 Series` 
   Documenting my learning journey of [Namaste React Live Course](https://learn.namastedev.com/) conducted by Akshay Saini
  
  ## Theory Assignment: `Chapter - 01 Inception`

  ### 1. What is Emmet ?

A: `Emmet` is the essential toolkit for web-developers. It allows you to `type shortcuts` that are then expanded into full pieces of code for writing `HTML and CSS`, based on an abbreviation structure most developers already use that expands into full-fledged HTML markup and CSS rules.

`HTML`
1. `html:5` - generates html5 boilerplate
2. `ui>li` - nested elements
3. `h1.#heading.container.con` - create h1 element with id heading and classes container and con
4. `div[data-name=Yash]` - Custom attribute <div data-name="Yash"></div>
5. `header+div+footer` - generate siblings <header></header> <div></div> <footer></footer>

`CSS`
1. `m10-10-10-10` -  Margin on all sides margin: 10px 10px 10px 10px;

### 2. Difference between library and framework ? 

A: A `library` is a collection of packages that perform specific operations whereas a `framework` contains the basic flow and architecture of an application. The major difference between them is the complexity. Libraries contain a number of methods that a developer can just call whenever they write code. React js is library and Angular is Framework.
The `framework` provides the flow of a software application and tells the developer what it needs and calls the code provided by the developer as required. If a `library` is used, the application calls the code from the library.

### 3. What is CDN ? Why do we use it ?
A CDN also called a content distribution network, is a group of geographically distributed and interconnected servers. They provide cached internet content from a network location closest to a user to speed up its delivery.
The main use of a CDN is to deliver content through a network of servers in a secure and efficient way.

### 4. Why is `React` known as React ?
`React` was developed for applications (Facebook) that have constantly changing data. Since React is a front-end framework or the `View` in MVC, this means that as the user clicks around and changes the app's data, 
the view should `react` or change with those user events.

### 5. What is cross-origin in script tag ?
The crossorigin attribute provides support for `CORS` , defining how the element handles cross-origin requests. CORS stands for Cross-Origin Resource Sharing. If cross-origin is set to "user-credential", then user authentication is required to access the file.

The purpose of crossorigin attribute is used to share the resources from one domain to another domain. Basically, it is used to handle the CORS request. It is used to handle the CORS request that checks whether it is safe to allow for sharing the resources from other domains.
### _Syntax_
```sh
<script crossorigin="anonymous|use-credentials">
```

### 6. What is difference between React and ReactDOM?
`React` library contains functionality utilised in web and mobile apps (react native). `ReactDOM` library contains functionality utilised in web browser. It contains DOM manipulation utilities.

### 7.What is the difference between react.production.js and react.development.js ?
`react.production.js` - production code of react library that is minified and production ready.
`react.development.js` - More readable and developer friendly react library code that can be used to debug.


### 8. What is async and defer?
A: `Async` - The async attribute is a `boolean attribute`. The script is downloaded in `parallel(in the background)` to parsing the page, and `executed as soon` as it is available (do not block HTML DOM construction during downloading process) and don’t wait for anything.
### _Syntax_
```sh
<script src="demo_async.js" async></script>
```

`Defer` - The defer attribute is a `boolean attribute`. The script is downloaded in `parallel(in the background)` to parsing the page, and `executed after the page` has finished parsing(when browser finished DOM construction). The `defer attribute` tells the browser `not to wait for the script`. Instead, the browser will continue to process the HTML, build DOM.
### _Syntax_
```sh
<script src="demo_defer.js" defer></script>
```