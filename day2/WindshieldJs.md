# Component Rendering with WindshieldJS

## History
1. Jave + JSP
2. Node + Handlebars + hapi
  - you can compose plumbing without using the kitchen sink
  - modular
  - difficult to manage over a large contributor base
3. WindshieldJS (hapi plugin)
  - Simple contributor workflow
  - Simple teamplating
  - Good performance
  - Integrate with any data source
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
