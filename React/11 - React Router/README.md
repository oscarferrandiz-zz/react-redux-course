### React-router

[React router doc](https://reacttraining.com/react-router/)

```js
import React from 'react';
import { Switch, Route } from 'react-router-dom';

// Pages
import ArtistsPage from '@/pages/ArtistsPage';
import ArtistPage from '@/pages/ArtistPage';
import AlbumPage from '@/pages/AlbumPage';

const Main = () => (
  <main>
    <Switch>
      <Route exact path="/" component={ArtistsPage} />
      <Route path="/artists/:artistId" exact component={ArtistPage} />
      <Route path="/artists/genre/:genre" exact component={ArtistsPage} />
      <Route path="/albums/:albumId" component={AlbumPage} />
    </Switch>
  </main>
);

export default Main;
```
