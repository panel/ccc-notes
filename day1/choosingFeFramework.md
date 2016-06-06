# Choosing between AngularJS, EmberJS and ReactJS+Redux

## Basic Comparison
- Angular, Ember use HTML and injects JS into the HTML
- React defines the template in the JS and is parsed there
  - Allows for easier debugging as template errors are in JS
  - Can use HTML if desired

## Engineering Criteria for Front End Development
### Checking Data Changes, View Updates
  - ng: dirty checking, key value tree diff. digest cycle
  - ng2: same basically as ng
  - ember:
    - Knockout style.
    - Done through inheretence with listeners/observables.
    - Pub/sub - ish.
  - React:
    - Model is pure JS. Only publish state object
    - Uses virtual DOM
    - Creates a diff between VDOM and real DOM and generates a patch
    - Applies the diff to the real DOM.
### DOM Tree Diffing
### 1 and 2 way data bindings
  - ng and Ember us 2 way binding.
  - React uses 1 way.
  - ng2 and modern Ember offer 1 way data binding.
  - In React, the DOM cannot affect changes in a model. It can only raise events that state can change.
    - done by default in ng.
    - 2 way can be more difficult to reason about
    - limits entry points to state mutation
### Views & Templates
  - ng: HTML
  - ember: HTML/handlebars.js
  - React: JSX (pure js)
### Testing
  - All the same, basically.
### Routing
  - Ember router is the best
  - ng
    - built in router which is OK
    - solid 3rd party angular-ui-router
  - React: 3rd party router based on ember's
### Tooling
  - Ember has rails like Ember CLI
  - ng and react have 3rd party generators
  - ng2 working with ember on developing cli
### Components
  - ng: directives
  - everything else calls 'em components
### Client Side ORM
  - Ember has ember data to abstract REST as ORM
  - ng2 will have the same thing as well
### Native app
  - React Native will compile down to native apps
  - NativeScript and React Native bypasses web view. hooks directly into the natvie UI
  - ng is working w/ Telerik on NativeScript
  - ember is ????
### Convention vs. Config
  - Ember:
    - Everything must have a route. Routes connects Everything
  - ng:
    - MV*
  - react:
    - Flux based architecture.
    - Everything is a component
    - Any state change must start with an Action, get handled by a Dispatcher to modify a Store

## Comparisons
  - ng, ng2, ember and react all support the industry standard paradigms
  - The main criteria are non-technical: past experience, institutional knowledge.

## Conclusion
