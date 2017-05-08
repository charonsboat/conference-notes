# A lap around React and Angular

## React

### server side architecture

- api (controllers)
- business layer
- data layer

Action based logic is simpler and more modular. Specific controller actions will talk with specific pieces of business logic.

We can break whole stacks into modules with their own layers of each.

#### JavaScript fatigue is a thing.

- switching between build tools such as grunt -> gulp -> webpack
- over the lifetime of your system, you may want to change js frameworks/methodologies... multiple times
- you will put yourself behind in the recruiting game if you are using old technology
    - devs want to work with modern tech, legacy code sucks
- you need to be able to change frameworks without having to rewrite the entire app
    - being able to break out pieces and converting a little at a time makes transitions easier and more manageable
- you need to keep learning

### SPAs (single page apps) and ASPs (apps of single pages)

SPAs:

- communicate to backend via APIs
- maintain state on clients
- servers can act in a stateless manner

ASPs:

- refreshes entire pages
- no state on client
- have to maintain sessions on server

### Angular 1 data binding

view <-data-> controller <-request/response-> service proxy <-cloud-> server

### React/Redux

Redux - unidirectional data binding

- if model changes it bubbles up to the view
- if view changes it bubbles down to the model

How everything communicates:

- view pops action
- action travels through reducer to update state
- new state is stored in store
- data is accessed by view via the store (state maintainer)
- actions might also communicate to backend (response usually sent to reducer to update state)

#### Virtual DOM

- in memory copy of the DOM
- when something changes, it re-renders the DOM virtually (in memory) and calculates a diff to only render the minimun necessary components in the real DOM

JSX

- include HTML in you JS files to make it easier to generate markup

#### Lifecycle Methods

mounting - component is being created and inserted into the DOM
updating - state/props values are changing

#### Testing

Multiple options:

- mocha, jasmine, jest - test runners
- chai - assertions
- enzyme - for testing react components

Things you can test:

- reducers - state changers
- component rendering

## Angular 2


