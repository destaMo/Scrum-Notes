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
- CRA
- JSX
- Components
- Hooks
- Performance
- Devtools
- Codebase structure
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

### 🎤 Interview

- What is React and what is it used for?
- Explain what does the main features of React do: 
  - Being component based
  - Using Virtual DOM
  - Using declarative paradigm
  - JSX

---

## 📦 React / CRA

After this section you will know how to use CRA to quickly setup React application.

### 🎓 Learn

- 📗 [Create React App](https://github.com/facebook/create-react-app)
- 📙 [What CRA actually do](https://levelup.gitconnected.com/what-does-create-react-app-actually-do-73c899443d61)

### 🎤 Interview

- What is create-react-app and how to use it?
- What you would need to do in order to setup a React application without CRA?

### 📝 Katas

- Setup application using CRA
- Show where the command for starting the application is defined, and what code does it run

---

## 📦 React / JSX

After this section you will know how to use JSX, how it differs from HTML and how to use ClassNames package

### 🎓 Learn

- 📗 [Conditional rendering](https://blog.logrocket.com/conditional-rendering-in-react-c6b0e5af381e)
- 📗 [ClassNames package](https://github.com/JedWatson/classnames)
- 📗 [Allowed tags in HTML table tag](https://www.w3schools.com/tags/tag_table.asp#:~:text=An%20HTML%20table%20consists,tfoot%3E%2C%20and%20%3Ctbody%3E%20elements.)
- 📗 [Fragment & flexbox](https://stackoverflow.com/questions/32969287/reactjs-and-flexbox-wrapping-divs-in-render-function-making-flex-hard)
- 🔎 [Handler methods example](https://github.com/Selleo/react_devpath_examples/blob/master/src/pages/Basic/HandlerMethods/HandlerMethods.js)

### 🎤 Interview

- What is the JSX?
  - Under the hood is JSX JavaScript or HTML?
- Differences between JSX and HTML:
  - Why in JSX we need to use "classNames" instead of "class" property and "htmlFor" instead of "for".
- What is the difference between defining handler methods inline, as const, with useCallback. When to use which? (example above)
- Why React components need to be capitalized when using in JSX? eg. &lt;MyComponent&gt; not &lt;myComponent&gt;
- What is React Fragment and how is it useful?
  - When creating table
  - When styling using flex
- What is React Portal?

### 📝 Katas

- Render parts of the UI conditionally
  - Multiple returns from the component
  - Ternary operator
  - "&&" notation
- Display list of data
- Handle user interaction using event handlers
- Use ClassNames package for conditional class assignment

---

## 📦 React / Components

After this section you will know how to use React Components, manage state and perform effects in them.

### 🎓 Learn

- 📗 [Unidirectional data flow](https://medium.com/@lizdenhup/understanding-unidirectional-data-flow-in-react-3e3524c09d8e)
- 📗 [React keys](https://dev.to/jtonzing/the-significance-of-react-keys---a-visual-explanation--56l7)
- 📗 [Reset React Component using key](https://medium.com/@albertogasparin/forcing-state-reset-on-a-react-component-by-using-the-key-prop-14b36cd7448e)

### 🎤 Interview

- "key" Component prop has usages mentioned below, explain how exactly they work 
  - identifying components rendered in an array
  - resetting one specific Component (force component unmount and mount)
- What does it mean that React has Unidirectional data flow?

---

## 📦 React / Hooks

After this section you will know commonly used React hooks and React-Use package.

### 🎓 Learn

- 📗 [Getting current state in setState with function argument](https://stackoverflow.com/questions/42494985/setstate-in-react-based-on-current-state/42496452#42496452)
- 📗 [Preventing memory leaks](https://egghead.io/lessons/react-stop-memory-leaks-with-componentwillunmount-lifecycle-method-in-react)
- 📗 [When to use state and when reducer](https://kentcdodds.com/blog/should-i-usestate-or-usereducer)
- 📗 [React refs guide](https://dmitripavlutin.com/react-useref-guide/)
- 📗 [React-Use](https://github.com/streamich/react-use)

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
- React-Use is package providing multitude of helpful hooks. Which of them you think might be useful for you? What they do?
- How does hooks dependency array work? How to make a hook run on component: mount, unmount, property change

### 📝 Katas

- Use useState hook with:
  - optimized initialValue eg. `useState(() => complex calculation)`
  - setValue with current value eg. `setValue((currentValue) => currentValue + 1)`
- Use useEffect hook with:
  - with empty dependency array
  - with filled dependency array
- When the Function component unmounts clear interval added using setInterval.
- Use useRef hook to hold html element or value reference.
- and useReducer hook in your app in case where it provides benefit over useState.
- Add React Context and consume it in a few components.
- Use at least 2 React-Use hooks in your app.

---

## 📦 React / Performance

After this section you will know how to prevent common programming mistakes degrading React performance.

### 🎓 Learn

- 📗 [Correct key for lists](https://medium.com/information-and-technology/a-simple-list-render-optimization-for-react-ef0a133e9c86)
- 📗 [TODO callback handlers examples]()
- 📗 [TODO TIL different cases when to use useMemo, and when not]()
- 📗 [Pass memoized data and callbacks to components](https://blog.bitsrc.io/optimize-your-react-functional-components-with-usecallback-and-usememo-34bb52bc9a13)
- 📗 [Optimization by reorganization](https://overreacted.io/before-you-memo/)

### 🎤 Interview

- What does the useCallback hook do and when to use it?
- What does the useMemo hook do and when to use it?
- Common performance bad practices are:
  - Using incorrect keys for lists. What keys are good what are bad?
  - Not using memoization for heavy computations in component. When to memoize, when not?
  - Having big components containing multiple states affecting only parts of the UI. How to fix it?

### 📝 Katas

- Use useCallback hook in situation when it provides performance benefit.
- Use useMemo hook in situation when it provides performance benefit.
- Use correct key for lists.

---

## 📦 React / Devtools

After this section you will know how to effectively use React Development tools.

### 🎓 Learn

- 📗 [React Devtools walk-through](https://blog.logrocket.com/debug-react-applications-with-the-new-react-devtools/)

### 🎤 Interview

- What are React Devtools?

### 📝 Katas

- Show how to find a Component in React Devtools (From Elements tab, From App UI, By component name)
- Show how to inspect Component (display state & props & hooks values, change state & props)
- Show how to debug Component (display its HTML element, display Source, access the component from the console)

---

## 📦 React / Codebase structure

After this section you will know how to organize project files in a clear manner.

### 🎓 Learn
- 📗 [How to organize application](https://engineering.udacity.com/react-folder-structure-for-enterprise-level-applications-f8384eff162b)

### 🎤 Katas

- Organize project files according to suggested pattern.

---

## 📦 React / Routing

After this section you will know how to implementing routing in React SPA application.

### 🎓 Learn

- 📗 [React router](https://reacttraining.com/react-router/web/guides/quick-start)
- 📗 [Router concepts](https://blog.bitsrc.io/must-know-concepts-of-react-router-fb9c8cc3c12)
- 📗 [History](https://medium.com/@pshrmn/a-little-bit-of-history-f245306f48dd)

### 🎤 Interview

- Why do we need to implement routing in SPA?
- What are different types of history used for routing?

### 📝 Katas

- Implement routing for a few pages
- Pass and use params through the url (eg. users/:userId)
- Redirect programmatically using history object (from React Router)

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

- Why using form library (like Formik) is often preferable over creating forms without such library?
- What are Wizard Forms and why use them rather than regular forms?
- What is the Button default type and why it is important in the context of forms?
- What is the Difference between Controlled Input and Uncontrolled input?
- Does it make sense to validate forms on the frontend if advanced users can disable it?

### 📝 Katas

- Implement Create and Edit Form in your app. Preferably both cases should be handled by the same component.
- Create Wizard form in your app.
- Implement form with array of fields (eg. user can add multiple addresses each consisting inputs for city, zip-code and street. User should be able to add as many addresses as needed. User should be able to remove addresses)
- Add validation to the form using the Yup library
- Add validation for fields depending on each other using the Yup library (eg. when user selects agreement to receive email, validate the age is over 18. Otherwise do not validate age is over 18)

---

## 📦 React / Testing

After this section you will know how to test React application

### 🎓 Learn

- 📗 [Jest.js](https://jestjs.io/)
- 📗 [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/)
- 📗 [Testing React cheatsheet](https://docs.google.com/presentation/d/10u5q9tKzWq-HDpC3YV-on1gH2jVipVpCiaxxZFvForc/edit#slide=id.g96256219f6_0_4)
- 📙 [Testing React presentation slides](https://docs.google.com/presentation/d/1L2JJ64hksvaU8Zi1omqs4IUiw5TPj3kgAq4_D9bxpRE/edit#slide=id.g96256219f6_0_4)
- 📙 [Testing React presentation recording](https://drive.google.com/file/d/1pNB8yqBDuFk0EaqqdDdpuKSPQrHbv-VD/view?usp=sharing)
- 📗 [Jest timer mocks](https://jestjs.io/docs/en/timer-mocks)
- 📗 [MockDate](https://github.com/boblauer/MockDate)
- 📗 [Axios mock adapter](https://www.npmjs.com/package/axios-mock-adapter)
- 📗 [Factory girl](https://github.com/aexmachina/factory-girl)

### 🎤 Interview

- What does Jest and React Testing Library do?
- When to use integration and when unit tests?
- Does it make sense to add tests for every single component?
- When testing we should "behave" like real user
  - what selectors we should use
  - how should we interact with the application
- What is the use-case for axios-mock-adapter library
- What is the use-case for factory-girl library

### 📝 Katas

- Create tests for a few components using the user perspective
- Create test for code making backend requests
  - delay the mocked responses for 1,5s
  - create the response data using factory girl library
- Create test for code dependent on time
  - displaying datetime or for logic using datetime
- Create test for code dependent on the passing of time
  - timeouts or intervals
- Wait for element to appear/disappear asynchronously

---

## 📦 Server State management / Overview

After this section you will know what is Server State and what challenges it presents.

### 🎓 Learn

- 📗 [Server state challenges](https://redux-toolkit.js.org/rtk-query/overview#motivation)
- 📗 [Server vs Client state presentation (slides)](https://docs.google.com/presentation/d/1Cohzlon3ZDFdKYSQ0_P0x9STEgSDMxQgK8ylVsZ6UpY/edit?usp=sharing)
- 📗 [TODO Server vs Client state presentation (recording)]()

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

- 📙 [React Query](https://react-query.tanstack.com)
- 📙 [RTK Query](https://redux-toolkit.js.org/rtk-query/overview)
- 📙 [Apollo Graphql](https://www.apollographql.com/docs/react/)

### 🎤 Interview

- Which one of the suggested tools do you use?
  - Apollo GraphQL
  - React Query
  - RTK Query

### 📝 Katas

- Implement fetching data for list and single item
  - Display spinner when loading data initially
  - When updating data in the background display small spinner in the corner of the screen
  - After fetching list use the data as initial for single resource
  - Use the backend data in at least 2 components without passing the it through the props
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
- 📗 [Server vs Client state presentation (slides)](https://redux-toolkit.js.org/rtk-query/overview#motivation)
- 📗 [TODO Server vs Client state presentation (recording)]()
- 📗 [TODO TIL when server state becomes client state]()

### 🎤 Interview

- What is Client State?
- How is Client State different from Server State?
- What is Global Client State?

---

## 📦 Global Client State management / Usage

After this section you will know how to manage Global Client State.

### 🎓 Learn

- 📗 [TODO: When to use contexts, when redux]()
- 
- 📗 [Mobx docs](https://github.com/mobxjs/mobx)
- 📗 [Redux Toolkit introduction](https://redux-toolkit.js.org/introduction/getting-started)
- 📗 [When Redux is not needed](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)
- 📗 [Reselect](https://github.com/reduxjs/reselect)
- 📗 [Selectors v2](https://blog.brainsandbeards.com/advanced-redux-patterns-selectors-cb9f88381d74)

- 📗 [Mobx devtools](https://www.npmjs.com/package/mobx-react-devtools)
- 📗 [Redux devtools](https://github.com/reduxjs/redux-devtools)
- 📗 [Redux devtools debugging tips](https://blog.logrocket.com/redux-devtools-tips-tricks-for-faster-debugging/)

- 📗 [TODO: When to add specific tests for Global Client State]()

### 🎤 Interview

- What to do when Global or Subtree State:
  - Is simple or changes rarely.
  - Is complex or changes often.
- Which one of the suggested tools do you use?
  - Redux Toolkit
  - MobX
- What makes the tool you use better in managing Global Client State than just using React Contexts?
- What parts of Redux/Mobx should we test, how?

### 📝 Katas

- Add Redux Toolkit and Reselect to your app and implement TODO: add idea for good redux use-case
- Walk me through the devtools features
- Create a few tests for Redux/MobX
