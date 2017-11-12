## Fetching remote data

```js
import React, { Component } from 'react';
import axios from 'axios';

export default class MyComponent extends Component {

  constructor(props) {
    super(props);
    this.state = {
      posts: [],
      error: null
    };
  }
  
  componentDidMount() {
    axios.get('http:remote-api-url.com/posts')
      .then((response) => {
        this.setState({ posts: response.data });
      })
      .error((error) => {
        this.setState({ error: error.message });
      }):
  }

  ...
```

With Es6 power!

```js
async componentDidMount() {
  try {
    const response = await axios.get('http:remote-api-url.com/posts');
    this.setState({ posts: response.data });
  } catch (error) {
    this.setState({ error: error.message });
  }
}
```
