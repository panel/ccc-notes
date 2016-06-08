# Component Rendering with WindshieldJS

## History

Driven by use of Angular.js on front end and need for SEO

1. Java + JSP
2. Node + Handlebars + hapi
  - you can compose plumbing without using the kitchen sink
  - modular
  - difficult to manage over a large contributor base
  - reuse is difficult with a large contributor base
3. WindshieldJS (hapi plugin)
  - Simple contributor workflow
  - Simple templating
  - Good performance
  - Integrate with any data source
  - Designed for content as a service
  - Abstractions for easily composing and swapping out services
  - Designed for component-based user experience.

## Composition

### Route
- path: ""
- context: {}
- adapters: []

### Page Object
- layout: string
- attributes: {}
- associations/zones: {}

### Adapters
- Resolve data

### Scaffolding
- Is runnable immediately

### Testing
- Mocha
- Chai
- Nock

### Takeaways
- Y not React tho?
- Components get spread over multiple files
