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
.collect - I found it interesting that both methods are fairly similar. Execpt Array has a bit more structure, and before using .collect there needs to be a created array. Enumerable has more freedom, the method uses a count and collects the provided enumerator in ("").
Array: city = [ "Boston", "Tokyo", "Bangkok", "Paris" ] <!--Array city is created with cities-->
city.collect { |x| x + "!" } <!--takes the item |x| from the pipes and executes the block x + "!" which creates a new array #=> ["Boston", "Tokyo", "Bangkok", "Paris"] -->

Enumerable: (1..5).collect ("dog") <!--Returns a new array by executing the block once for each element in the enum #=> ["dog", "dog", "dog", "dog", "dog"]-->

.find_index - Index has a bit more structure in array where the index needs an array to locate an index. Enumerable uses (1..5) and it'll count 1-5 and return the index of the selected value. Both methods also share similar {} logic.
Array = .index{ |item| block} #=> int or nil
Enumerable = .find_index { |obj| block} #=< int or nil

Array: city = [ "Boston", "Tokyo", "Bangkok", "Paris" ] <!--Array city is created with cities-->
city.index("Boston") <!--Returns the index of Boston #=> 0 -->

Enumerable: (1..100).find_index(5) <!--finds the index of 5 #=> 4 -->


```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
Arary indexes start at 0 and a negative index is assumed to be at the end of the array. Unlike Enumerables where negative numbers are counted in reverse.
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Streams uses searching methods like enumerables. Both are a collection of data. Enumerables use maps and lists operations while stream supports lazy operation.
```
