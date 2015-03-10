# flux-react-introduction
Presentation on Flux and React.js for Code Camp 2015

Notes
-----

React
- fast
- testable
- simple

Why I love React
- Put the smarts back in the developer
- Testable without mocking everything
- Give the power back to the people
- Uses Imutable patterns from functional programming
- Data changing over time is the root of all evil

http://tutorialzine.com/2014/07/5-practical-examples-for-learning-facebooks-react-framework/


Nested components inside of other components

You are creating a UI as a tree of functions.

## Flex/React terms
- component
- reconciliation
- JSX
- props
- state
- action
- immutable
- store
- key
- mixins
- dispatcher
- render
- callback

## web terms
- router
- 


### Building with React

1. Start with the UI design
1. Create your components tree

### React Speed

[reconciliation](http://facebook.github.io/react/docs/reconciliation.html)

react pure mixin

### Virtual DOM (and event system)

On every update...
- React builds a new virtual DOM subtree
- ...diffs it with the old one
- ...computes the minimal set of DOM mutations and puts them in a queue
- ...and batch executes all updates

### JSX
- not a templete engine
- compiles directly to js
- think coffee
- dsl around html with the ability to js

### State
``getInitalState``
``setState``
Application State vs Component State
reconciliation

#### Component State
* timers
* dropdowns
* list subseting

#### Application State

* component
* action

An action is fired by a component

"Flux could be called a bunch of callbacks with some orginazation with a subscription pattern" - Colin Megill - Learn React, Flux and Flow Part 1

## Events

http://facebook.github.io/react/docs/events.html

* How is bubbling handled?


## Misc

### Flux

#### Implementations
* alt
* Barracks
* Delorean
* Fluxify
* Flux
* Fluxxor
* Fluxy
* Fynx
* marty.js
* McFly
* Reflux

Riot application?

## Routing

* react-router
* react-router-component
* director


## Components

We strongly believe that components are the right way to separate concerns rather than "templates" and "display logic."

keep as many of your components as possible stateless

compute any other information you need based on this state

React.PropTypes exports a range of validators that can be used to make sure the data you receive is valid.

`mixin` are used for removing duplication in cross-cutting-concerns

### Reconciliation

data flows from owner to owned component through props

### render()

required and must be `pure`

### getInitialState()

### getDefaultProps()

### propTypes()

### mixins()

### statics()

### displayName()


## Imutability

`Update`

Helper functions

```javascript
var initialArray = [1, 2, 3];
var newArray = update(initialArray, {$push: [4]}); // => [1, 2, 3, 4]
```

initialArray is still [1, 2, 3].

[Immutable-js](https://github.com/facebook/immutable-js)


## Take aways

- Components not templates
- Re-render don't mutate
- Virtual DOM is simple and fast

## Best pratices

- Use PureRenderMixin
- Use PropTypes
- Avoid State
- Centralize State
- Do more in render()
- Use mixins
- Ok to use instant properties for events (not render)
- Think in Elements

http://aeflash.com/2015-02/react-tips-and-best-practices.html



