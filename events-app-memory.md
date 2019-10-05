
## Areas to consider
- property initializer syntax
- disposal/release of resources
- use of .bind
- use PureComponent?


### Property initializer syntax (aka 'class properties')

- sets a function expression to an instance variable of a class
- class properties bind to the instance of a class, not to the prototype. Therefore, each instance has a copy of the function. This uses more memory and can be a problem for components that you render a lot of, e.b., a list item component that is rendered many times.

.babelrc for Events client

```
{
  "presets": [ "react-app"],
  "plugins": [
    "@babel/plugin-proposal-class-properties"
  ]
}
```

inline functions
- using a function like
```js
<SomeComponent onClick={() => }
```

### Use of .bind
- Some prople always bind even when using propert initializer syntax <sup>3</sup>




## References
- 1. [Demystifying Memory Usage using ES6 React Classes](https://medium.com/dailyjs/demystifying-memory-usage-using-es6-react-classes-d9d904bc4557)
- 2. [Ending the debate on inline functions in React](https://flexport.engineering/ending-the-debate-on-inline-functions-in-react-8c03fabd144)
  - use their babel transform to solve problems with using inline functions
- 3. [The constructor is dead, long live the constructor!](https://hackernoon.com/the-constructor-is-dead-long-live-the-constructor-c10871bea599)
  - good article on what babel will transform for you
- 4. [Arrow Functions in Class Properties Might Not Be As Great As We Think](https://medium.com/@charpeni/arrow-functions-in-class-properties-might-not-be-as-great-as-we-think-3b3551c440b1)
  - Babel moves class properties to the constructor



