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
They share 'any?' and 'collect'. Array may redefine methods as it has a greater scope than any given Enumerable, and Enumerable may have more rigid parameters than Array. Both of the methods mentioned work the same way for Array and Enumerable.
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
Enumerable's count method operates very differently. In Ruby's built-in data structures like Array and Hash, length simply retrieves the pre-computed size of the data structure and should always return instantly.

For Enumerable#count, however, there's no way for it to know what sort of structure it's operating on and thus no quick, clever way to get the size of the enumeration (this is because Enumerable is a module, and can be included in any class). Enumerables are not guaranteed to have lengths, and thus the length method does not make sense.
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Both Enumerables and Streams enumerate, meaning they take each item at a time and do something with it. The Enum module is “eager” and will act on data straight away. This works well in most use cases. However, if you need to make a pipeline of transformations on a large dataset, it would be advantageous to use the Stream module. The Stream module will lazily act on the data, creating a stream that represents the function, but without actually acting on it straight away, rather than creating a new list at each step of the process.
```
