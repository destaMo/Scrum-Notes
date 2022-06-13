+++
title = "JavaScript/React - Advanced"
weight = 2
+++

{{%bubble %}}

## Framework & Language Advanced

**Points:** 2

**Description:** You can apply the best practices across the framework while delivering solution.

**Person who successfully completed requirement for given block can:**

- Comprehend, design and deliver a full range of functionalities with no need for consultation (yet intuitively knows, when to ask for second opinion)
- Demonstrate debugging skills for a full range of problems within application, also by investigating the framework code
- Identify all framework capabilities and best-practices
- Name, explain, choose and apply a wide range of software design patterns to solve particular problems
- Demonstrate strong skills in TDD/BDD

**Prerequisites:**
- [Styling advanced 1](/web_development/skills/styling/02_junior_ii/)
- [Styling advanced 2](/web_development/skills/styling/03_independent_i/)

{{% /bubble%}}

## Areas

**React**

- React with TS
- Hooks
- Performance
- Error handling
- Patterns
- Code-smells
- Testing

**Redux**

- Usage
- Tools
- Debugging

**Application Features**

- Bundle optimization
- Realtime

**Graphql with Apollo**

- Usage
- TypeScript
- Subscriptions

---

## 📦 React / React with TS

After this section you will know how to setup and use TypeScript in React.

### 🎓 Learn

