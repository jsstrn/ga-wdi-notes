# Notes

## Schedule

- Week 1
- Week 2
- Week 3 - Project: Build a game in the browser
- Week 4
- Week 5
- Week 6 - Project: Build a simple Ruby on Rails web app with sign up/log in
- Week 7
- Week 8
- Week 9 - Project: Build a NodeJS web app with NoSQL database (Group Work)
- Week 10
- Week 11
- Week 12 - Project: Your final project
- Week 13 - Meet and Greet

## Resources

- iDoneThis https://idonethis.com/
- Events aggregator http://webuild.sg/
- Front-end; TLDR http://feds.strikingly.com/
- Module Counts http://www.modulecounts.com/
- npm search http://npmsearch.com/
- DevFest Asia http://2015.devfest.asia/
- Node School http://nodeschool.io/
- W3C CSS3 Selectors http://www.w3.org/TR/css3-selectors/
- 147 Colors http://www.colors.commutercreative.com/grid/
- CSS Specificity Calculator http://specificity.keegan.st/
- Can I Use http://caniuse.com/
- Flexbox https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- View HTML pages on GitHub with https://htmlpreview.github.io/
- Idempotence https://en.wikipedia.org/wiki/Idempotence

## Books

- The Hard Thing About Hard Things http://www.amazon.com/The-Hard-Thing-About-Things/dp/0062273205
- Zero to One http://www.amazon.com/Zero-One-Notes-Startups-Future/dp/0804139296

## Terminal

- traceroute -- traces the route taken to get a URL
- curl -- a browser for the terminal
- find -- lists files and directories in a tree display
- grep -- search for specific words in a file
- \*\*/\*.txt -- a way to get all files of a specific file type

## Common Git commands

- `$ git status` -- check the status of your local git repo
- `$ git add <filename>` -- add file(s) to the staging area
- `$ git commit -m "Your message"` -- commit your file to the local repo
- `$ git push origin master` -- push the commit to the remote master branch
- `$ git pull origin master` -- pull changes from a remore master branch
- `$ git remote` -- check for remote repos
- `$ git remote add origin <HTTPS URL>` -- add an existing remote repo 
- `$ git checkout <branch>` -- switch to another branch
- `$ git checkout -b <new branch> <existing branch>` -- create a new branch from an existing branch

## Vim commands

- Type i to enter insert mode
- Type Esc to exit insert mode
- Type : to enter command mode
- In command mode, enter 
  - Type w for write (save)
  - Type q for quit
  - You can also chain commands, type :wq to do all the above at once
  
## CSS

- margin is spacing outside of the border in the box model
- padding is spacing inside of the border in the box model 
- `display: inline` -- inline will collapse the margin-top and margin-bottom
- `display: inline-block` -- inline-block retains the margin-top and margin-bottom

## JavaScript

- `arr.map(callback)` -- method creates a new array with the results of calling a provided function on every element in this array
- `arr.forEach(callback)` -- method executes a provided function once per array element
- `0.1 + 0.2 === 0.3` evaluates to `false` in JavaScript, it evaluates to `0.30000000000000004`
- parameters is what you pass into functions when you call them (e.g. `bar(123)`)
- arguments is what you put when you're defining a function (e.g. `function bar(myArg) {}`)
- Methods `Array.some()`, `Array.every()`, `String.filter()`, `Array.map()`
- install on every directory 
 - `npm init`
 - `npm install standard` -- a JS linter
 - `npm install babel-cli` -- a JS transpiler (translates and compiles) for ES6 to ES5 for compatibility
 - create `.gitignore` file to ignore `node_module/` and `.DS_Store` in your git repo
- [Ternary operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator): `condition ? statement_if_true : statement_if_false`
- DOM https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model

### Running an HTTP Server
- Open Terminal and type `npm install http-server` -- installs http-server to a specific directory
- Then run `./node_modules/.bin/http-server` -- runs the http-server
- Go to the IP address as stated in the Terminal (typically `http:127.0.0.1:8080`)
- More [info](https://www.npmjs.com/package/http-server)
- ALternatives to GitHub Pages, https://surge.sh/

### NodeSchool.io
- JavaScripting
 - Install `npm install -g javascripting` 
 - Run `javascripting`
- Functional Javascript Workshop
 - Install `npm install -g functional-javascript-workshop`
 - Run `functional-javascript-workshop`
 
### Animations in JavaScript
- `var timerID = setTimeout(func, delay)`
- `var timerID = setInterval(func, delay)`
- `clearTimeout(timerID)`
- `clearInterval(timerID)`
-  `requestAnimationFrame(func)` -- better for animations
