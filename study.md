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
<!-- Two instance methods that both Array and Enumerable share would be 'any?'
andn 'map'. Array would redefine methods included from Enumerable because while they
have similar names and purposes, they handle different portions of the code.
For example: Array method .map's notation indicates the following:
map{|item| block}

While Enumerable's provides:
map{|obj| block}

They're being used for a similar idea, but the information they take is different. Therefore, thats why Array redefined methods included from Enumerable.
 -->
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
<!--
'Length' is sensibly defined on Array and not Enumerable because Enumerable
methods rely on an ordering between numbers in the collection, whereas Array
methods are ordered, integer-indexed collections of any object. This implies that
Enumerable methods dont have a 'length' method because the Enumerable methods
rely on the relative value of each number in the collection. While array methods can
always access these values with the index.
 -->
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
<!-- Enumerables are able to be counted on a one-to-one correspondance. In a similar light, a stream can be thought of as items on a conveyer belt being processed one at a time rather than in large batches. They both have a specified level of grainulinit. However steams are codata ( potentially unlimited ) where as enumerables are not because they can be counted on a one-to-one correspondance rate.   -->
```
