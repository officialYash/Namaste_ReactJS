# `Learn React With Yash 👨‍💻 Series` 
   Documenting my learning journey of [Namaste React Live Course](https://learn.namastedev.com/) conducted by Akshay Saini
  
  ## Theory Assignment: `Chapter - 03 Laying the Foundation`

  ### 1. What is `JSX`?
`JSX` is neither a string nor a html tag but a syntactic sugar for the React object. It is a `html-like syntax` inside `js` code for creating react elements. By using JSX, instead of writting markup (html) and logic(js) separately, the separation of concerns (SoC) is emphasized based on loosely coupled units called 'Components' which contains both. JSX stands for JavaScript XML. JSX allows us to write HTML elements in JavaScript and place them in the DOM without any createElement() and/or appendChild() methods. JSX makes it easier to write and add HTML in React. 

Broswer does not understand JSX and a transpiler/compiler is required to convert this to browser understandable js code. Eg: Babel

JSX ------> React.createElement() -----> React element ----> Object to be rendered in the DOM

### Example 1 using JSX:
```
const myElement = <h1>I Love JSX!</h1>;
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```
### Example 2 Without JSX:
```
const myElement = React.createElement('h1', {}, 'I do not use JSX!');
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myElement);
```


### 2. Superpowers of JSX 

- JSX as `variables` : markup (html-like) syntax can be set in a variable. This creates a react element (object).

- `javascript expressions` in JSX : JSX supports all js expressions by wrapping them in {} 

- `Attributes` in JSX : We can pass all the html attributes inside jsx tag (attributes must be CamelCased). Even, custom attributes can be created, but it must not use CamelCase. 

- `Props` in JSX : The values of each attribute can be passed as properties (props) to a react element. This is my favourite superpower of jsx, since it can handle dynamic data to create react elements.

Using JSX, you can write markup inside Javascript, providing you with a superpower to write logic and markup of a component inside a single .jsx file. JSX is easy to maintain and debug.

### Example
```
function greeting(user) {
//JSX
  return <h1>{user}, How are you!!!</h1>;
}
```


### 3. Role of type attribute in script tag ? What options can I use there ?

`type` attribute of the <script> tag indicates the type of script. Until HTML 4,  type is a required attribute. The value of type can be any of the following : 

```
<script type="" src="app.js"></script>
```
In HTML5, type attribute is not mandatory. If type attribute is not present(default), or an empty string (type="") or javascript MIME type (text/javascript or application/ecmascript), it is treated as classic "javascript" file.

```
<script type="module" src="app.js"></script>
```
If the type attribute is set `module`, then the code in that js file is treated as module.

```
<script type="importmap" src="app.js"></script>
```
If the type attribute is set `importmap`, the body of the element contains importmap ie an JSON object using which the browser can resolve the module specifiers while importing modules.

```
<script type="{$anyothervalue}" src="app.js"></script>
```
  
If the type attribute contains anyother value, then the code is treated as data block and will not be processed by the browser. A valid MIME type other than Javascript MIME type (Eg: image/png or text/css) must be mentioned. All the other attributes for this type will be ignored even the `src` attribute.

### 4. `{ TitleComponent }` vs `{ <TitleComponent /> }` vs `{ <TitleComponent> </TitleComponent> }` in JSX    
The Difference is stated below:
- `{TitleComponent}`: This value describes the `TitleComponent` as a javascript expression or a variable. 
The `{}` can embed a javascript expression or a variable inside it.
- `<TitleComponent/>` : This value represents a Component that is basically returning Some JSX value. In simple terms `TitleComponent` a function that is returning a JSX value.
A component is written inside the `{<  />}` expression.
- `<TitleComponent></TitleComponent>` :  `<TitleComponent />` and `<TitleComponent></TitleComponent>` are equivalent only when `< TitleComponent />` has no child components. The opening and closing tags are created to include the child components.
### Example
```
<TitleComponent>
    <FirstChildComponent />
    <SecondChildComponent />
    <ThirdChildComponent />
</TitleComponent>
```