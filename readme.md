# React

## Basic

### History

- Founder: Jordan walke
- Birthdate: 2011 (Facebook's newsfeed feature)
- ReleaseYear: 2013 (V0.3.0)
- Details: Maintained by facebook and community
- Goals: Make SPA development easy and reliable, it also allows us to create reusable UI components
- Concept: A library for building user interfaces

### What is react?

An open-source library/tool for building UIs.

### React vs Angular vs Vue

- React is a library but angular/vue are framework
- React is lightweight library for building UI but angular and vue are heavyweight frameworks or complete packages
- React library is also can be called view-engine

### Why react?

- Easy to install
- Lots of compatible libraries
- It's composable
- Easy to learn
- Suitable for rich user interfaces
- Fast load speed
- Scalable and flexible
- Component-based architecture
- Hirable skill
- Maintained by skilled people

### How does react work?

React creates a VIRTUAL DOM of real DOM in memory, when data change that data-owned component will re-render.

### Add react to simple website by cdn

- react library (CDN)
- react-dom library (CDN)
- babel library (CDN)
- index.html > `<div id="root"></div>`
- `<script src="..." type="text/babel"></script>`
- `ReactDOM.render(<h1>hello world!</h1>, document.getElementById("root"))`

Exercise: Create a component and feed it in `ReactDOM.render(<Helloworld />, document.getElementById("root"))`

react use:

- babel
- webpack
- eslint

### React prerequisite

- HTML
- CSS
- JavaScript
- git and github

### JavaScript topics needed for react

- Arrow function
- Variables
- Destructuring
- Array methods
- Modules
- Spread operator
- Ternary operator

### Setup

0.Tools

    - editor: vscode - sublime text - bracket - ...
    - install node.js

1.How to test if node.js is successfully installed?

    - node -v || node --version
    - npm -v || npm --version

2.How to get react basic template?

    - method 1:

    - open terminal of vscode
    - npm uninstall -g create-react-app: to make sure install latest react library
    - npm init react-app `<project name>`
    - npm start

    - method 2:

    - npm create vite@latest
    - npm install || npm i

3.Chrome extension

    react developer tools

4.VSCode extensions

    - ES7+ React/Redux/React-Native snippets
    - indent-rainbow
    - Prettier

5.VSCode setting

    setting > search emmet > add item:javascript value:javascriptreact

### React file extensions

jsx is extension for react files that means combination of javascript and xml.
jsx also known as syntax extension to javascript.

### File and folder structures

- node_modules: a folder/container/repository for all third-party packages/modules.
- src: a folder/container/repository for all components, pages, shared, hooks, contexts, utils and ...
- index.html: react start point, output view.

### Components

- what is a component?
  a standalone, isolated and reusable parts of ui.
  in fact you can consider a web app as a collection of components.

### Component name convension

the best convension for naming a component is PascalCase format because its help react to distinguish between regular html elements and a component.

### React capablities

- Build and compose components
- High performance rendering
- Component rendering

### Basic libraries

import React from 'react';
import ReactDOM from 'react-dom/client';

### Output in react

`const root = ReactDOM.createRoot(document.getElementById("root"));`
`root.render(<App />);`

### Variables

- Can we define variable in a component?
  yes

Exercise: make use of all value-type data types in react component.

### Function

- Can we define function in a component?
  yes

Example: find random name from an array.

### Custom functional components

- Can we define custom components in react?
  yes

- what is standard of creating a custom functional component?
  every custom component should be create in components folder.

#### Challenge

- create header component
- create content component
- create footer component
- reference them all in app.js file

### Styles

#### normal css

import "./app.css";

#### css module

- vite.config.js >

`export default defineConfig({`
`plugins: [react()],`
`css: {`
`modules: {`
`localsConvention: "camelCase",`
`generateScopedName: "[local]",`
`},`
`},`
`});`

- filename format: [filename].module.css
- import [name]CSS from "./[Name].module.css";
- `<section className={`${[name]CSS.[className]}`}></section>`

#### inline css in component

const listStyle = {
listStyleType: "none",
backgroundColor: "black"
};

`<ul style={listStyle}> <li>Item 1</li> <li> Item 2 </li> <li> Item 3 </li> </ul>`

#### Use sass to component

- npm install sass
- create sass file
- reference it in the component

#### Styled components

- npm i styled-components
- components > styled > [filename].style.js
- `import styled from "styled-components"`
- `const Button = styled.alert`
  width: 100%;
  max-width: 1100px;
  margin-inline: auto;
  `;`

#### How to add css frameworks to our project

- bootstrap
- tailwind
- material ui

### folder structures

#### basic

- src >
  - tests
    - components
    - hooks
  - assets
  - components
  - hooks
- js

#### intermediate

- src >
  - assets
  - components
  - pages
  - layouts
  - hooks
  - services/contexts | redux
  - helpers/utils
- js | ts

### advance

- src >
  - assets
  - components
    - form
    - ui
  - pages
    - home | login | register | products | profile
      - test
  - layouts
  - data/constants
  - hooks
  - contexts | redux
  - services
  - helpers/utils
  - validations
- ts

### props

#### props pros

- Send multiple datatypes
- Flexible dynamic contents

#### props cons

- one-way data-binding
- props are readonly

Note:

Pure function: always returns the same output for the same args.

#### Add props from parent component to child component

`let movie = { id: 1, title: "", releaseYear: 1996, director: "", actors: [] }`

`<table> <tr> <td>ID</td> <td>{movie.id}</td> </tr> </table>`
`<table> <Row id={movie.id} title={movie.title} /> </table>`
`<table> <Row movie={movie} /> </table>`

#### Props and props drilling

- what do props help us accomplish?
  props help us to send data from parent component to child component.

- how to pass a prop to a component?
  attribute-shaped.

- Can someone pass custom prop to html element?
  no, not defined in html.

- how to receive props in a component?

Example:

`<User name="pouria nayeb" phoneNumber="09354425459" email="pour68@outlook.com" />`
`<Employee name="hamed abdeli" salary="60000" position="manager" company="nanochem" />`

### Embed jsx expressions as an attribute

import logo from "./logo.png";

`const Logo = () => <img src={logo} alt="logo of ..." />`

### Event

- event
- eventHandler
- action

#### Handling an event

Example:

- toggle
- display input data
- increase/decrease/set to zero

## Intermediate

### list

- what does the map array do?
  loop through each object and map each one to new array.

- what do we usually use map for in react?
  for map each object props on html elements.

Example:

`const names = [ "", "", "" ]`
`const users = [ {}, {}, {} ]`
`const planets = [ { name: "Earth", isGasPlanet: false }, { name: "Jupiter", isGasPlanet: true } ]`

`<ul> {names.map((name, index) => <li key={index}> {name} </li>)} </ul>`
`<> {users.map((user, index) => <User key={index} user={user} />)} </>`
`<> {planets.map((user, index) => !planet.isGasPlanet && <Planet key={index} planet={planet} />)} </>`

### Handling an event with params

- todolist + add/delete/complete ops

Tricks:

`const newArray = [...oldArray, newItem];`
`const newObject = {...oldObject, prop: newValue};`

### useState hook

- data in components that determines behavior
- enable components to manage data

import { useState } from "react";

const [data, setData] = useState([]);

- why state?

create a variable and try to manipulate it in an event, you can see manipulated data never displayed in the screen but can be logged in the console.

- state or props?
  local data for a component is called state, props is a kind of data passed from parent element to child element.

- when use state over props?
  when a component wants to have its own data.

- state or props which is immutable?
  state is mutable and props is immutable.

### Link and routing

### Life cycles

- mounting
- updating
- unmounting

### useEffect hook

import Axios from "axios";

// execute once
useEffect(() => {}, []);

// execute every-time items change
useEffect(() => {}, [items]);

// mounted and unmouted phase

useEffect(() => {
// mounted phase

    return () => {
        // unmounted phase
    };

}, []);

Note: in strict-mode mounted/unmounted execute once more for validating-code purposes.

Trick:

// only try to access age prop when person is not null
person?.age

### Add react icons library

### Conditional rendering

### Controlled components

### React router dom

import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom";

`<Router>`
`<Link to="/">Home</Link> <Link to="/Products">Products</Link> <Link to="/Contact">Contact</Link>`
`<Routes> <Route path="/" element={<Home />} /> </Routes>`
`</Router>`

### Context hook

import { createContext } from "react";

export const AppContext = createContext();

`<AppContext.Provider value={{ username, serUsername }}>`
`<Router> ... </Router>`
`</AppContext.Provider>`

import {useContext} from "react";
import {AppContext} from "../App";

`const { username, setUsername } = useContext(AppContext);`

### React query

import { QueryClient, QueryClientProvider } from "@tanstack/react-query";

// change data when tab changes
const client = new QueryClient({
defaultOptions: {
queries: {
refetchOnWindowFocus: false
}
}
});

`<QueryClientProvider client={client}>`
`<Router> ... </Router>`
`</QueryClientProvider>`

import { useQuery } from "@tanstack/react-query";

const { data, isLoading, isError, refetch } = useQuery(["cat"], () => {
return Axios.get("address").then(res => res.data);;
});

### React form

import { useForm } from "react-hook-form";
import { yupResolver } from "@hookform/resolvers/yup";
import \* as yup from "yup";

const { register, handleSubmit, formState: {errors} } = useForm({
resolver: yupResolver(schema)
});
const schema = yup.object().shape({
fullName: yup.string().required("fullname is required."),
email: yup.string().email().required(),
password: yup.string().min(6).required(),
confirmPassword: yup.string().oneOf([yup.ref("password"), null], "password don't match").required()
});

const onSubmit = () => {}

`<form onSubmit={handleSubmit(onSubmit)}>`
`<input type="text" {...register("fullname")} />`
`<span>{errors.fullName?.message}</span>`
`<input type="text" {...register("email")} />`
`<input type="text" {...register("password")} />`
`<input type="text" {...register("comfirmPassword")} />`
`</form>`

### .env variables

### Custom hooks

const useToggle = () => {
const [state, setState] = useState(false);

    const toggle = () => {
        setState(prev => !prev);
    }

    return [state, toggle];

}

const useFetch = (url, initial = []) => {
const [address] = useState(url);
const [data, setData] = useState(initial);
const [loading, setLoading] = useState(true);

    useFetch(() => {
        const data = Axios.get(address).then(res => res.data);

        setData(data);
        setLoading(false);
    }, [address]);

    return [data, loading];

}

const useCount = (initial = 0) => {
const [count, setCount] = useState(initial);

    const increase = () => {
        setCount(prev => prev + 1);
    }

    const decrease = () => {
        setCount(prev => prev - 1);
    }

    const restart = () => {
        setCount(0);
    }

    return {count, increase, decrease, restart};

}

## Advance

### useContext

- Context provider
- Context customer

```const ShoppingCartContext = React.createContext();```

```const ShoppingCartProvider = ({ children }) => {```
```const [shoppingCart, setShoppingCart] = useState([]);```

```return <ShoppingCartContext.Provider value={{ shoppingCart, setShoppingCart }}>```
```{children}```
```</ShoppingCartContext.Provider>```
```}```

```export default ShoppingCartProvider;```

### useReducer

### useMemo

### useCallback
