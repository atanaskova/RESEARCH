# BEM (Block Element Modifier)

BEM stands for Block Element Modifier and it is a methodology developed by the folks at [yandex](https://yandex.com/) in the year 2009. The idea behind BEM is to divide the user interface into **independent blocks**.

This makes interface development easy and fast even with a complex UI, and it allows reuse of existing code without copying and pasting.

BEM is an abbreviation of the key elements of the methodology — Block, Element and Modifier.

### 1. Block

Standalone entity that is meaningful on its own.

The block name should describe its purpose not what the element looks like nor how it behaves.

- The block shouldn't influence its environment, meaning you shouldn't set the external geometry (margin) or positioning for the block.

- You also shouldn't use CSS tag or ID selectors when using BEM

- Blocks can be nested in each other.

- You can have any number of nesting levels.

*Examples:*

*header, container, menu, checkbox, input*

### 2. Element

A part of a block that has no standalone meaning and is semantically tied to its block.

Can't be used separately from it. You can think of an element like a mother—child relationship.

The element name is separated from the block with a double underscore. (__).

- Elements can be nested inside each other.

- You can have any number of nesting levels.

- An element is always part of a block, not another element.

*Examples:*

*menu item, list item, checkbox caption, header title*

### 3. Modifier

A flag on a block or element. Use them to change appearance or behavior.

The modifier name is separated from the block or element name by a single underscore (_) and it can not be used alone as we'll demonstrate briefly.

- Used when only the presence or absence of the modifier is important, and its value is irrelevant.

- Used when the modifier value is important.

*Examples*

*disabled, highlighted, checked, fixed, size big, color yellow*

## Benefits

- **Modularity**

Block styles are never dependent on other elements on a page, so you will never experience problems from cascading.

You also get the ability to transfer blocks from your finished projects to new ones.

- **Reusability**

Composing independent blocks in different ways, and reusing them intelligently, reduces the amount of CSS code that you will have to maintain.

With a set of style guidelines in place, you can build a library of blocks, making your CSS super effective.

- **Structure**

BEM methodology gives your CSS code a solid structure that remains simple and easy to understand.

>The reason I choose BEM over other methodologies comes down to this: it is less confusing than the other methods (i.e. SMACSS) but still provides us the good architecture we want (i.e. OOCSS) and with a recognizable terminology.

> -Mark McDonnell, Maintainable CSS with BEM