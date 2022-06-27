# Rendering an Element into the DOM (ReactDom)
Let’s say there is a < div > somewhere in your HTML file:
```html
<div id="root"></div>
```

We call this a “root” DOM node because everything inside it will be managed by React DOM.

```js
const element = <h1>Hello, world</h1>
const node = document.getElementById('root')
ReactDOM.createRoot(node);
```

# React Element
## A Simple Component

React components extends React.Component.

```js
class HelloWorld extends React.Component {
  render() {
    return (
      <div>Hello World</div>
    )
  }
}

const node = document.getElementById('root')
const root = ReactDOM.createRoot(node);
root.render(<HelloWorld />);
```

## A Simple function

A stateless component can be replace by a simple function.

```js
const HelloWorld = () => {
  return (
    <div>Hello World</div>
  );
}

const node = document.getElementById('root')
const root = ReactDOM.createRoot(node);
root.render(<HelloWorld />);
```
