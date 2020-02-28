# Junior - level I

This path include some of the requirements from original React lvl 1. They are linked down here.

## Areas

**React**

- [Validating props structure](../react/01_level_1.md#-react--validating-props-structure) (original React path)
- [Structuring the app](../react/01_level_1.md#-react--structuring-the-app) (original React path)
- [Cleaning up on end of component life](../react/01_level_1.md#-react--cleaning-up-on-end-of-component-life) (original React path)
- [Performance](../react/01_level_1.md#-react--performance) (original React path)

**State management**

- [React state and props](../react/01_level_1.md#-state-management--react-state-and-props) (original React path)
- [Redux](../react/01_level_1.md#-state-management--redux) (original React path)

**Forms**

- [Forms](../react/01_level_1.md#-forms) (original React path)
- [Validation](../react/01_level_1.md#-forms--validation) (original React path)

**Testing**

- [Testing](../react/01_level_1.md#-testing) (original React path)
- [Rendering React](../react/01_level_1.md#-testing--rendering-react) (original React path)

**Patterns**

- [Patterns](../react/01_level_1.md#-patterns) (original React path)

**ReactNative**

- [Overview](#-reactnative--overview)
- [Debugging](#-reactnative--debugging)
- [Linking](#-reactnative--linking)
- [Styling](#-reactnative--styling)
- [Navigation](#-reactnative--navigation)
- [Platfom Specific Code](#-reactnative--platform-specific-code)
- [Lists](#-reactnative--lists)


---

## 📦 ReactNative / Overview

You need to know that it is acctualy React Native and thinks like Expo. Should be able to answer questions about pros and const vs native apps.

### 🎓 Learn

- 📗 [ReactNative page](https://facebook.github.io/react-native/)
- 📗 [Expo vs Vanila RN](https://apiko.com/blog/expo-vs-vanilla-react-native/)
- 📗 [Metro](https://medium.com/@rishabh0297/role-of-metro-bundler-in-react-native-24d178c7117e)
- 📙 [More info about RN](https://ideamotive.co/react-native-development-guide/)

### 🎤 Interview

- What is RN and who create it/maintain it?
- What are the advantages of use RN over Native
- What dependencies you need to build and run RN app on iOS and Android
- What is expo? Cons and pros using it?
- What is the metro?

### 📝 Katas

- Setup React Native app (with latest version of library) on Android or iOS (can be simualtors)

---

## 📦 ReactNative / Debugging

I need to check if you know how to debug RN app with usage of React Native DevTools

### 🎓 Learn

- 📗 [Info about debbuging](https://facebook.github.io/react-native/docs/debugging.html#accessing-the-in-app-developer-menu)
- 📗 [React Native Debugger](https://github.com/jhen0409/react-native-debugger)

### 🎤 Interview

- How to turn on debugger on simulator and real device?
- Show me how to inspect element in RN (by clicking on the element inside the app)

### 📝 Katas

- Install React Native Debugger and debbug app by using it

---

## 📦 ReactNative / Linking

From react-native 0.60 linking is easier, however when adding libraries to our project it is important for run for example `pod install`. However, you need to know what is grandle and cocoapods.

### 🎓 Learn

- 📗 [Cocoapods](https://cocoapods.org/)
- 📗 [Gradle](https://stackoverflow.com/questions/16754643/what-is-gradle-in-android-studio)
- 📙 (deprecated) [Linking](https://facebook.github.io/react-native/docs/linking-libraries-ios.html)

### 🎤 Interview

- Why do we need to link?
- What is cocoapods? How to run them?
- What is gradle?

### 📝 Katas

- Add react-navigation to project
- Add react-native-vector-icons to project

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

- Using flexBox create an input with clear icon (x) - components that you can use are `View`, `TextInput`, `Icon` (material vector-icons, check [Linking](#-reactnative--linking))
- `TextInput` and `Icon` should be wrapped with `View` that have some border
- `Icon` should be on the right of `TextInput`
- `TextInput` should have blue background and white text and take all the remaining space

---

## 📦 ReactNative / Navigation

Instead of React Router we have React Navigation that is a leading library in case of navigation in RN community

### 🎓 Learn

- 📗 [Project Homepage](https://reactnavigation.org/)
- 📗 [Crating sample navigation](https://www.youtube.com/watch?v=p_9K0N0yDvU)
- 📙 [Auth Flow](https://reactnavigation.org/docs/en/auth-flow.html)

### 🎤 Interview

- How to navigate from screen to another?
- How to go back?
- Drawer? What it is?
- Show sample navigation structure
- Push vs navigate?
- Other RN alternatives for Navigation

### 📝 Katas

- Show simple stack navigation with at least one back action

---

## 📦 ReactNative / Platform specific code

Sometimes we need to apply code only to iOS or Android platform

### 🎓 Learn

- 📗 [Official Documentation](https://facebook.github.io/react-native/docs/platform-specific-code.html)
- 📙 [Nice Article](https://medium.com/maestral-solutions/react-native-platform-specific-code-e217db5778f)

### 🎤 Interview

- How to use Platform.select to add platform specific styles?
- How to render component conditionaly?

### 📝 Katas

- Using `&&` or tendary render `<Text>iOS it the best</Text>` only on `iOS`

---

## 📦 ReactNative / Lists

Very offen we using virtual list components to render some results from B/E

### 🎓 Learn

- 📗 [Custom ListView](https://medium.com/@benhur.quintino/react-native-creating-a-custom-listview-9cdc2868a6fa)
- 📙 [SectionList height](https://medium.com/@jsoendermann/sectionlist-and-getitemlayout-2293b0b916fb)
- 📗 [FlatList](https://medium.com/sanjagh/how-to-optimize-your-react-native-flatlist-946490c8c49b)

### 🎤 Interview

- Can you say in own words what is virtualization?
- What is diff between SectionList and FlatList?
- What is RefreshControll?
- What prop trigger FlatList rerender?

### 📝 Katas

- Render list of months using FlatList - overy 3rd month should have blue name
