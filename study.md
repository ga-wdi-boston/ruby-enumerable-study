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
If a class inherits enumberable, one of the requirements is to have method "each". We also need to explicitly include Enumerable like so:

class <class name>
include Enumerable

block of code

end
end

 Enumerable allows iterations inside or/and outside of the class. Once enumberable is defined, we can create new objects, and apply methods on them. New objects are created based on defined enumerable.

Two methods that array and enumberable share are find_index and map method. If block of code isn't provided within the each method, then enumerale is returned.

1. find_index method

Method find_index returns an index of a first object that evaluates as non false when block of code is executed. Returns nil if no match is found.


2. map method

Map method creates a new array containing the values returned by the block.


```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
Enumerable isn't a class. It is a collection of different functionalities that are used by multiple classes. Therefore the length can't be determined ahead of time.

Lenght method is used when length is known and can be returned.

Count method on enumerable can be equivalent to the length. Count tend to be used when length can't be predicted ahead of time and it needs to be computed by iteration.
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Streams are a sequences of data elements that are available over time.

The difference between streams and enumerable is that within streams functions can't operate on a stream as a whole but rather on one item of a stream at the time.

Whereas in case of having enumerables, we can operate on all items at the time.
```
