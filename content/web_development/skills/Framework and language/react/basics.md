+++
title = "JavaScript/React - Basics"
weight = 1
+++

{{%bubble %}}

## Framework & Language Basics

**Points:** 2 

**Description:** You can use basic features of the framework, that allows you to deliver the most common features.

**Person which successfully completed requirement for given block can:** 

- Can deliver simple, typical functionalities with little to no additional help
- When asking for help, can present the problem and already explored solutions clearly and in detail
- Can debug simple problems within the application (excluding framework) using the right tooling
- Can present the strenghts and use cases for the framework
- Is capable of leveraging most commonly used standard library capabilities
- Has working knowledge of most commonly used packages/libraries

**Prerequisites:** [Styling basics](/web_development/skills/styling/01_junior_i/)

{{% /bubble%}}

## Areas

**React**

- Overview
- JSX
- Handling events
- Validating props structure
- Setting up the app
- Accessing DOM elements
- Structuring the app
- Performance
- Cleaning up on end of component life
- Routing

**State management**

- React state and props
- Redux
- MobX (alternative)

**Forms**

- Forms
- Validation

**Testing**

- Testing
- Rendering React

**Patterns**

- Patterns

---

## 📦 React / Overview

Know what is React and what it's used for.

### 🎓 Learn

- 📗 [react main page](https://reactjs.org/)
- 📗 [what is react](https://reactjs.org/tutorial/tutorial.html#what-is-react)
- 📗 [react lifecycle](http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

### 🎤 Interview

- What is React?
- What lifecycle flows & methods does React have?

---

## 📦 React / JSX

Know what is JSX and how to use it in React.

### 🎓 Learn

- 📗 [JSX in depth](https://reactjs.org/docs/jsx-in-depth.html)
- 📗 [Function and class components](https://reactjs.org/docs/components-and-props.html#function-and-class-components)
- 📗 [Functional stateless component](https://stackoverflow.com/questions/40703675/react-functional-stateless-component-purecomponent-component-what-are-the-dif)
- 📗 [Conditional rendering](https://blog.logrocket.com/conditional-rendering-in-react-c6b0e5af381e)
- 📗 [ClassNames package](https://github.com/JedWatson/classnames)
- 📗 [Fragments](https://reactjs.org/docs/fragments.html)
- 📗 [Portals](https://reactjs.org/docs/portals.html)

### 🎤 Interview

- What is the JSX?
- What are the differences between JSX and HTML?
- What are the types of React components?
- Why React components need to be capitalized when using in JSX? eg. <MyComponent>
- How to handle conditionally assigned css classes?
- What is React Fragment?
- What is React Portal?

---

## 📦 React / Handling events

Knows how to add behavior to interactions with the UI.

### 🎓 Learn

- 📗 [Events](https://reactjs.org/docs/events.html)
- 📗 [Handling events](https://medium.com/@machnicki/handle-events-in-react-with-arrow-functions-ede88184bbb)

### 🎤 Interview

- How to assign handler to element event?
- Why it’s better to define handler method as fat arrow than assign it using fat arrow in render?

---

## 📦 React / Validating props structure

Knows how to validate properties received by the component.

### 🎓 Learn

- 📗 [validating props with prop types](https://blog.logrocket.com/validating-react-component-props-with-prop-types-ef14b29963fc)

### 🎤 Interview

- What are React Prop types and how to use them?

---

## 📦 React / Setting up the app

Knows how to use CRA to quickly setup React application.

### 🎓 Learn

- 📗 [Create React App](https://github.com/facebook/create-react-app)

### 🎤 Interview

- What is create-react-app and how to use it?

---

## 📦 React / Accessing DOM elements

Knows how to use refs to get element reference in script.

### 🎓 Learn

- 📗 [Refs and the dom](https://reactjs.org/docs/refs-and-the-dom.html)

### 🎤 Interview

- How to use React Ref’s to get DOM element?

---

## 📦 React / Structuring the app

Knows how to structure the react application.

### 🎓 Learn

- 📗 [Project structure](https://hackernoon.com/structuring-projects-and-naming-components-in-react-1261b6e18d76)
- 📗 [How to organize application](https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1)

### 🎤 Interview

- How would you structure react components and redux files?
- What structure of folders you have on the project? Would you change something?

---

## 📦 React / Performance

Knows how to avoid bad patterns affecting performance.

### 🎓 Learn

- 📗 [React keys](https://dev.to/jtonzing/the-significance-of-react-keys---a-visual-explanation--56l7)
- 📗 [Using shouldComponentUpdate](https://developmentarc.gitbooks.io/react-indepth/content/life_cycle/update/using_should_component_update.html)
- 📗 [List of optimizations](https://medium.com/information-and-technology/a-simple-list-render-optimization-for-react-ef0a133e9c86)

### 🎤 Interview

- How does React identify components as the same even if it’s properties change?
- What are bad practices affecting React performance?
- What should be the key for list elements?

---

## 📦 React / Cleaning up on end of component life

Knows possible situations leading to memory leaks and how to prevent them.

### 🎓 Learn

- 📗 [Forcing component remount](https://medium.com/@albertogasparin/forcing-state-reset-on-a-react-component-by-using-the-key-prop-14b36cd7448e)
- 📗 [Preventing memory leaks](https://egghead.io/lessons/react-stop-memory-leaks-with-componentwillunmount-lifecycle-method-in-react)

### 🎤 Interview

- How to unmount component?
- How to replace the same component class - unmount old and mount new?
- How to prevent memory leaks in React?

---

## 📦 React / Routing

Knows how to make multiple routes in React app.

### 🎓 Learn

- 📗 [React router](https://reacttraining.com/react-router/web/guides/quick-start)
- 📗 [Router concepts](https://blog.bitsrc.io/must-know-concepts-of-react-router-fb9c8cc3c12)
- 📗 [Understanding react router](https://medium.com/@AkyunaAkish/understanding-react-router-4-df73a66d96c4)
- 📙 [Redux router](https://github.com/acdlite/redux-router)

### 🎤 Interview

- How do you handle routes in your app?
- How to pass and use params as part of url?
- How to programmatically redirect to another route?

### 📝 Katas

- Implement routing for a few pages
- Pass and use params through the url (eg. users/:userId)
- Redirect programmatically using history object (from React Router)

---

## 📦 State management / React state and props

Knows how to manage state using only the React tools. 

### 🎓 Learn

- 📗 [React state](https://reactjs.org/docs/state-and-lifecycle.html)
- 📗 [Unidirectional data flow](https://medium.com/@lizdenhup/understanding-unidirectional-data-flow-in-react-3e3524c09d8e)


### 🎤 Interview

- How to modify component state?
- What’s the difference between state and props?
- What is unidirectional data flow? How it works in React?

### 📝 Katas

- Implement usage of props and state.

---

## 📦 State management / Redux

Knows how to use Redux.

### 🎓 Learn

- 📗 [When Redux is not needed](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)
- 📗 [Redux introduction](https://redux.js.org/introduction/getting-started)
- 📗 [Functional programming paradigms](https://hackernoon.com/functional-programming-paradigms-in-modern-JavaScript-immutability-4e9751ca005c)
- 📗 [Redux step-by-step](https://hackernoon.com/redux-step-by-step-a-simple-and-robust-workflow-for-real-life-apps-1fdf7df46092)
- 📗 [Seamless immutable](https://medium.com/@ckoster22/seamless-immutable-an-alternative-to-immutablejs-12795d6bf577)
- 📗 [Selectors](https://redux.js.org/introduction/learning-resources#selectors)
- 📗 [Selectors v2](https://blog.brainsandbeards.com/advanced-redux-patterns-selectors-cb9f88381d74)
- 📗 [Redux devtools](https://github.com/reduxjs/redux-devtools)

### 🎤 Interview

- What is Redux?
- What is the use case(s) for Redux?
- How do you connect Redux to React app and use it to manage application state?
- What elements does Redux have and what are their responsibilities?
- Can you mutate redux store data? Why?
- How Redux devtools can support you with debugging/development?
- What’s the flow from user interaction through redux and back to UI?


### 📝 Katas

- Implement Redux (action creators, reducers, selectors, and connect to the component)

---

## 📦 State management / MobX (alternative)

Knows how to use MobX for state management.

### 🎓 Learn

- 📗 [Mobx main page](https://github.com/mobxjs/mobx)
- 📗 [Redux vs Mobx](https://www.robinwieruch.de/redux-mobx-confusion)
- 📗 [Flows](https://mobx.js.org/best/actions.html#flows)
- 📗 [React bindings for MobX](https://github.com/mobxjs/mobx-react)
- 📗 [Observable](https://github.com/mobxjs/mobx#observable-state)


### 🎤 Interview

- How do you use mobx to manage application state?
- What’s the flow from user interaction through mobx and back to UI?
- What are observables, and how to turn any data structure into it?
- What are computed values and how to use them?
- What are reactions and how to use them?
- How to handle errors in computed values and reactions?
- What are actions and how to use them?
- How do you connect mobx with react component?
- Why it is discouraged to use shouldComponentUpdate
- Why it is discouraged to use Observer with pureComponent 

---

## 📦 Forms

Knows how to create forms in React using the popular libraries.

### 🎓 Learn

- 📗 [Formik](https://github.com/jaredpalmer/formik)
- 📗 [Controlled vs uncontrolled components](https://stackoverflow.com/a/42522792)
- 📗 [Button default action](https://stackoverflow.com/a/10836076)
- 📙 [Redux form](https://redux-form.com/8.1.0/)

### 🎤 Interview

- What form solutions you are familiar with? How they work for you?
- What are the differences between create and edit forms? How do you handle them?
- Difference between Controlled Component and Uncontrolled Component?
- What should you be aware of when having many buttons in form?

### 📝 Katas

- Create one form for create and edit
- Create form handling nested data (eg. user.address.postalCode)
- Create form handling data arrays

---

## 📦 Forms / Validation

Knows how to validate forms in different stages of the user interaction.

### 🎓 Learn

- 📗 [yup.js](https://github.com/jquense/yup/)
- 📗 [Submit and field validation in formik](https://jaredpalmer.com/formik/docs/guides/validation)
- 📗 [Running validation in redux form](https://redux-form.com/7.3.0/examples/syncvalidation/)

### 🎤 Interview

- Does it make sense to validate forms on the frontend, as advanced users can disable it?
- When to validate form inputs?
- Have you implemented some advanced validations? What were they?
- Do you use package, or custom conditionals to validate form data? How is that solution work for you?
- What two conditions should be met to show error message under input

### 📝 Katas

- Add validation
    - on input change
    - on form submit

---

## 📦 Testing

Knows how to test frontend application and how to provide the test data.

### 🎓 Learn

- 📗 [Jest.js](https://jestjs.io/)
- 📗 [Faker.js](https://github.com/marak/Faker.js)
- 📗 [Unit testing react](https://medium.com/JavaScript-scene/unit-testing-react-components-aeda9a44aae2)
- 📗 [Factory girl](https://github.com/aexmachina/factory-girl)

### 🎤 Interview

- How do you test your application?
- How do you provide data for tests?

---

## 📦 Testing / Rendering React

Knows how to use Enzyme or React Testing Library to render components in unit tests.

### 🎓 Learn

- 📗 [Enzyme](https://github.com/airbnb/enzyme/) suggested
- 📗 [Why not use shallow rendering](https://blog.kentcdodds.com/why-i-never-use-shallow-rendering-c08851a68bb7)
- 📗 [Why use shallow rendering](https://hackernoon.com/why-i-always-use-shallow-rendering-a3a50da60942)
- 📗 [Pattern to setup components in enzyme](https://selleo.com/blog/how-to-setup-react-component-in-tests)
- 📙 [React testing library](https://github.com/testing-library/react-testing-library)
- 📙 [Additional matchers for enzyme](https://github.com/FormidableLabs/enzyme-matchers/tree/master/packages/jest-enzyme)

### 🎤 Interview

- How do you render React component in tests?
- Do you repeat component setup on every test case?

### 📝 Katas

- Add tests for component UI (conditional rendering & rendering of the lists)
    - find element and expect it’s content
    - using snapshots
- Add tests for event handlers
    - find element, perform event (eg. click) and test what happened next
- Add tests for code in lifecycle methods
- Add tests for methods passed to child components.
- Setup component using buildSetup pattern
- Add tests for reducer
- Add tests using full rendering for component connected to store (will require creating mocked store)

---

## 📦 Patterns

Know what are Higher Order Components and how to test them.

### 🎓 Learn

- 📗 [HOC-in-depth](https://medium.com/@franleplant/react-higher-order-components-in-depth-cf9032ee6c3e)
- 📗 [Components golden rule](https://medium.freecodecamp.org/how-the-golden-rule-of-react-components-can-help-you-write-better-code-127046b478eb)
- 📙 [HOC-deep-dive1](https://medium.com/@toastui/a-deep-dive-into-the-react-hoc-1-fb431c131866)
- 📙 [HOC-deep-dive2](https://medium.com/@toastui/a-deep-dive-into-the-react-hoc-2-3e8ed18b848b)

### 🎤 Interview

- How does HOC’s work, and how to share functionality between components?
- What about general purpose functions needed in different components? e.g date formatting

### 📝 Katas

- Create HOC and use it a few times to share the behaviour between multiple components
- Add tests for HOC
