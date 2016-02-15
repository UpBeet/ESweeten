# `ESweeten` (alternatively `diabetES`)

A modular (but opinionated) macro based extension of the JavaScript runtime 

## Motivation

ES6 isn't perfect. There are some strange language choices and while at the runtime level we are stuck with what ECMA declares, at a syntactic and semantic level we have some degree of freedom as to what the code we write gets commpiled from.

Babel's AST based approach, while modular under the hood, only allows plugins via a poorly documented and fragile API. This isn't to say that Babel is bad, just that it's maintainers goals are focused on providing the ES6 API and so plugins and additions are not first-class citizens.

As of now we plan on using Mozilla's Sweet.js macro system.

## Language Specification

### Functions
#### `=>` Bound function declaration
#### `->` Unbound function declaration
#### `~>` Autocurried function declaration (bindable, but unbound)
#### `*>` Function generator declaration

### Variable declaration
#### `let`
#### `const`
### `type` || `` for immutable declaration?

### Decorators

## What we are exluding (for now)

* Classes
* ???
