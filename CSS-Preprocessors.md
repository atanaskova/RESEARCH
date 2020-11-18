# CSS Preprocessors

A CSS preprocessor is a program that lets you generate CSS from the preprocessor's own unique syntax. 

There are many CSS preprocessors to choose from, however most CSS preprocessors will add some features that don't exist in pure CSS, such as mixin, nesting selector, inheritance selector, and so on. 

These features make the CSS structure more readable and easier to maintain.

CSS Preprocessors are tools that extend the functionality of vanilla CSS by adding a wide variety of logical syntax such as you might see in a normal programming language.

Preprocessors take code written with this new and versatile syntax, and then compile it into traditional CSS that the browser can work with. 

## The 3 most well-known CSS preprocessors are:
- SASS (or SCSS)
- LESS
- Stylus

> *All the three CSS pre-processors, more or less have similar features.*

There are a lot of reasons why CSS preprocessors are a very important tool for front end and full stack developers, particularly those who are working on a large and complex code base.

1. The DRY Principle (Don't Repeat Yourself)

What it means is that a programmer should always strive to avoid rewriting any bit of code within their application. 

This is often solved by taking a piece of code that may have been repeated in the app and turning it into a reusable helper function or variable.

CSS Preprocessors allow you to keep your code DRY because they give you access to things like *variables*, *mixins* and *extends* which allow you to replace repeated css rules with something reusable.

2. Complex Logic

Preprocessors give you access to some logical syntax you would find in your favorite programming language of choice, so that you can create dynamic styling that responds to the output of the logic.

This includes *loops*, *If / Else statements*, and visual *nesting* of CSS rules.

## Primary Features

- Variables

Variables can be created to reuse data multiple times within your stylesheet.

```css

$color-one: #AAF700;
div {
     background-color: $color-one;
}

```

- Nesting

Many programmers probably find it frustrating that you can’t create a nested visual hierarchy of CSS elements that inherit from one another. 

```css

$font-size: 24px;
ol {
    margin: 10px 0;
    li {
        padding: 5px 5px;
    }
}

```

Preprocessors give you this functionality.

- Mixins

Mixins allow you to take a prewritten set of CSS rules and plug it in inside of any CSS element’s styling. 

```css

@mixin hugediv($height) {
     height: $height;
     &:hover {
         background-color: #F5F5F5;
     }
}
#my-favorite-div {
     @include hugediv(900px);
}

```

This is excellent for cutting down on repeated code.

- Extends

Extends let you share the entire list of CSS rules of one element with any other element of your choice. Hence the name “Extends” because elements can extend their full styling to other elements.

```css

.dinosaur-div { 
       background-image: url('https://dino.com/trex.jpg');
       background-repeat: no-repeat;
       background-size: cover;
}
#some-other-div {
       @extend .dinosaur-div;
}

```

- If / Else Statements

Preprocessors give your styling the ability to dynamically alter itself depending on certain conditionals.

```css

$my-variable: true;
@if $my-variable == true {
        $color-one: blue;
} @else {
        $color-one: red;
}

```

- Color Functions

Preprocessors support a wide variety of built in functions for altering a color dynamically.

```css

saturate($color, $amount)
desaturate($color, $amount)
lighten($color, $amount)
darken($color, $amount)
adjust-hue($color, $amount)
opacify($color, $amount) 
transparentize($color, $amount)
mix($color1, $color2, [$amount])
grayscale($color)
complement($color)

```

- Loops

Iteration becomes possible within a preprocessor by using loop syntax.

```css

@for $i from 1 through 100 {
        .content-div#{$i} {
            background-color: darken(blue, 0% + $i);
        }
}

```

- Imports

You can easily combine multiple stylesheets into one without rewriting any code by importing them.

```css

@import "mixins/mixin.scss";
@import "card.css";

```

- Math

Preprocessors allow for arithmetic to be written anywhere within a CSS rule without the need for the calc() function used in vanilla CSS.

```css

my-div {
        width: (100vw / 3);
}

```

