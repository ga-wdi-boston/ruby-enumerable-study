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
Two instance method names that both Array and Enumerable share
are map and select. Array redefines methods included from
Enumerable because Array is a kind of like a subtype of the Enumerable class. Array itself is an enumerable but there are also other types of enumerables, for instance hashes. Iterating over an array is potentially different from iterating over a hash. Map is very similar in both Array and Enumerable but Select is different depending on what is being iterated over. If one is iterating over a range or array its basically the same but if one is iterating over a hash Select returns another hash object instead of an array.
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
This is a guess: Its because length could mean different things when applied to a hash (if it has keys with multiple values such as an array or another hash) but when applied to an array or range the returned results are more concrete.
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Streams are similar to Enumerables because in both instances items in enumerables when interated over and items in a stream are processed one at a time. They are different because hashes, ranges, and arrays are finite whereas Streams are potentially infinite. 
```
