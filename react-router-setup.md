# Setting up React Router

> create-react-app
> npm install react-router-dom --save
> npm install
> npm start
> go to localhost:3000

## App.js
>import { BrowserRouter, Route } from 'react-router-dom';
- BrowserRouter can only have 1 child
- Route takes a path and component
    - if no path, handle error component
- Switch allows only the component pointing to the route to load instead of multiple components

Renders Home and Error @ localhost:3000
```javascript
<BrowserRouter>
    <div>
        <Route path='/' component={Home} exact />
        <Route path='/about' component={About} />
        <Route path='/contact' component={Contact} />
        <Route component={Error} />
    </div>
</BrowserRouter>
```
vs

Renders only Home @ localhost:3000
Renders only About @ localhost:3000/about
```javascript
<BrowserRouter>
    <Switch>
        <Route path='/' component={Home} exact />
        <Route path='/about' component={About} />
        <Route path='/contact' component={Contact} />
        <Route component={Error} />
    </Switch>
</BrowserRouter>
```


### Create folder called components inside 'src'
add files - Home, About, Contact, Navigation

## Navigation.js
```javascript
import React from 'react';
import { NavLink } from 'react-router-dom';

const Navigation = () => {
    return (
        <div>
            <NavLink to="/">Home</NavLink>
            <NavLink to="/about">About</NavLink>
            <NavLink to="/contact">Contact</NavLink>
        </div>
    )
};

export default Navigation;

```


