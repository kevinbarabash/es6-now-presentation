title: YYCjs Slides
output: index.html
theme: theme
controls: false
logo: theme/logo.png

-- title

# YYC.js Presents

-- title

# ES6 Now!

-- presenter

![Kevin Barabash](img/iambuildingaworldforyou.gif)

## Kevin Barabash

- [<i class="fa fa-github"></i> kevinb7](https://github.com/kevinb7)

--

# Agenda

- What is ES6?
- ES6 in action (demo)
- Status of ES6
- Tooling
- Gotchas
- Questions

--

# ES6?

ES6 = ECMAScript 6 = next version of JavaScript

ES6 brings tonnes of exciting new features, some of which you may already be 
familiar with from other languages.  These include:

- string templating, multi-line strings
- default, rest paramters, destructuring assignment
- arrow functions
- new class syntax and modules
- (weak)map, (weak)set
- constants, block scoping via "let" keyword
- ...

--

# Demo

<a href="http://kevinb7.github.io/es6-playground"><img src="img/es6-playground.png"></a>

--

# Status of ES6

Currently, most browsers fully support ES5.  All the major browser vendors are
working on implementing various parts of ES6.

Browsers (by number of features implemented):

- IE Tech Preview: 70%
- Firefox 36: 67%
- Chrome 40: ~56%
- Safari 8: 23%

Source: [Kangax ES6 Compatability table](http://kangax.github.io/compat-table/es6/)

More info:
[modern.ie](https://status.modern.ie),
[Chromium Dashboard](https://www.chromestatus.com/features)

-- title

# But I want it now!

--

# Transpilers

- TypeScript (8%)
- es6-shim (23%)
- Closure Compiler (27%)
- ES6 Transpiler (27%)
- Traceur (60%)
- 6to5 (77%)

Source: [Kangax ES6 Compatability table](http://kangax.github.io/compat-table/es6/)

--

# 6to5

<a href="http://6to5.org"><img src="img/6to5homepage.png"></a>

--

# 6to5 gotchas

- output for classes could be more readable/performant<br>
  __solution__: use the "loose: classes" option
- some features require a polyfill (25 KB)<br>
  __solution__: include regenerator and/or core-js custom build
- helper functions added at the start of every file<br>
  __solution__: use the "runtime: true" option and manually add runtime.js (2 KB) to your bundle
- comments don't appear where they should in output code<br>
  __solution__: run your doc generator on the ES6 source
  
--

# What about...

- linting?
- your favorite minifier, bundler, etc.?
- editor support?
- testing?
- debugger? source maps

--

# Demo

link: https://github.com/kevinb7/es6-browserify-example

-- title

# Questions

-- sponsors

# Our Sponsors

![Assembly](img/sponsors/assembly_logo.png)

![Village Brewery](img/sponsors/village_brewery_logo.png)

![Startup Calgary](img/sponsors/startup_calgary_logo.png)

![PetroFeed](img/sponsors/petrofeed_logo.png)
