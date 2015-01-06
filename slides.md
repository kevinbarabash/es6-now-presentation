title: YYCjs Slides
output: index.html
theme: theme
controls: false
logo: theme/logo.png

--

# YYC.js Presents:

## An Epic Slide Template

### That totally kicks some ass

#### Kind of like Chuck Norris

##### And Jackie Chan

Maybe even Chris Rock

-- title

# ES6 Today!

-- image

<img src="https://github.global.ssl.fastly.net/images/modules/logos_page/GitHub-Logo.png" width="50%">

# Brought to you by

-- presenter

![David Luecke](http://gravatar.com/avatar/a14850281f19396480bdba4aab2d52ef?s=200)

## David Luecke

* [<i class="fa fa-github"></i> daffl](https://github.com/daffl)
* [<i class="fa fa-twitter"></i> @daffl](http://twitter.com/daffl)

-- presenter

![Kevin Barabash](http://www.gravatar.com/avatar/de8cd250d9fe39b78f1c0f98b718670d.png?s=200)

## Kevin Barabash

* [<i class="fa fa-github"></i> kevinb7](https://github.com/kevinb7)

--

# ES6?

ES6 = ECMAScript 6 = next version of JavaScript

ES6 brings tonnes of exciting new features, some of which you may already be 
familiar with from other languages.  These include:

- new class syntax
- modules
- arrow functions
- (weak)map, (weak)set
- rest parameters
- block scoping
- constants
- ...

--

# Classes

TODO: add badges for ES5 and ES6

    function Shape(color) { ... }
    Shape.prototype.draw = function () { ... };
    
    function Rectangle(color, width, height) { 
        Shape.call(this, color);
        ...
    }
    Rectangle.prototype = Object.create(Shape.prototype);
    Rectangle.prototype.constructor = Rectangle;
    
    Rectangle.prototype.draw = function () { ... };
    Rectangle.redRectangle = function (width, height) { ... };

--

# Classes

    class Shape {
        constructor(color) { ... }
        draw() { ... }
    }
    
    class Rectangle extends Shape {
        constructor(color, width, height) {
            super(color);
            ...
        }
        draw() { ... }
        static redRectangle(width, height) { ... }
    }
    
Static methods are called the same way, `Rectangle.redRectangle(5,10);`.  The
`prototype` is still there if you want to modify the class after defining it.

--

# Getters/Setters

    Object.defineProperty(Rectangle.prototype, "border", {
        get: function () {
            return this.thickness + " " + this.color;
        },
        set: function (value) {
            // parse value and set data members
        }
    });

--

# Getters/Setters

    class Rectangle extends Shape {
        ...
        get border() {
            return this.thickness + " " + this.color;
        }
        set border(value) {
            // parse value and set data members
        }
        ...
    }

--

# Modules

--

# Modules

--

# Binding `this`

    var numbers = [1,2,3,4,...];
    var sum = numbers.reduce(function (total, number) {
        return total + number;
    });
    
    Calendar.prototype.showMonth = function (month) {
        var self = this;
        month.days.forEach(function (day) {
            day.addEventListener("click", function () {
                self.addAppointmentFor(day);
            });
        });
    };

--

# Binding `this`

    var numbers = [1,2,3,4,...];
    var sum = numbers.reduce((total, number) => total + number);
    
    Calendar.prototype.showMonth = function (month) {
        month.days.forEach(day => {
            day.addEventListener("click", () => {
                this.addAppointMentFor(day);
            });
        });
    };
    
Arrow functions automatically bind `this` correctly.  No more `self = this;` or 
`this.method.bind(this);` or `$.proxy(this.method,this);`.  Also, notice the 
lack of `return` statements whent the `=>` points to a single expression.

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
https://status.modern.ie,
https://www.chromestatus.com/features

-- sponsors

# Our Sponsors

![Assembly](img/sponsors/assembly_logo.png)

![Village Brewery](img/sponsors/village_brewery_logo.png)

![Startup Calgary](img/sponsors/startup_calgary_logo.png)

![PetroFeed](img/sponsors/petrofeed_logo.png)

--

# Last Month

* Something awesome
* More awesomeness

--

# Next Month

* Something awesome
* More awesomeness
