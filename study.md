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

Please read the google definition of enumerable, the _description_ of the Ruby
Array Class (the part before [Creating
Arrays](http://ruby-doc.org/core-2.3.0/Array.html#class-Array-label-Creating+Arrays)),
the _description_ of the Ruby Enumerable Module (the part before **Public
Instance Methods**), and the _overview_ of the List ADT at Wikipedia (the part
before the Contents block).  Also, please read through the list of method names
in the **Methods** block on the left side of [Ruby Array
Class](http://ruby-doc.org/core-2.3.0/Array.html) and [Ruby Enumerable
Module](http://ruby-doc.org/core-2.3.0/Enumerable.html).  Note that Enumerable
is listed as an **Included Module** for Array.

## Methods on Array and Enumerable

List at least two instance method names (other than `count`) that Array and
Enumerable share. An included module provides behavior to instances of the
including class. Why might Array redefine methods included from Enumerable?
Please give reasons for the methods you list.

```md
I'm not completely sure, but my best guess is that Array redefines some methods
that are included from Enumerable because it gets rid of the need for it to also
use the each method. The Enumerable methods require the class to have an each
method that's used to pass each element to the provided block. Two examples of
method names that are shared between Array and Enumerable are:
1. include? - the Enumerable version checks to see if any member of enum is equal to obj whereas the Array version, checks against self.
2. to_a - I thought this one was interesting.  The Enumerable version returns an array containing the items in enum wheras the Array one just returns self. The Array version can also be called on a sub-class of Array, it converts that sub-class to an Array object.

Resources:
http://ruby-doc.org/core-2.3.0/Array.html
http://ruby-doc.org/core-2.3.0/Enumerable.html
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
An Array has a length because it already has a defined size.  The Enumerable methods are reliant
on the class to use it's each method to provide it one element at a time so it doesn't
have a set size from the start.  It can count the number of items passed through though.
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
I really like the analogy used in the wikipedia article: "A stream can be thought of as items on a conveyor belt being processed one at a time."  Similarly, enumerables are intaking one element at a time and processing them.  I think
the biggest difference is that where a stream may potentially be unlimited, an enumerable will always end when the
collection ends.

Resources:
https://en.wikipedia.org/wiki/Stream_%28computing%29
http://ruby-doc.org/core-2.3.0/Enumerable.html
```
