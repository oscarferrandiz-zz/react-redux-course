## Higher-Order Components

A higher-order component (HOC) is an advanced technique in React for reusing component logic. HOCs are not part of the React API, per se. They are a pattern that emerges from React’s compositional nature.

```js
const EnhancedComponent = higherOrderComponent(WrappedComponent);
```

## Don’t Mutate the Original Component. Use Composition.

```js

import MyComponent from './MyComponent';
import Spinner from './Spinner';

const withSpinner = (Component) => {
  return class Loader extends Component { 
    render() {
      const { loading, ...restProps } = this.props;
      return (
        <div>
          {loading ? <Spinner /> : <Component {...restProps} />}          
        </div>
      );
    }
  }
};

export default withSpinner(MyComponent)
```
 
