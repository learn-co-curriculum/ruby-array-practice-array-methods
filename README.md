---
tags: readme
language: ruby
resources: 0
track: web development
topic: ruby
unit: arrays
lesson: overview
---

# Array Overview

## Introduction

* An array is just a list in your computer.
* Arrays allow us to store information. They can contain, amoung other things: strings, integers, other arrays, objects or hashes (we'll talk about these last two later).

## Creation

* There are a couple different ways to make a new array.

```ruby
my_array = Array.new
#  └── []
my_array = []
#  └── []
```

* To make an array that isn't empty, you can separate each item, known as an elements, by a `,` and wrap all the elements in brackets, `[]`.

```ruby
puppies = ["bulldog", "terrier", "poodle"]
#  └── ["bulldog", "terrier", "poodle"]

random_numbers = [ 2, 5, 6, 8, 30050]
#  └── [ 2, 5, 6, 8, 30050]

mixed = ["this", "array", 7, 20, "has", 45, "integers", "&", "strings", 309]
#  └── ["this", "array", 7, 20, "has", 45, "integers", "&", "strings", 309]
```

## Manipulation

* To add items to an array, you can use the double-shovel method, `<<`, where the array name goes on the left side and the item you'd like to add goes on the right.

```ruby
famous_cats = ["Cheshire Cat", "MoonCat", "Puss in Boots"]

famous_cats << "Garfield"
puts famous_cats.inspect
#  └── ["Cheshire Cat", "MoonCat", "Puss in Boots", "Garfield"]
```

## Retrieval

* Just like how items in a numbered lists have a number, elements in an array have what's called an index. However, these indexes are always one number less than you might expect. For instance, the third element in an array, like `"Puss in Boots"` above, has an index of 2. To retrieve "Puss in Boots" from the array, you simply write the name of the array followed with the element's index in brackets.

```ruby
famous_cats =  ["Cheshire Cat", "MoonCat", "Puss in Boots", "Garfield"]

famous_cats[2]
#  └── "Puss in Boots"

famous_cats[0]
#  └── "Cheshire Cat"

famous_cats[3]
#  └── "Garfield"

famous_cats[20]
#  └── nil

```
