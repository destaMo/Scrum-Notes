+++
title = "JavaScript/React - Basics"
weight = 1
+++

{{%bubble %}}

## Framework & Language Basics

**Points:** 2

**Description:** You can use basic features of the framework, that allows you to deliver the most common features.

**Person who successfully completed requirement for given block can:**

- Can deliver simple, typical functionalities with little to no additional help
- When asking for help, can present the problem and already explored solutions clearly and in detail
- Can debug simple problems within the application (excluding framework) using the right tooling
- Can use Redux and related tools
- Is capable of leveraging the most commonly used React capabilities
- Has working knowledge of the most commonly used packages/libraries

**Prerequisites:** [Styling basics](/web_development/skills/styling/01_junior_i/)

{{% /bubble%}}

## Areas

**React**

- Overview
- JSX
- Hooks
- Performance
- Devtools
- Routing
- Forms
- Testing

**Server State management**

- Overview
- Usage
- Devtools

**Global Client State management**

- Overview
- Usage

---

## 📦 React / Overview

After this section you will know what is React and what it's used for.

### 🎓 Learn

- 📗 [react main page](https://reactjs.org/)
- 📗 [virtual DOM](https://reactjs.org/docs/faq-internals.html#what-is-the-virtual-dom)
- 📗 [Unidirectional data flow](https://medium.com/@lizdenhup/understanding-unidirectional-data-flow-in-react-3e3524c09d8e)
- 📗 [Create React App](https://github.com/facebook/create-react-app)
- 📗 [How to organize application](https://engineering.udacity.com/react-folder-structure-for-enterprise-level-applications-f8384eff162b)

### 🎤 Interview

- What is React?
- Explain what does the main features of React do: 
  - Being component based
  - Using Virtual DOM
  - Using declarative paradigm 
  - Unidirectional data flow

### 📝 Katas

- Setup application using CRA
- Organize project files according to suggested pattern.

---

## 📦 React / JSX

After this section you will know how to use JSX, how it differs from HTML and how to use ClassNames package

### 🎓 Learn

- 📗 [Conditional rendering](https://blog.logrocket.com/conditional-rendering-in-react-c6b0e5af381e)
- 📗 [Allowed tags in HTML table tag](https://www.w3schools.com/tags/tag_table.asp#:~:text=An%20HTML%20table%20consists,tfoot%3E%2C%20and%20%3Ctbody%3E%20elements.)
- 📗 [Fragment & flexbox](https://stackoverflow.com/questions/32969287/reactjs-and-flexbox-wrapping-divs-in-render-function-making-flex-hard)
- 📗 [ClassNames package](https://github.com/JedWatson/classnames)

### 🎤 Interview

- What is the JSX?
  - Under the hood is JSX JavaScript or HTML?
- Why is React Fragment useful when:
  - creating tables
  - styling using flex
- What is React Portal?

### 📝 Katas

- Render parts of the UI conditionally
  - Multiple returns from the component
  - Ternary operator
  - "&&" notation
- Display list of data
- Handle user interaction (eg. clicks, changes, blurs)
- Use ClassNames package for conditional class assignment

---

## 📦 React / Hooks

After this section you will know commonly used React hooks and React-Use package.

### 🎓 Learn

- 📗 [Getting current state in setState with function argument](https://stackoverflow.com/questions/42494985/setstate-in-react-based-on-current-state/42496452#42496452)
- 📗 [Preventing memory leaks](https://egghead.io/lessons/react-stop-memory-leaks-with-componentwillunmount-lifecycle-method-in-react)
- 📗 [When to use state and when reducer](https://kentcdodds.com/blog/should-i-usestate-or-usereducer)
- 📗 [React refs guide](https://dmitripavlutin.com/react-useref-guide/)
- 📗 [React-Use](https://github.com/streamich/react-use)
- 📗 [Stale closure](https://dmitripavlutin.com/react-hooks-stale-closures/)
- 🔎 [Template for context Provider (code)](https://github.com/Selleo/react_devpath_examples/blob/master/src/pages/Basic/ContextExample/MyContext.js)
- 🔎 [Template for context Provider (app)](https://react-devpath-examples.netlify.app/basics/contextExample)
- 🔎 [Example of useEffect cleanup function (code)](https://github.com/Selleo/react_devpath_examples/blob/master/src/pages/Basic/UseEffectFlow/UseEffectFlow.js)
- 🔎 [Example of useEffect cleanup function (app)](https://react-devpath-examples.netlify.app/basics/useEffect)

### 🎤 Interview

- What are the React Hooks?
- What is useState hook used for?
- What is useEffect hook used for?
- When is the function returned from useEffect triggered?
  - When dependency array is empty
  - When dependency array has values
- What does the useRef hook do and when to use it?
- What does the useReducer hook do and when to use it?
- What is React Context, and what is its use-case?
- What is stale closure, and when it happens?

### 📝 Katas

- Use useState hook with:
  - optimized initialValue eg. `useState(() => complex calculation)`
  - setValue with current value eg. `setValue((currentValue) => currentValue + 1)`
- Use useEffect hook with:
  - with empty dependency array
  - with filled dependency array
- When the Function component unmounts, or changes property clear interval added using setInterval.
- Use useRef hook to hold html element or value reference.
- and useReducer hook in your app in case where it provides benefit over useState.
- Add React Context and consume it in a few components.
- Use at least 2 React-Use hooks in your app.

---

## 📦 React / Performance

After this section you will know how to prevent common mistakes degrading React performance.

### 🎓 Learn

- 📗 [Correct key for lists](https://medium.com/information-and-technology/a-simple-list-render-optimization-for-react-ef0a133e9c86)
- 📗 [Pass memoized data and callbacks to components](https://blog.bitsrc.io/optimize-your-react-functional-components-with-usecallback-and-usememo-34bb52bc9a13)
- 📗 [Optimization by reorganization](https://overreacted.io/before-you-memo/)
- 📗 [How to handle big & slow components](https://selleo.com/til/posts/tiqujjynoi-react-optimization-of-lists-in-big-components)
- 🔎 [Example of big component with state affecting only parts of the UI (code)](https://github.com/Selleo/react_devpath_examples/blob/master/src/pages/Basic/BigListOptimizationExample/Unoptimized/UnoptimizedApp.js)
- 🔎 [Example of big component with state affecting only parts of the UI (app)](https://react-devpath-examples.netlify.app/basics/bigComponentOptimization)
- 🔎 [Handler methods example (code)](https://github.com/Selleo/react_devpath_examples/blob/master/src/pages/Basic/HandlerMethods/HandlerMethods.js)
- 🔎 [Handler methods example (app)](https://react-devpath-examples.netlify.app/basics/handler)

### 🎤 Interview

- What does the useCallback hook do and when to use it?
- What is the difference between defining handler methods inline, as const, with useCallback. When to use which? (example above)
- What does the useMemo hook do and when to use it?
- Common performance bad practices are:
  - Using incorrect keys for lists. What keys are good what are bad?
  - Not using memoization for heavy computations in component. When to memoize, when not?
  - Having big components containing multiple states affecting only parts of the UI. How to fix it? (example above)

### 📝 Katas

- Use useCallback hook in situation when it provides performance benefit.
- Use useMemo hook in situation when it provides performance benefit.
- Use correct key for lists.

---

## 📦 React / Devtools

After this section you will know how to effectively use React Development tools.

### 🎓 Learn

- 📗 [React Devtools walk-through](https://blog.logrocket.com/debug-react-applications-with-the-new-react-devtools/)

### 📝 Katas

- Show how to find a Component in React Devtools (From Elements tab, From App UI, By component name)
- Show how to inspect Component (display state & props & hooks values, change state & props)
- Show how to debug Component (display its HTML element, display Source, access the component from the console)

---

## 📦 React / Routing

After this section you will know how to implement routing in React SPA application.

### 🎓 Learn

- 📗 [React router](https://reacttraining.com/react-router/web/guides/quick-start)
- 📗 [Router concepts](https://blog.bitsrc.io/must-know-concepts-of-react-router-fb9c8cc3c12)
- 📗 [History](https://medium.com/@pshrmn/a-little-bit-of-history-f245306f48dd)

### 🎤 Interview

- What are different types of history used for routing?

### 📝 Katas

- Implement routing for a few pages
- Pass and use params through the url (eg. users/:userId)
- Redirect programmatically using "navigate" from React Router

---

## 📦 React / Forms

After this section you will know how to create basic forms and validate user input.

### 🎓 Learn

- 📗 [Formik](https://github.com/jaredpalmer/formik)
- 📗 [yup.js](https://github.com/jquense/yup/)
- 📗 [Button default action](https://stackoverflow.com/a/10836076)
- 📗 [Controlled vs uncontrolled components](https://stackoverflow.com/a/42522792)
- 📗 [Why use frontend validation](https://www.codebyamir.com/blog/never-trust-data-from-the-browser#:~:text=Client%2DSide%20Validation,to%20the%20user.)

### 🎤 Interview

- Why using form library (like Formik) is preferable over creating forms only by hand?
- What is the Button default type and why it is important in the context of forms?
- What is the Difference between Controlled Input and Uncontrolled input?
- Does it make sense to validate forms on the frontend if advanced users can disable it?

### 📝 Katas

- Implement Create and Edit Form in your app. Preferably both cases should be handled by the same component.
- Implement form with array of fields (eg. user can add multiple addresses each consisting inputs for city, zip-code and street. User should be able to add as many addresses as needed. User should be able to remove addresses)
- Add validation to the form using the Yup library

---

## 📦 React / Testing

After this section you will know how to test React application

### 🎓 Learn

- 📗 [Jest.js](https://jestjs.io/)
- 📗 [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)
- 📗 [Testing React cheatsheet](https://docs.google.com/presentation/d/10u5q9tKzWq-HDpC3YV-on1gH2jVipVpCiaxxZFvForc/edit#slide=id.g96256219f6_0_4)
- 📙 [Testing React cheatsheet slides](https://docs.google.com/presentation/d/10u5q9tKzWq-HDpC3YV-on1gH2jVipVpCiaxxZFvForc/edit)
- 📙 [Testing React presentation slides](https://docs.google.com/presentation/d/1L2JJ64hksvaU8Zi1omqs4IUiw5TPj3kgAq4_D9bxpRE/edit#slide=id.g96256219f6_0_4)
- 📙 [Testing React presentation recording](https://drive.google.com/file/d/1pNB8yqBDuFk0EaqqdDdpuKSPQrHbv-VD/view?usp=sharing)
- 📗 [Jest timer mocks](https://jestjs.io/docs/en/timer-mocks)
- 📗 [Axios mock adapter](https://www.npmjs.com/package/axios-mock-adapter)

### 🎤 Interview

- What does Jest and React Testing Library do?
- When to use integration and when unit tests?
- Does it make sense to add tests for every single component?
- What is the use-case for axios-mock-adapter library

### 📝 Katas

- Create tests for a few components using the user perspective
- Create test for code making backend requests
  - delay the mocked responses for 1,5s
- Create test for code dependent on the passing of time
  - timeouts or intervals
- Wait for element to appear/disappear asynchronously

---

## 📦 Server State management / Overview

After this section you will know what is Server State and what challenges it presents.

### 🎓 Learn

- 📗 [Server state challenges](https://redux-toolkit.js.org/rtk-query/overview#motivation)
- 📗 [Server vs Client state presentation slides (slides 5 to 9)](https://docs.google.com/presentation/d/1Cohzlon3ZDFdKYSQ0_P0x9STEgSDMxQgK8ylVsZ6UpY/edit?usp=sharing)

[comment]: <> (- 📗 [TODO Server vs Client state presentation recording]&#40;&#41;)

### 🎤 Interview

- What is Server State?
- What challenges arise from Server State unique characteristics mentioned below:
  - Is asynchronous
  - We do not control the source of truth (backend)
  - Other users or systems can change it
  - We need the data in different places of the application
  - Different places of the application might try to fetch the same resource
  - More possibilities for something to break (network/backend issues)
- Why traditional solutions like Contexts or Redux are not suitable for managing Server State?

---

## 📦 Server State management / Usage

After this section you will know how to implement basic features for Server State.

### 🎓 Learn

- 📗 [Simple backend with json-server](https://github.com/typicode/json-server)
- 📙 [React Query](https://react-query.tanstack.com)
- 📙 [RTK Query](https://redux-toolkit.js.org/rtk-query/overview)
- 📙 [Apollo Graphql](https://www.apollographql.com/docs/react/)

### 🎤 Interview

- Which one of the suggested tools do you use?
  - Apollo GraphQL
  - React Query
  - RTK Query

### 📝 Katas

- Setup simple backend using json-server (unless you have other tool)
- Implement fetching data for list and single item
  - Display spinner during initial data load
  - When updating data in the background display small spinner in the corner of the screen
  - After fetching list use the data as initial for single resource
  - Use the backend data in at least 2 components without passing them through the props
  - When using backend data in 2 components make sure request is sent only once
- Implement CRUD for resource
  - Handle create, update, delete actions 
  - Invalidate cache of changed item after performing update request
  - Handle errored requests with 2 retries

---

## 📦 Server State management / Devtools

After this section you will know how to use devtools for preferred Server State management package.

### 🎓 Learn

- 📙 [React-Query devtools](https://react-query.tanstack.com/devtools)
- 📙 [RTK Query devtools (regular redux devtools)](https://github.com/zalmoxisus/redux-devtools-extension#docs)
- 📙 [Apollo Graphql devtools](https://www.apollographql.com/docs/react/development-testing/developer-tooling/#apollo-client-devtools)

### 📝 Katas

- Setup devtools for your package (if applicable)
- Show the devtools features and explain how they are useful

---

## 📦 Global Client State management / Overview

After this section you will know what is Client State and Global Client State.

### 🎓 Learn

- 📗 [8 ways to handle Client State](https://twitter.com/housecor/status/1437765667906854915?lang=en)
- 📗 [Server vs Client state presentation (slides 5 to 9)](https://docs.google.com/presentation/d/1Cohzlon3ZDFdKYSQ0_P0x9STEgSDMxQgK8ylVsZ6UpY/edit#slide=id.gebf84830b7_0_0)

[comment]: <> (- 📗 [TODO Server vs Client state presentation &#40;recording&#41;]&#40;&#41;)

### 🎤 Interview

- What is Client State?
- What is Global Client State?
- How is Client State different from Server State?

---

## 📦 Global Client State management / Usage

After this section you will know how to manage Global Client State.

### 🎓 Learn

- 📗 [Mobx docs](https://github.com/mobxjs/mobx)
- 📗 [Redux Toolkit introduction](https://redux-toolkit.js.org/introduction/getting-started)
- 📗 [When Redux is not needed](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)
- 📗 [Reselect](https://github.com/reduxjs/reselect)
- 📗 [Selectors v2](https://blog.brainsandbeards.com/advanced-redux-patterns-selectors-cb9f88381d74)

- 📗 [Mobx devtools](https://www.npmjs.com/package/mobx-react-devtools)
- 📗 [Redux devtools](https://github.com/reduxjs/redux-devtools)
- 📗 [Redux devtools debugging tips](https://blog.logrocket.com/redux-devtools-tips-tricks-for-faster-debugging/)

- 📗 [When to add unit tests for Global Client State](https://docs.google.com/presentation/d/1L2JJ64hksvaU8Zi1omqs4IUiw5TPj3kgAq4_D9bxpRE/edit#slide=id.g1018d1a4257_1_81)

### 🎤 Interview

- What to do when Global or Subtree State:
  - Is simple or changes rarely
  - Is complex or changes often
- Which one of the suggested tools do you use?
  - Redux Toolkit
  - MobX
- Why the tool you use is better in managing Global Client State than React Contexts?
- In what situations should we tests Redux/Mobx?

### 📝 Katas

- Add Redux Toolkit and Reselect to your app and implement managing non-backend data
- Walk me through the devtools features
- Create a few tests for Redux/MobX
