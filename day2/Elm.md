# Elm

## Goals
- immutable data
- stateless
- good coverage of webplatform in standard lib (websockets, virtual dom)

## Language Considerations
- hard to test:
  - mutable data
  - side effects
  - implicit state
- unmaintainable:
  - untyped data
  - unpredictable code and file structure
  - unmanaged interactions
- unreliable
  - `null`
  - errors
  - Type Errors
  - package managers
- You have to buy into language creator's decisions about a lot of things
- Elm's package manager handles versioning

## Language
- Auto-currying :curry:
- Custom types
- `Maybe`, `Never`, `Just` types

## Compiler
- Super easy tree shaking as all functions, variables, etc are namespaced within the global JS scope, allowing minifiers to clean up unused identifiers easily.
- Great developer experience as it auto suggests fixes for compile errors (uses Levenshtein distance)

## Takeaways
- Trades easy comprehension for purity and explicit flow control
- Hard to live-code even a simple example
