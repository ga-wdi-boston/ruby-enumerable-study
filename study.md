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
- any
- collect
- (count)

- cycle = for enumerable: prevents original elements from being alerted, after
the inital interaction, during successive interactions with the block

- drop
- drop_while
- find_index
- first
- include?
- map
- reject
- reverse_each
- select
- sort
- take
- take_while

- to_a = for enumerable: creates a new array which contains the values of
enumerable

- to_h
- zip

The enumerable methods generally include an extra step, which protects the
original elements from being altered. When Array describes the method, the
'protective' step is left out.

resources:
http://ruby-doc.org/core-2.3.0/Array.html
http://ruby-doc.org/core-2.3.0/Enumerable.html
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
Array has a defined length, even if it's not explicitly spelled out. Enumerable
could theoretically never end, so a length can't be determined.

resources:
http://stackoverflow.com/questions/28839037/why-does-enumerable-not-have-a-length-attribute-in-ruby
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Streams, like enumerables could be infinite. But all of an enumerable's data is
available at the same time, where a stream's data is provided in chunks over time.

resources:
https://en.wikipedia.org/wiki/Stream_%28computing%29
```
