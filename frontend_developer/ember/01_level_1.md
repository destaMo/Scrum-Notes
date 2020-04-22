# Ember - level I

## Areas

**Ember Basic Concepts I**
- Application structure
- Ember Object
- Models
- Router
- Route

**Ember CLI**
- Start a new application
- Addons
- Commands
- Application file structure
- Build

**Templates & Helpers**
- Understand the implication that handlebars is not javascript
- Can explain diff between helper and component
- Know how to write helpers
- Know and use helpers
- Conditionals: if, unless
- Lists: each, each-in, else
- Actions: action, mut
- Forms: input, textarea

**Tooling**
- Know how to run / Build ember project (also in production mode)
- Know how to run tests in development (console / browser ) and in CI (Circle CI)
- Know how to use ember inspector
- Know how to debug application
- Know all the packages in package.json
- Know the app structure
- using ember-cli, generators, blueprints

**Routing 1**
 - can explain how the routing works, how router translate path to route, and what is the relation with controller and the template
 - use application, index, wildcard route
 - use nested route and use dynamic segments (router, route)
 - use beforeModel, model, afterModel, redirect hooks

**Components**
- Communication with the outside world: Data Down | Actions Up | Services
- Customize Component:
-    html: splatattributes
- handling actions:
-    component events
-    actions hash / how to access?
- Component Properties: element, elementId
- tracked property
- Component Lifecycle

**Unit Tests**
- can explain when write test for what
- can explain how tests are executed (in: dev / browser / ci)
- skill to write unit tests (utils | helpers)
- use ember-exam
- use ember-cli-coverage

---

## 📦 Ember / Core Concepts

Knows the core concepts and anatomy of every Ember.js application

### 🎓 Learn

- 📗 [Ember.js](https://emberjs.com/)
- 📗 [Ember guides](https://guides.emberjs.com/)
- 📗 [Ember tutorial](https://guides.emberjs.com/release/tutorial/part-1/)
- 📗 [Anatomy of Ember App](https://guides.emberjs.com/release/getting-started/anatomy-of-an-ember-app/)
- 📗 [Models] (https://guides.emberjs.com/release/getting-started/anatomy-of-an-ember-app/#toc_models)
- 📗 [Router and routes](https://guides.emberjs.com/release/getting-started/anatomy-of-an-ember-app/#toc_router-and-route-handlers)

### 🎤 Interview

- Explain basic flow of Ember application
- What is the role of router in Ember application?
- What can be achieved by using routes handlers?
- What is the role of models in Ember?
- What data management libraries can you use instead of the default one?

### 📝 Katas
- Present a finished tutorial application (Optional)

---

## 📦 Ember / Ember CLI

Optimalize your work with Ember CLI in your toolbelt

### 🎓 Learn

- 📗 [Ember CLI](https://cli.emberjs.com/release/)
- 📗 [Basic use](https://cli.emberjs.com/release/basic-use/)
- 📗 [Ember observer](https://emberobserver.com/)
- 📗 [Addons](https://cli.emberjs.com/release/#whatareaddons)
- 📗 [Application file structure](https://cli.emberjs.com/release/basic-use/folder-layout/)

### 🎤 Interview

- How can we install Ember CLI and create a new project?
- What are addons to Ember application? Where can you look for interesting package and how to install it?
- How can you generate a model/component/test by using Ember CLI?
- What will happen after running `ember build`
- What are the differences between `ember test` and `ember test --server`. Which will be better in the development?
- What is the role of file/directory e.g `/template-lintrc.js` or `/vendor`

---

## 📦 Ember / Templates and Helpers

Understand role of templates and helpers in Ember application

### 🎓 Learn

- 📗 [Templates introduction](https://guides.emberjs.com/release/components/)
- 📗 [Lists of elements](https://guides.emberjs.com/release/components/looping-through-lists/)
- 📗 [Conditionals in templates](https://guides.emberjs.com/release/components/conditional-content/)
- 📗 [Helpers](https://guides.emberjs.com/release/components/helper-functions/)

### 🎤 Interview

- How can you display properties in the template
- What should you use to display a label depending on given value?
- Explain a difference between `each` and `each-in`
- Are we able to use multiple helpers together?
- How would you handle an empty state of array in the template?

### 📝 Katas
- Create a helper which will take a raw date object and return formatted date. E.g `11-03-2020`
