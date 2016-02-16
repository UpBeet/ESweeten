# `diabeetES`

A modular (but opinionated) macro based extension of the JavaScript runtime 

## Motivation

ES6 isn't perfect. There are some strange language choices and while at the runtime level we are stuck with what ECMA declares, at a syntactic and semantic level we have some degree of freedom as to what the code we write gets commpiled from.

Babel's AST based approach, while modular under the hood, only allows plugins via a poorly documented and fragile API. This isn't to say that Babel is bad, just that it's maintainers goals are focused on providing the ES6 API and so plugins and additions are not first-class citizens.

As of now we plan on using Mozilla's Sweet.js macro system.

## Existential crisis

- [ ] Implement ES6/7/* features as pluggable macros for the Sweet community
- [x] Implement new language features from external communities (PureScript/Haskell, Elm, Clojure, etc)
- [x] Implement syntactic sugar on top of ES6 runtime, which could then be passed to an ES6 transpiler if your runtime does not support it.

## Methodolgy / Manifesto / Strategy / Modus operandi
* Macros should be coupled only to the declarative structure, any non-runtime logic should be pluggable with external implementation or the internal provided one (e.g. write your own curry function or just use the Ramda we plug in).
* Target the ES6 runtime

## Language Specification

### Functions
#### `=>` Bound function declaration
#### `->` Unbound function declaration
#### `~>` Auto-curried function declaration (bindable, but unbound)
#### `*>` Function generator declaration

### Data type literals, perhaps immutable.js mappings
#### `#{}` Map literal
#### `#()` Set literal
#### `∆{}` Weak map literal
#### `∆()` Weak set literal

### Functional programming syntax sugar
#### `|>` pipe operator
`f(x) |> g |> h === h(g(f(x)))`
#### `•` (from Haskell) and/or `>>` (from F#) compose operator
`f * g * h(x) === f >> g >> h(x) === f(g(h(x)))`

### Pattern matching?
