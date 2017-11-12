## State

```js
class Clock extends React.Component {
  constructor(props) {
    super(props);
    this.state = {date: new Date()};
  }

  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}
```

## setState

Is used to schedule updates to the component local state.

### Do Not Modify State Directly

```js
// Wrong
this.state.comment = 'Hello';
```

```js
// Correct
this.setState({comment: 'Hello'});
```

### State Updates May Be Asynchronous

```js
// Wrong
this.setState({
  counter: this.state.counter + this.props.increment,
});
```

```js
// Correct
this.setState((prevState, props) => ({
  counter: prevState.counter + props.increment
}));
```

### State Updates are Merged

When you call `setState()`, React merges the object you provide into the current state.


