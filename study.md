# Ruby Enumerable Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings

-   [Enumerable definition at google](https://www.google.com/#q=enumerable+definition)
-   [Ruby Array Class](http://ruby-doc.org/core-2.3.0/Array.html)
-   [Ruby Enumerable Module](http://ruby-doc.org/core-2.3.0/Enumerable.html)
-   [List ADT](https://en.wikipedia.org/wiki/List_%28abstract_data_type%29)

Please read:
- The google definition of enumerable
- The _description_ of the Ruby
Array Class (the part before [Creating
Arrays](http://ruby-doc.org/core-2.3.0/Array.html#class-Array-label-Creating+Arrays))
- The _description_ of the Ruby Enumerable Module (the part before **Public
Instance Methods**)
- The _overview_ of the List ADT at Wikipedia (the part
before the Contents block)
- The list of method names
in the **Methods** block on the left side of [Ruby Array
Class](http://ruby-doc.org/core-2.3.0/Array.html) and [Ruby Enumerable
Module](http://ruby-doc.org/core-2.3.0/Enumerable.html).
  - Note that Enumerable
is listed as an **Included Module** for Array.

## Methods on Array and Enumerable

List at least two instance method names (other than `count`) that Array and
Enumerable share. An included module provides behavior to instances of the
including class. Why might Array redefine methods included from Enumerable?
Please give reasons for the methods you list.

```md
first - The Array `first` method returns the same thing as the Enumerable `first`
method.

select - The Array `select` method returns the same thing as the Enumerable `select`
method.

References:
http://ruby-doc.org/core-2.3.1/Array.html
http://ruby-doc.org/core-2.3.1/Enumerable.html
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
The Enumerable mixin module can be inherited by different classes (not just
Array).  It may not make sense to have a `length` method defined for these
types of classes (i.e. `hash` class that inherits the Enumberable mixin module).

The Enumerable mixin module uses its `count` method to iterate through.

References:
http://ruby-doc.org/core-2.3.1/Array.html
http://ruby-doc.org/core-2.3.1/Enumerable.html
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Both streams and enumerables are logical sequences of data that can be iterated
through.

Streams can be infinite (and ongoing) sequences of data and enumberables are
finite sequences of data.

Reference:
https://en.wikipedia.org/wiki/Stream_%28computing%29
```
