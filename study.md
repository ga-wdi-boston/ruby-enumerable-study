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
I chose these methods to study because they are used in other languages as well, so I thought it would be important.
.map
using map on an array will map a function (that you define within it) and apply it to each element of the array. This will create a new array with these new values. The difference between using an array or an enumerator is the syntax (map{|item|block} -> new array) vs (map{|object| block} -> array)

.collect
also goes through each element of the array and redefines it depending on what function you put inside.

Looks like the difference between array and enumerable is how you use them. Array takes in an item where enumerable will take in an object. WIth an array, each item will be separated, acted upon, and then brought back to define a new array but for enumerable, the object you define is just placed inside the array in each place.



```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
with an array, length will return the number of elements in that array, including zero if there are no elements. length cannot be defined with enumerable but it wouldn't make sense. You cannot place length inside each element of the enumerable object the same way you can count the length of an array by counting each element.
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
streams process items one at a time, similar to enumerable, functions don't operate on them as a whole but affect each object.
```
