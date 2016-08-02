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
map
reject
for array reject returns a new array of the  items in self when the given block is not true. The ordering of non-rejected elements is maintained. For enumerable, it is almost the same, except it is an array for all elements of enum for which the given block returns false. In both cases.If no block is given, an Enumerator is returned instead.
zip
With zip:
for enumerable it takes an element from emum and merges it with the other elements from each argument. It creates a sequence of n element arrays. Where N is one more than the count of the arguments. If the size of any of the elements is less than the enumerable size then the values are all nil. If a block is given it is returned as the output of the array,otherwise an array of arrays gets returned. The big difference here is that with array it converts any arguments into arrays then merges the elements of SELF with the elements frome each argument.

There are slight differenciations in these behaviors which would make using them in one definition or another much easier than if there was only one rule/definition to abide by. This way we can implement them with different usages depending on the situation.
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
Length is definied on array but not enumerable because arrays are a list of values, where enumberables are simply collections of classes. Therfore having the definition be in array where we can manipulate the list depending on that length makes much more sense. I
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Both streams and enumerables involves sequences, specifically elements. Usually streams need to be interacted with one at a time instead of in batches. But enumerables are grouped together and can affect more than one element at a time
```
