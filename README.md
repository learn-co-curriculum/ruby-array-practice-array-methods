# Array Overview

## Objectives

1. Understand the purpose of arrays
2. Learn to create and populate arrays
3. Learn to manipulate arrays and start getting comfortable with the Ruby documentation on arrays
4. Learn to retrieve data from arrays

##What is an Array?

An array is just a list in your computer. It is a way for your program to store data in list form. Arrays can contain any data types in any combination––strings, ingegers, other arrays, hashes, etc. 

Arrays consist of comman separated values, enclosed in brackets: 

`["hi", 1, "I", 42.3, "am", true, "an", 3, "array"]`

## Creation

There are a few different ways to make a new array. You can use the literal constructor or the class constructor. 

**The Literal Constructor:**

```ruby
my_array = []
```
**The Class Constructor:**

```ruby
my_array = Array.new
#  └── []
```

To make an array that isn't empty, you can separate each item, known as an element, by a `,` and wrap all the elements in brackets, `[]`.

```ruby
puppies = ["bulldog", "terrier", "poodle"]
#  └── ["bulldog", "terrier", "poodle"]

random_numbers = [ 2, 5, 6, 8, 30050]
#  └── [ 2, 5, 6, 8, 30050]

mixed = ["this", "array", 7, 20, "has", 45, "integers", "&", "strings", 309]
#  └── ["this", "array", 7, 20, "has", 45, "integers", "&", "strings", 309]
```

## Manipulating Arrays

If an array is a storage container for a list of data, we can imagine needing to adding items to and remove item from it. There are a number of ways to do both of these. 

###Adding Items to an Array

**Double Shovel Method**

The double shovel method, `<<`, allows you to shovel or add items to the *end* of an array. 

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]

famous_cats << "nala cat"

puts famous_cats.inspect
  => ["lil' bub", "grumpy cat", "Maru", "nala cat"]

```

**The `.push` Method**

Calling `.push` on an array, and giving the push method an argument of the element you want to add to the array, will add that element to the *end* of the array. 

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]

famous_cats.push("nala cat")

famous_cats.inspect
  => ["lil' bub", "grumpy cat", "Maru", "nala cat"]

```

**The `.unshift` Method**

To add an element to the *front* of an array, you can call `.unshift` on it and give the unshift method an argument of the element you want to add. 

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]

famous_cats.unshift("nala cat")

puts famous_cats.inspect
  => ["nala cat, "lil' bub", "grumpy cat", "Maru"]

```
### Removing Items from an Array

**The `.pop` Method**

Calling `.pop` on an array will remove the last item from the end of the array. 

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famout_cats.pop

famous_cats.inspect 
 => ["lil' bub", "grumpy cat", "Maru"]
```

*It is worth noting that the `.pop` method will return the element that you removed. 

**The `.shift` Method**

Calling `.shift` on an array will remove the *first* item from the array. 

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]
famout_cats.shift

famous_cats.inspect
  => ["grumpy cat", "Maru"]
```

*It is worth noting that the shift method returns the element that you have removed. 

### Operating on Arrays

There are a number of other methods available for manipulating arrays. You can learn more about them [here](http://ruby-doc.org/core-2.2.0/Array.html), but we'll look at just a few examples together. 

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]

famout_cats.sort
  => ["grumpy cat", "lil' bub", "Maru"]
  
famous_wizards = ["Dumbledore", "Gandalf"]

famous_wizards.reverse
  => ["Gandalf", "Dumbledore"] 
```

We can also ask an array if it contains a certain element with the `.include` method. 

```ruby
famous_cats = ["lil' bub", "grumpy cat", "Maru"]

famous_cats.include?("Garfield")
  => false

famous_cats.include?("Maru")
  => true
```

***A Note on Iteration***

One of the most common operations you'll be preforming on arrays is that of iteration. Iteration is the act of looping over each element of the array and doing something to it (i.e, go over each element of the array and capialize it, for example). We will be learning much more about iteration in an upcoming unit. 

## Retrieving Items from Array

Just like how items in a numbered lists have a number, elements in an array have what's called an index. However, these indexes are always one number less than you might expect. Instead of starting our count at 1, an array's first index is referred to as 0. So, in the following array: 

`["Cheshire Cat", "Puss in Boots", "Garfield"]`

The Cheshire Cat has an index of 0, Puss has an index of 1 and Garfield has an index of 2. 

To retrieve any of these items, we can type the name of the array, followed by the index number of that item, encloesd in brackets, `[]`. 


```ruby
famous_cats =  ["Cheshire Cat", "Puss in Boots", "Garfield"]

famous_cats[1]
#  └── "Puss in Boots"

famous_cats[0]
#  └── "Cheshire Cat"

famous_cats[2]
#  └── "Garfield"

famous_cats[20]
#  └── nil

```

**Finding an element's index**

To discover the index number of an element within an array, we use the `.index` method. Calling `.index` on an array, and giving it an argument of the element whose index you want to learn, will return the index number. 

```ruby
famous_cats =  ["Cheshire Cat", "Puss in Boots", "Garfield"]

famous_cats.index("Puss in Boots")
#  └── 1
```

