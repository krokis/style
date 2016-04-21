# Classes

## Names

* Class names must be in **PascalCase**. They cannot contain underscores or any other symbols; only letters and numbers.

  ~~~ coffee
  class foobar  # Bad
  class fooBar  # Bad
  class foo_bar # Bad
  class Foobar  # Bad
  class FooBar  # Good
  ~~~

* Members, including methods, properties and accessors, must be in **camelCase**.

  ~~~ coffee
  class FooBar
    Foobar: ->  # Bad
    foobar: ->  # Bad
    foo_bar: -> # Bad
    fooBar: ->  # Good
  ~~~

## Order of members

* Class members must appear in the following order, according to their nature:

  1. Static accessors
  2. Static methods
  3. `constructor()`
  4. Instance accessors
  5. Instance methods

  Inside each of these five groups, you should try your best to group them by similar functionality. Order them so if one method depends on another, the latter is defined first.
