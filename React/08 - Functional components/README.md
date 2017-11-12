## Functional components

Stateless and without lifecycle methods.

```js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

ES6 power!

```js
const Welcome = ({ name }) => <h1>Hello, {name}</h1>
```

![Awesome](https://media.giphy.com/media/90F8aUepslB84/giphy.gif)
