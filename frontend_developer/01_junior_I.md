# Junior - level I

## Areas

**Tools**

- Work environment
- IDE
- Browser tools
- GIT CLI

**Language & Browser API**

- JavaScript Basics
- HTML
- Browser events

**Networking**

- HTTP

**Backend**

- Backend for Frontend developer

**Testing**

- Unit

**Styling**

- Styling (Level I)

**Framework & Libs**

- Framework A Level I

---

## 📦 Tools / Work environment

Know your environment (operating system, terminal, basic command lines, running docker on your machine). Ensure you are able to type with all you fingers, and without looking at the keyboard. Improve your everyday workflow.

### 🎓 Learn

- [MacOS or Linux](/backend_developer/devops/os.md)

---

## 📦 Tools / IDE

Know your editor - below are materials for VSCode, but you can choose other. Ensure you know basic keyboard shortcuts, and you ide / editor is configured in a manner that supports frontend development.

### 🎓 Learn

- 📗 [vscode using & customizing](https://github.com/mike-works/vscode-fundamentals/tree/master/docs) (**Usefull Extensions:** ESLint, Sass, Prettier, Jest)
- 📙 [intro to vim: from chapter: "background", to chapter "save & exit"](https://www.turnkeylinux.org/blog/vim-tutorial)
- 📙 [practice vim](https://www.openvim.com/)
- 📙 [vim emulator from vscode](https://github.com/VSCodeVim/Vim)
- 📙 [install Tab Nine](https://tabnine.com/)
- 📙 [enable semantic completions](https://tabnine.com/semantic)

### 🎤 Interview

- Why do you use linters?

### 📝 Katas

- Walk me through your IDE
    - what features you use the most often
    - how did you configure it
    - what plugins do you use
    - Is there anything unique

---

## 📦 Tools / Browser Tools

Read about how the web works - you do not need to remember all the details, just familiar yourself with the concept, and remember where you can find more. Read the documentation for dev tools - to have a overview about what is possible.

### 🎓 Learn

- 📗 [how the web works](https://github.com/vasanthk/how-web-works)
- 📗 [what web can do today](https://whatwebcando.today/)
- 📗 choose your tool:
    - **Chrome DevTools**
        - 📗 [crash course](https://www.youtube.com/watch?v=x4q86IjJFag)
        - 📗 [official guide](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/) - Home/ Open Dev tools / DevTools for beginners / CSS / JavaScript / Console / Network / HTML
    - **Firefox Developer tools**
        - 📗 [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/)
        - 📗 [Core Tools](https://developer.mozilla.org/en-US/docs/Tools) - Page inspector / Web Console / JavaScript Debugger / Network Monitor

### 🎤 Interview

- What did you learn from the article “how web works”?
- Is there anything interesting your found in the page “what web can do today?”

### 📝 Katas

- How dev tools will help you develop and debug the app? (Inspector / console / debugger / network / break points usage)

---

## 📦 Language & Browser API / JavaScript Basic

Familiarize yourself with the concepts from the book, be able to explain then, and give an example where you would use it. Have a decent skill in writing solutions & tests in javascript.

### 🎓 Learn

- 📗 [Professional Software Developer](https://mixmastamyk.bitbucket.io/pro_soft_dev/intro.html)
- 📗 [5 rules of programming](http://users.ece.utexas.edu/~adnan/pike.html)
- 📗 [Eloquent JavaScript](http://eloquentjavascript.net/) ([our crash course](https://github.com/miksturait/od-zera-do-js-developera))
    - **Optional**
        - [Project: A Programming Language](http://eloquentjavascript.net/12_language.html)
        - [Drawing on Canvas](http://eloquentjavascript.net/17_canvas.html)
        - [Http and the forms](http://eloquentjavascript.net/18_http.html)
        - [Project: Pixlr editor](http://eloquentjavascript.net/19_paint.html)
- 📙 [Introduction to ES6+](https://scrimba.com/g/gintrotoes6)
- 📙 [Introduction to Regulax Expressions](https://scrimba.com/g/gregularexpressions)
- 📙 [regular expresions](http://regexr.com/) as much as you need to practice

### 🎤 Interview

- Software development in general:
  - How you would explain 5 rules of programming in your own words?
  - Why the code needs to be testable? (And how TDD and BDD might help)
  - What kind of feedback loops can be included in the software development process that will improve quality and the speed of the development?
  - How Continues Delivery impact sofware development?
  - Why is beneficial to use Scrum as softwarer development methodology?
  - What is your role in Scrum team and Scrum events?
  - Could you guide me with your own words, through [Joel Spolsky Test](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/)
- JavaScript:
  - Explain differences between JavaScript, EcmaScrpt & TypeScript (high-level)
  - Explain what is scope. What you should avoid in terms of scope?
  - Explain differences between `var`, `let`, `const`
  - Explain `this`
  - Explain the difference between `function` & `arrow function`
  - How the `closure` works
  - Explain modules. How `require` & `import` works?
  - Explain JS hoisting (does it also apply to Class?)
  - Explain the  asynchronous programming
  - What `async` does?
  - Elaborate about examples of built-in higher-order functions

### 📝 Katas

- Solve 5 problems (with tests coverage) from [the list](https://github.com/mre/the-coding-interview/tree/master/problems)

---

## 📦 Networking / HTTP

### 🎓 Learn

- 📗 [HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP)

### 🎤 Interview

- what 2xx tells you?
- what 3xx usually does?
- what 4xx tells you?
- what 5xx tells you?
- What E-tag is responsible for?
- elaborate about HEAD method?
- elaborate about OPTIONS method?
- What DNS is responsible for?
- How would you use cookies in your app?

### 📝 Katas

- Show me how would you access web socket traffic information in the browser

---

## 📦 Backend / Backend for Frontend developer

Developer knows how to run the backend based on the project documentation (it doesn't have to be any specific framework project, but you need to proove that you know how to achieve this)

### 🎓 Learn

- 📗 [rails guide - just learn about the app structure](https://guides.rubyonrails.org/getting_started.html)

### 📝 Katas

- Run your current project backend base on the documentation (it doesn't have to be any specific framework project, but you need to prove that you know how to achieve this)
- RoR example (optional to your current project)
    - install ruby `asdf ruby install 2.6.0 && asdf global ruby 2.6.0`
    - install postgresql `brew install postgresql`
    - fetch rails project `git clone git@github.com:Selleo/selleo-mail-log-api.git`
    - setup the project, based on the readme
    - run the server `bin/rails server`
    - browse the source code (`config/route.rb and app/controllers/**/*.rb`)
    - [run rails project on docker](https://docs.docker.com/compose/rails/)
    - Guide me [through the files of rails app](https://github.com/Selleo/dm3), starting from the endpoint path (eq. `/api/v1/finance/customer-balances`)

---

## 📦 Testing / Unit

### 🎓 Learn

- 📗 [Jest](https://jestjs.io/docs/en/getting-started.html)


### 🎤 Interview

- Explain role of unit tests
- What you should test in unit tests?

### 📝 Katas

- Show example usage of your unit test and describe it
