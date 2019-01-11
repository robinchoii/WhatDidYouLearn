#Setting up React Router

>create-react-app
>npm install react-router-dom --save
>npm install
>npm start
>go to localhost:3000

##App.js
>import { BrowserRouter, Route } from 'react-router-dom';
- BrowserRouter can only have 1 child
- Route takes a path and component
    - if no path, handle error component
- Switch allows only the component pointing to the route to load instead of multiple components
```javascript
<BrowserRouter>
    <div>
        <Route path='/' component={Home} exact}/>
        <Route path='/about' component={About} exact}/>
        <Route path='/contact' component={Contact} exact}/>
        <Route component={Error} exact}/>
    </div>
</BrowserRouter>
```

###Create folder called components inside 'src'
add files - Home, About, Contact

