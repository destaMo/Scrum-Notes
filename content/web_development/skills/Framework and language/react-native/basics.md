+++
title = "JavaScript/React Native - Basics"
weight = 1
+++

{{%bubble %}}

**Points:** 2

**Description:** You can build simple Mobile App, that have basic functionalities and user experience. Utilize library responsible for common requirements that normal mobile app should meet.

**Person who successfully completed requirement for given block can:**

- Run React Native application on Android or iOS simulator or device.
- Can debug using ReactNativeDebugger or Flipper, with usage of console statements.
- Can describe why ReactNative can be chosen over other Native/Hybrid solutions
- Can style elements with ease
- Can create simple navigation inside project
- Can manage data with usage of redux
- Can create simple form with Formik
- Can add custom font

**Prerequisites:** 
- [JavaScript's basics](/web_development/skills/framework-and-language/javascript/)
- [Styling 1](/web_development/skills/styling/01_junior_i/)

{{% /bubble%}}

After finishing this course you should be able to run an ReactNative environment with running application, create components, utilize navigation and write test with jest.

## Areas

**Overview**

- Know what ReactNative is
- Can tell advantage of using it over other solutions
- Start a new application
- ReactNative Commands
- Build and Run Metro
- What is a PWA?

**Debugging**

- Can run debugger
- Can inspect element
- Can console log information and show it

**Linking**

- Know concept of linking libraries (and their native implementation)
- Can tell a bit about cocoapods and grandle
- Can link/add new library into project

**Navigation**

- Can implement navigation within app
- Can tell difference between tab and stack navigation
- Can navigate back
- Know what Drawer is

**Redux**

- Know that is a basic flow with redux
- Can configure reducers and actions to mutate data
- Know that data in reducers should be immutable
- Know what is selector is
- Can utilize redux with usage of react-redux hooks

**Lists**

- Knows that components are responsible for rendering Lists
- Know how to re-render this elements and improve its performance

**React Hooks**

- Knows how to use basic hooks
- Knows how to build own custom hooks
- Knows how to mimic old lifecycle methods

**React Styling**

- Knows how to style elements with RN API
- Is aware of limitations that comes with ReactNative styling (these are not CSS)

**Platform specific code**

- Knows how to get information about current platform
- Knows how to write platform specific file implementations for components and utils
- Knows how to use `Plaform.select` to write styles

**Formik basic + basic validation**

- Creates simple create/edit forms
- Create array-like fields
- Validate data inside form
- Display errors of validation

**Testing basic**

- Is able to write simple snap tests
- Is able to write simple integration test
- Is able to write test that checks redux

**Custom Fonts**

- Is able to add custom font into project and use it

---

## 📦 ReactNative / Overview

You need to know what React Native is and what things like Expo are. You should be able to answer questions about pros and cons of react native/expo vs native apps.

### 🎓 Learn

- 📗 [ReactNative page](https://facebook.github.io/react-native/)
- 📗 [Expo vs Vanila RN](https://apiko.com/blog/expo-vs-vanilla-react-native/)
- 📗 [Metro](https://medium.com/@rishabh0297/role-of-metro-bundler-in-react-native-24d178c7117e)
- 📙 [More info about RN](https://ideamotive.co/react-native-development-guide/)

### 🎤 Interview

- What is RN and who creates it/maintains it?
- What are the advantages of using RN over Native
- What dependencies you need to build and run RN app on iOS and Android
- What is expo? Cons and pros using it?
- What is the metro?
- What is a PWA? That does ReactNative allow more than PWA?

### 📝 Katas

- Setup React Native app (with latest version of library) on Android or iOS (can use simulators) - please don't use `expo`!

---

## 📦 ReactNative / Debugging

We need to check if you know how to debug RN app with usage of React Native DevTools or Flipper (choose one, Flipper should work out-of-box in latest RN)

### 🎓 Learn

- 📗 [Info about debbuging](https://facebook.github.io/react-native/docs/debugging.html#accessing-the-in-app-developer-menu)
- 📗 [React Native Debugger](https://github.com/jhen0409/react-native-debugger)
- 📗 [Debugging with Flipper](https://callstack.com/blog/debugging-with-flipper/)
- 📗 [Flipper tutorial video](https://www.youtube.com/watch?v=qsaNOILmSXw)

### 🎤 Interview

- How to turn on debugger on simulator and real device?
- Show me how to inspect element in RN (by clicking on the element inside the app) and change one of the props

### 📝 Katas

- Install React Native Debugger (or Flipper) and debug app by using it

---

## 📦 ReactNative / Linking

Since react-native 0.60 linking is easier, however when adding libraries to our project it is important to run `pod install`. Moreover, you need to know what **gradle** and **cocoapods** are.

### 🎓 Learn

- 📗 [About linking and setting up autolinking](https://callstack.com/blog/automate-dependency-management-with-autolinking/)
- 📗 [Cocoapods](https://cocoapods.org/)
- 📗 [Gradle](https://stackoverflow.com/questions/16754643/what-is-gradle-in-android-studio)

### 🎤 Interview

- Why do we need to link?
- What is cocoapods? How to run them?
- What is gradle?

### 📝 Katas

- Add react-navigation to project (check documentation to add all the required libs)
- Add react-native-vector-icons to project

---

## 📦 ReactNative / Navigation

Instead of React Router we have React Navigation that is a leading library in case of navigation in RN community

### 🎓 Learn

- 📗 [Project Homepage](https://reactnavigation.org/)
- 📗 [Crating sample navigation](https://www.youtube.com/watch?v=28Xr22XDcDg)
- 📙 [Auth Flow](https://reactnavigation.org/docs/en/auth-flow.html)

### 🎤 Interview

- How to navigate from one screen to another?
- How to go back?
- Explain what is "Drawer"?
- Show sample navigation structure
- Push vs navigate?

### 📝 Katas

- Create tab navigation with three tabs - Habits, Todos, Settings
- Create screens for adding/editing habits and todos (can be empty for now)

---

## 📦 ReactNative / Redux

Knows how to use Redux data management.

### 🎓 Learn

- 📗 [Redux introduction](https://redux.js.org/introduction/getting-started)
- 📗 [Immutability](https://hackernoon.com/functional-programming-paradigms-in-modern-javascript-immutability-4e9751ca005c)
- 📗 [Redux devtools](https://github.com/reduxjs/redux-devtools)
- [Redux hooks](https://react-redux.js.org/api/hooks)
- [Why we should avoid mutation](https://stackoverflow.com/questions/37531909/redux-why-is-avoiding-mutations-such-a-fundamental-part-of-using-it)

### 🎤 Interview

- What is Redux?
- What is the use case(s) for Redux?
- What is action, reducer, selector?
- Can you mutate redux store data? Why?
- How Redux devtools can support you with debugging/development?

### 📝 Katas

- Config redux devtools (or Flipper redux devtools) within app
- Implement Habits and Todos Reducers - both with add/edit/remove actions
- Connect them to Habits and Todos Screens using react-redux hooks
- Create CompletedHabitsPerDay reducer where you will keep ids of completed habits per day
- upon completing habit we should put its id into CompletedHabitsPerDay for today and increase its `series` counter by one
- habits should have `difficulty` value 0-5 that will inform how difficult is to complete this habit
- Todos have only completed flag
- create selector that will only display completed Todos
- create selector that will display all the habits for current day with flag that inform if habit was completed today with usage of data from CompletedHabitsPerDay
- setup redux-persist - to keep data inside an app

---

## 📦 ReactNative / Lists

You need to know how to render virtual list component from Backend

### 🎓 Learn

- 📗 [Custom ListView](https://medium.com/@benhur.quintino/react-native-creating-a-custom-listview-9cdc2868a6fa)
- 📗 [FlatList](https://medium.com/sanjagh/how-to-optimize-your-react-native-flatlist-946490c8c49b)
- 📙 [SectionList height](https://medium.com/@jsoendermann/sectionlist-and-getitemlayout-2293b0b916fb)

### 🎤 Interview

- Can you say in own words what is virtualization?
- What is difference between SectionList and FlatList?
- What is RefreshControl?
- Which prop triggers FlatList rerender?

### 📝 Katas

- Render Habits and Todos inside created screens using FlatList - for now you don't need to style them
- Use selectors that was described in redux section

---

## ReactNative / React Hooks

Developer should use new functional approach to create functional components with usage of React hooks.

### 🎓 Learn

- [How to start](https://medium.com/swlh/how-to-start-with-react-hooks-b8ab723ec048)
- [8 Nice Hooks (can skip useClickInside and useClickOutside)](https://medium.com/better-programming/8-awesome-react-hooks-2cb31aed4f3d)

### 🎤 Interview

- How to get/keep previous value of useState hook?
- What when method what is returned by useEffect is called?
- How to increment useState value by one - present both ways
- Where to keep timeout id returned by setTimeout? And how to clean it, where?

### 📝 Katas

- Create [Switch](https://reactnative.dev/docs/switch) inside Habits view that will display only unfinished habits for this day (it will decide that selector use as data)

---

## 📦 ReactNative / Styling

I need to know that you are able to style components, by using original ReactNative StyleSheets or StyledComponents

### 🎓 Learn

- 📗 [StyleSheets Cheat Sheet](https://github.com/vhpoet/react-native-styling-cheat-sheet)
- 📗 [FlexBox](https://facebook.github.io/react-native/docs/flexbox)
- 📗 [get height/width of screen](https://medium.com/mindorks/everything-to-know-about-styling-in-react-native-7e30aed53ad)
- 📙 [StyledComponents](https://www.styled-components.com/)

### 🎤 Interview

- How to apply styles to components?
- Why we use array as styles? Why you should consider using flatten when applying styles? (tricky one, answer is not required)
- How to get height / width of screen?

### 📝 Katas

- Create )floating Plus button)[https://material.io/components/buttons-floating-action-button] in bottom right of the screens with TouchableOpacity
- Create components to display Habits that will display habit description and difficultly (with usage of some vector icons)
- Both Habit and Todo components that will be displayed by FlatList should have touchable checkbox that represent if task is completed - it should have empty and present state
- Completed task/habit should have gray version that represent completion
- Each habit/task should have edit icon/button that will take us to edit view

---

## 📦 ReactNative / Platform specific code

You need to know how to apply platform-specific code (to iOS or Android platform)

### 🎓 Learn

- 📗 [Official Documentation](https://facebook.github.io/react-native/docs/platform-specific-code.html)
- 📙 [Nice Article](https://medium.com/maestral-solutions/react-native-platform-specific-code-e217db5778f)

### 🎤 Interview

- How to use Platform.select to add platform specific styles?
- How to render component conditionally?

### 📝 Katas

- Inside Settings render information about current platform (if this it iOS or Android) - `${platform} is the best!`

---

## ReactNative / Formik basic + basic validation

As a best practice we use Formik as a library that handle form management. Developer should be able to use it and know how it works.

### 🎓 Learn

- 📗 [Formik](https://github.com/jaredpalmer/formik)
- 📗 [Formik with ReactNative](https://formik.org/docs/guides/react-native)
- 📗 [Creating and Validationg React Native forms with Formik](https://blog.jscrambler.com/creating-and-validating-react-native-forms-with-formik/)

### 🎤 Interview

- What are the differences between create and edit forms? How do you handle them?
- Where is an information about errors and touched inputs when using Formik?
- What is a library we use to validation in formik? How to write own validation function?

### 📝 Katas

- Create form for create and edit todos and habits
- Create tags field inside habit that is an array of strings (user can remove or add any)
- Create validation for Habit form (name should be present and have at least 3 chars)

---

## ReactNative / Testing basic

Everyone that is using React Native should be able to write simple integration (Component), util or snapshot test.

- 📗 [ReactNativeTestingLibrary](https://github.com/callstack/react-native-testing-library)
- 📗 [ReactNativeTestingLibrary + Jest](https://www.youtube.com/watch?v=CpTQb0XWlRc)

### 🎤 Interview

- What is snapshot test? What can they detect?
- Where we can place Jest config (what files)?

### 📝 Katas

- Setups specs and run specs (can be problematic because of Navigation, feel free to reach me in case of troubles)
- Write specs that checks if your implementation of components that display Habit entry - check if it runs proper redux action upon clicking into check and if it is displaying right when there is a different difficulty

---

## ReactNative / Custom Fonts

- 📗 [Add Custom Fonts](https://dev.to/aneeqakhan/add-custom-fonts-in-react-native-0-63-for-ios-and-android-3a9e )
- 📙 [Ultimate Guide to Use fonts in ReactNative](https://medium.com/@mehrankhandev/ultimate-guide-to-use-custom-fonts-in-react-native-77fcdf859cf4 )

### 📝 Katas

- Add [Dancing Script Font](https://fonts.google.com/specimen/Dancing+Script) into project and make Habit's name use that font