- 📗 [CRA with TS](https://create-react-app.dev/docs/adding-typescript/)
- 📗 [React TS Cheatsheet](https://github.com/typescript-cheatsheets/react)
- 📗 [Typescript React tips](https://medium.com/@martin_hotell/10-typescript-pro-tips-patterns-with-or-without-react-5799488d6680)
- 📗 [Typesync](https://github.com/jeffijoe/typesync)
- 📗 [Generic components](https://react-typescript-cheatsheet.netlify.app/docs/advanced/patterns_by_usecase#generic-components)
- 📗 ["as" type assertion](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#type-assertions)
- 📗 ["is" type guard](https://www.typescriptlang.org/docs/handbook/advanced-types.html#user-defined-type-guards)

### 🎤 Interview

- How to setup app using CRA with TS?
- How to add TS to existing CRA app?
- What's the difference between JSX.Element vs React.ReactNode types, and which one should be used to type props.children?
- How to type component props?
- How to type context when default value is 'undefined'?
- Typescript Enums usage is discouraged. What should we do instead?
- What does the Typesync package do?
- Explain what does (as, is, in, typeof, keyof, !, ?) operators do?

### 📝 Katas

- Setup or add TS to evaluation application
- Have the app typed without 'any' keyword

---

## 📦 React / Hooks

After this section you will know how to use less common React hooks and create own hooks.

### 🎓 Learn

- 📗 [React hooks](https://reactjs.org/docs/hooks-reference.html)
- 📗 [Stale closure in react hooks](https://dmitripavlutin.com/react-hooks-stale-closures/)

### 🎤 Interview

- Explain how does useImperativeHandle, useLayoutEffect, useDebugValue hooks work and when to use them.
- What is stale closure and how to prevent it in react hooks?
- What are the rules of hooks?

### 📝 Katas

- Implement your custom hook and use it.

---

## 📦 React / Performance

After this section you will know how to optimize React and measure the application performance.

### 🎓 Learn

- 📗 [React profiler](https://kentcdodds.com/blog/profile-a-react-app-for-performance)
- 📗 [React memo](https://dmitripavlutin.com/use-react-memo-wisely/)
- 📗 [React virtualized](https://blog.theodo.fr/2018/09/use-react-virtualized/)
- 📗 [Lists in memoized component](https://selleo.com/til/posts/tiqujjynoi-react-optimization-of-lists-in-big-components)
- 📗 [useRef as optimization technique](https://hackernoon.com/how-to-optimize-react-performace-by-using-useref-hooks-4t1n315h)
- 📗 [Forwarding refs](https://reactjs.org/docs/forwarding-refs.html)

### 🎤 Interview

- When to use React.memo for optimization? Why not use it always?
- How to rerender component only when certain prop changes?
- What is virtualization and how it improves app performance?
- Why extracting lists to separate component might improve performance, and when it should be done?
- When and how use refs for optimization?
- What is refForwarding, and when to use it?

### 📝 Katas

- Use react profiler to check the application performance in development mode.
- Use react profiler to check the application performance in production mode.
- Use react.memo in your app in a way that improves the performance.
- Implement virtualized list in the application. Show the difference with and without virtualization.

---

## 📦 React / Error handling

After this section you will know how to handle errors on production.

### 🎓 Learn

- 📗 [Error Boundaries](https://reactjs.org/docs/error-boundaries.html)
- 📗 [CRA adds overlay on error](https://github.com/facebook/create-react-app/issues/3627)
- 📗 [Sentry for React](https://sentry.io/for/react/)

### 🎤 Interview

- What are error boundaries? What methods does error boundary has?
- Which errors cannot be caught by error boundary?
- What are sourcemaps?
- Why we need external services for error tracking in production?

### 📝 Katas

- Add error boundary to your app, so the application handles UI errors gracefully.
- Make sure your production build has source maps.
- Use free plan of Sentry to monitor errors in deployed application.

---

## 📦 React / Patterns

After this section you will know common react patterns.

- 📗 [HOC-in-depth](https://medium.com/@franleplant/react-higher-order-components-in-depth-cf9032ee6c3e)
- 📗 [RenderProps](https://tylermcginnis.com/react-render-props/)
- 📗 [Containment part1](https://twitter.com/dan_abramov/status/1021850251865587712)
- 📗 [Containment part2](https://twitter.com/a_wazard/status/1021861930603036672)
- 📗 [Containment & Specialization](https://reactjs.org/docs/composition-vs-inheritance.html)
- 📗 [Containment (here called Compound)](https://medium.com/@Dane_s/react-js-compound-components-a6e54b5c9992)
- 📗 [Components golden rule](https://medium.freecodecamp.org/how-the-golden-rule-of-react-components-can-help-you-write-better-code-127046b478eb)

### 🎤 Interview

- How does HOC’s work, and how to share functionality between components?
- What about general purpose functions needed in different components? e.g date formatting
- How does RenderProps work?
- How does the Specialization work?
- How does the Containment work?
- What’s the difference between Containment and RenderProps patterns?

### 📝 Katas

- Create HOC and use it a few times to share the behaviour between multiple components
- Share functionality with render prop
- Create a generic component used by at least 2 specialized components
- Create a component according to containment pattern

---

## 📦 React / Code-smells

After this section you will be able to spot common code-smells in React and know how to fix them.

### 🎓 Learn

- 📗 [Multiple code smells](https://antongunnarsson.com/react-component-code-smells/)
- 📗 [Mapping UI with item methods](https://selleo.com/til/posts/5ow1uwvx4u-react-code-smells-mapping-ui-having-methods-for-items)
- 📗 [Big components that couldn't be split](https://selleo.com/til/posts/o8vscahgsw-react-code-smells-big-form-components)
- 📗 [Props used only to calculate another value](https://selleo.com/til/posts/os7iebhu87-react-code-smells-passing-unnecessary-props)
- 📗 [Data preparation in component](https://selleo.com/til/posts/zpky27yv6u-react-redux-code-smells-data-preparation-in-component)
- 📗 [Storing data from props in state](https://selleo.com/til/posts/nbg6zqxe3n-react-redux-code-smells-storing-props-in-state)

### 🎤 Interview

- What can we do with Big/Complex components > ~300LOC? (3 solutions)
- What can we do when mapped UI has methods for mapped items?
- What can we do when component receives lots of props? (3 solutions)
- Why handling data preparation in component (when having redux) is an antipattern?
- What can we do when having multiple useState in component?
- In which cases below storing data from props in state is an antipattern? What are possible fixes?
  - when child stores transformed props.
  - when child needs to change value of props
  - when child should be able to change value from props, but should not change parent data

---

## 📦 React / Testing

After this section you will know how to test async code.

### 🎓 Learn

- 📗 [Use debugger in jest tests](https://pragmaticpineapple.com/7-ways-to-debug-jest-tests-in-terminal/)
- 📗 [Use breakpoints and logpoints](https://selleo.com/til/posts/mxkd8fpqbw-debug-prod-app-with-logpoints-conditional-breakpoints)
- 📗 [Jest ES6 Mock](https://jestjs.io/docs/es6-class-mocks)
- 📗 [TDD with React Testing Library](https://typeofweb.com/tdd-react-testing-library/)
- 📗 [When to use TDD](https://kentcdodds.com/blog/when-i-follow-tdd)
- 📗 [MockDate](https://github.com/boblauer/MockDate)
- 📙 [use React Devtools in Cypress tests](https://selleo.com/til/posts/rvajzbhbww-loading-react-redux-dev-tools-in-cypress)

### 🎤 Interview

- What are the challenges when testing async code?
- What are the challenges when testing time dependent code?
- Is mocking in tests good or bad practice? Why?

### 📝 Katas

- What is TDD?
- When to use TDD?
- Develop a few components or the whole app using TDD (should be verifiable by commit history)
- Mock imported library using Jest ES6 Mocks
- Create test for code dependent on time
  - displaying datetime

  or
  - logic using datetime

---

## 📦 Redux / Usage

After this section you will know what are best practices in redux, what is redux toolkit and how to use re-reselect.

### 🎓 Learn

- 📗 [Redux style guide](https://redux.js.org/style-guide/style-guide)
- 📗 [Suggested redux store structure](https://selleo.com/til/posts/csah7dmbxh-redux-suggested-store-structure)

### 🎤 Interview

- What is the preferred redux file structure?
- Should redux store be structured based on UI or data types?
- Why data in redux should be normalized? What is the preferred structure?

### 📝 Katas

- Implement redux in your application according to style guides. What have you changed?
- Implement backend data normalization.

---

## 📦 Redux / Tools

After this section you will know how to use more advanced middleware than redux thunk.

### 🎓 Learn

- 📗 [Redux toolkit](https://redux-toolkit.js.org/)
- 📗 [Redux toolkit devtools default](https://selleo.com/til/posts/tevlm7o3lb-redux-devtools-config-with-redux-toolkit)
- 📗 [re-reselect](https://github.com/toomuchdesign/re-reselect)
- 📗 [Custom redux middleware](https://medium.com/@jacobp100/you-arent-using-redux-middleware-enough-94ffe991e6)
- 📗 [Redux-observable](https://redux-observable.js.org/)
  OR
- 📗 [Redux-saga](https://redux-saga.js.org/)

### 🎤 Interview

- What is redux toolkit and how it simplifies working with redux?
- What is re-reselect? How it differs with reselect?
- How does redux middlewares work? How can you create your own middleware?
- What are use cases for middlewares like redux-observable or redux-saga compared to thunk?
- How does redux-observable or redux-saga works?

### 📝 Katas

- Implement redux using redux toolkit.
- Implement selector using re-reselect in situation when it is appropriate.
- Implement selector with custom equality check.
- Use redux-observable or redux-saga to implement some complex flow in redux.

---

## 📦 Redux / Debugging

After this section you will know how to debug redux store in production.

### 🎓 Learn

- 📗 [Redux middleware for sentry](https://docs.sentry.io/platforms/javascript/guides/react/configuration/integrations/redux/)
- 📗 [Using redux devtools in production](https://medium.com/@zalmoxis/using-redux-devtools-in-production-4c5b56c5600f)
- 📗 [Monitor store on production without devtools](https://selleo.com/til/posts/ksyni8azo6-monitor-redux-store-on-production)
- 📗 [Access store on production without devtools](https://stackoverflow.com/a/44318447/4349813)

### 🎤 Interview

- Why integrate redux with sentry?
- What do you think about enabling redux devtools on production?
- How to display and monitor store on production when redux devtools are not enabled?

### 📝 Katas

- Add sentry middleware to redux.
- In sentry middleware use state and action transformers.

---

## 📦 Application Features / Bundle optimization

After this section you will know how to split and optimize application bundle size.

### 🎓 Learn

- 📗 [Lazy](https://reactjs.org/docs/code-splitting.html#reactlazy)
- 📗 [Suspense](https://reactjs.org/docs/code-splitting.html#suspense)
- 📗 [Webpack bundle analyzer](https://www.npmjs.com/package/webpack-bundle-analyzer)
- 📗 [Analyze bundle with CRA](https://create-react-app.dev/docs/analyzing-the-bundle-size/)
- 📗 [Tips on bundle optimization](https://selleo.com/til/posts/tv7kzj7rkl-react-app-bundle-optimalization)


### 🎤 Interview

- How can we inspect bundle size to find possible issues?
- How to decide if the application needs code splitting?
- How can we decrease initial bundle size using lazy and suspense?

### 📝 Katas

- Create examples of lazy and suspense.
- Generate visualization for your app bundle.

---

## 📦 Application Features / Realtime

After this section you will know how to implement realtime functionalities.

### 🎓 Learn

- 📗 [HTTP vs WS](https://medium.com/platform-engineer/web-api-design-35df8167460)
- 📗 [socked.io with react](https://medium.com/dailyjs/combining-react-with-socket-io-for-real-time-goodness-d26168429a34)

### 🎤 Interview

- What are websockets? How they compare to http?
- What are alternatives if for some reason you cannot use websockets in your project?
- What is socked.io and how does it help with implementing realtime communications in web app?

### 📝 Katas

- Implement real time data feature with socked.io

---

## 📦 Graphql with Apollo / Usage

After this section you will know how to use graphql queries and mutations.

### 🎓 Learn

- 📗 [Graphql](https://graphql.org/learn/)
- 📗 [Apollo React](https://www.apollographql.com/docs/react/)

- 📗 [Rubymine/Webstorm config](https://selleo.com/til/posts/gl9wnfvo8f-configure-graphql-syntax-highlight-in-intellij-ides)
- 📗 [VSCode config](https://selleo.com/til/posts/m8hz8irrqk-configure-graphql-syntax-highlight-in-vs-code)

### 🎤 Interview

- What is GraphQL and how it’s different from the REST?
- What is Apollo?
- How do you get data?
- How do you update data?
- How to use Fragments to simplify queries and mutations?
- What Aliases in graphql query?
- What are @include @skip Directives? What they do?

### 📝 Katas

- Create example CRUD app using GraphQL
- 📗 [easy to setup Graphql local server](https://www.npmjs.com/package/json-graphql-server) you can create your own
- 📗 [example DB](https://gist.github.com/pokiujf/c466843979fda7c640518b58278a0dfd) you can create your own

---

## 📦 Graphql with Apollo / TypeScript

After this section you will know how to generate types for your schema and use them in the frontend.

### 🎓 Learn

- 📗 [creating types and hooks with codegen](https://selleo.com/til/posts/g8sdwxnyzl-use-graphql-schema-to-create-ts-types-and-react-hooks)

### 🎤 Interview

- What benefit do we have from using codegen, and typing backend responses?

### 📝 Katas

- Configure typings and code generation in your project.
- Use generated hooks for fetching/updating data.
- Use the typings for data returned from the server.

---

## 📦 Graphql with Apollo / Subscriptions

After this section you will know how to implement realtime communication using graphql Subscriptions.

### 🎓 Learn

- 📗 [Subscriptions](https://www.apollographql.com/docs/react/data/subscriptions/)
- 📗 [Realtime app with GraphQL](https://hackernoon.com/real-time-react-app-with-graphql-websocket-fe64f42e97bc)
- 📗 [GraphQL subscriptions](https://medium.com/@hpux/make-web-real-time-with-graphql-subscriptions-5a59ac1b010c)

### 🎤 Interview

- What are Graphql Subscriptions?
- When to use Subscriptions and when polling?

### 📝 Katas

- Configure websocket and http links for Apollo.
- Add authorization params to subscription connection.
- Implement feature to only observe the new updates to the data.
- Implement feature to fetch already existing data and subscribe for updates.
