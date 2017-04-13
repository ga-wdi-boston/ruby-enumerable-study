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

One shared instance method is select.  For an array, a new array is returned and a block returns a true value.  For an enumerable, the select instance method operates on a hash instance.  Although select acts similarly for both arrays and enumerables, it will return a hash object when it is operated on by a hash.

Another shared instance method is reject.  For both arrays and enumerables, the reject instance method reutrns an array.  However, it appears that the array instance method returns a new array at the end, rather than the original array.

```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
Source: http://stackoverflow.com/questions/28839037/why-does-enumerable-not-have-a-length-attribute-in-ruby

According to the above source, while length and count appear to complete the same task, they are different in how they execute the method.  With enumerables, the data structure is not immediately known and accessible.  While arrays have a predetermined length, enumerables only determine length by actually enumerating through the data.  Therefore, the enumerable value cannot return a value immediately and it is given a different name than length.

```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md

Streams can be thought of as an alterative to enumerables.  Streams support lazy operations (whereas enumerables are eager).  By lazy, I mean the category of non-enumerables where operations do not require the generation of intermeidate lists until achieving a result.  Another difference regards purpose of streams and enumerables.  Because enumerables, like count, cannot be predetermined, they are ill suited for infinite data (see question above).  It is for this reason taht streams are a better option when working with large data sets.

```
