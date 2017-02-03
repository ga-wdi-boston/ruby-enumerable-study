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
A Enumerable module is found within any class, and they act to group methods and constants.
Array may redifine methods included from Enumerable because the methods are assigned to
objects when used over an Array, whereas Enumerable methods can be used on
anything defined as enumerable, which includes all array values.

With the array find_index method, this method will iterate over an array and
return the index of the first object that is equal to the compared object.
The Enum find_index method being used here could be redefined in this situation
because any number blocks or arguements set as enumerables may not exist within the array,
causing a different response to those parameters.
The take(n) method in an Array will return the first positive number n elememts
from the array.  If a negative number is given an error will result, whereas the take(n) Enumerable method does have that same restriction.
```

## Array#length versus Enumerable#count

Although both Array and Enumerable have a `count` method, Array also defines the
method `length`.  Why is `length` sensibly defined on Array but not Enumerable?

```md
Length is not defined with Enumerables because enumerables only have a set length when
used to create modules set to other classes, like an Array.  The enumerable 'count' method counts from the beginning, so it is still possible for the count to continue without knowing the endpoint.
```

## Compare Enumerable to Stream

Please read the Wikipedia entry for
[Stream](https://en.wikipedia.org/wiki/Stream_%28computing%29).  How are streams
like enumerables?  How are they different?  Please compare and contrast these
types.

```md
Streams are like enumerables in tbat they have data of an undefined length, and in OOP, they can both be used as iterators of objects.  Streams cannot have normal functions operated on them; only filters can, which produce other streams, referred to as pipelines.  Enumerables can have methods operated on them that return only one result or a specific number of results, and then the function ends.  
```
