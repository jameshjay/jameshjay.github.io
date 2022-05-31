---
layout: default
title: • Swift - Arrays
parent: Reference Guides
grand_parent: 
nav_order: 1
description: "Arrays reference guide"
permalink: /swift-arrays/
image: 
author: James H. Jay
---

```
📌 Update in progress
```

### Swift Programming 
{: .no_toc }

Xcode
{: .label .label-blue }

iOS
{: .label .label-purple }

# Arrays 
{: .no_toc }

## What we'll learn:
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## What are arrays?

Arrays are the most commonly used data types in programming. You use arrays when you want to organize a collection of values of the same data type.
Values could be of any data type – from integers, strings to objects.

### Syntax 
{: .no_toc }

```swift 
var arrayName: [type] = [value, value, value]
```

---

## Create an Array 

### Create an Empty Array 
{: .no_toc }

To create an empty array, specify the data type in your array declaration.
We can create an array in two ways:

```swift
//option 1
var numbers: [Int] = []

// option 2
var colors = [String]()
```

### Create an Array of String Elements 
{: .no_toc }

To create an array with integer elements, surround your values with an enclosing and closing bracket separated by commas.

```swift
var colors: [String] = ["blue", "green", "red"]
```

---
<h2 style="color: #9464D6">{ Access or Insert }</h2>

### Access an Array

To access a specific element of an array, address your array name followed by a subscript with the index position of the value you want to retrieve. 

Any value outside of the index rage will result in an error. 

```swift
//access element at index 1
colors[1]

print(colors[1])
// prints green
```

### Append value in an Array

appending value will be added to the end of the array

```swift
// Use the assign equals operator (+=) to append the string "purple" to the colors array.
colors += ["purple"]
```

The appending signature is equivalent to:

```swift
// same as the code above 
colors = colors + ["purple"]
```

### Insert Value at specific index of an Array
{: .no_toc }


Use the `.insert ("_", at:_)` method to insert an element at a specific index. The elements at that index are shifted to make room. 

```swift
// insert "red" at index 1 (note: index starts at 0)
colors.insert("purple", at: 1)
```
---
<h2 style="color: #9464D6">{ Remove Value }</h2>

### Remove Value in an Array

### Remove Value at Specific Index 
{: .no_toc }

To remove elements from a specific index of an array, use the `remove(at: ___)` method.

```swift
// remove value at index 1
colors.remove(at: 1)
```

### Remove the Last Value
{: .no_toc }

If you want to remove the last value of an array, use the `removeLast()` method. 

```swift
colors.removeLast()
```
---
<h2 style="color: #9464D6">{ Change Value }</h2>


### Change the Value in an Array

### Change Value of a Specific Index
{: .no_toc }

```swift
// change the value at index 0
colors[0] = "orange"
```

### Change Range of Values
{: .no_toc }

```swift
// change a range of values
colors[1...2] = ["red", "white", "blue"]
```
---

<h2 style="color: #9464D6">{ Data Types }</h2>


## Data Types and Properties

### Common Data Types
With Swift's type inference, the data type can be removed if default values are given.

```swift
var arrayOfInts: [Int] = [1,2,3,4,5]
var arrayOfStrings: [String] = ["here is one string", "another string", "and another"]
var arrayOfCharacters: [Character] = ["d","f", "g"]
var arrayDoubles: [Double] = [0.1, 0.22, 0.333]
var arrayBool: [Bool] = [true, false, true, true]
```
---

<h2 style="color: #9464D6">{ Array Properties }</h2>

### Count Property 
```swift
//returns number of elements in Array
colors.count
```

### isEmpty Property 
```swift
// returns true or false (boolean value) 
colors.isEmpty
```

### Contains Property 
```swift
// returns a boolean value indicating whether the array contains the given element.
colors.contains("pink)
``` 
<br>

---

<h1><center> You may also like </center></h1>
<div class="row">
    <div class="column_grid">
        <a href="/google-static-api">
            <img border="0" alt="img" src="/assets/images/cards/maps_static.png" width="230" height="450">
        </a>
    </div>
    <div class="column_grid">
        <a href="/swift-variables">
            <img border="0" alt="img" src="/assets/images/cards/var.png" width="230" height="450">
        </a>
    </div>
    <div class="column_grid">
        <a href="/swift-arrays">
            <img border="0" alt="img" src="/assets/images/cards/arrays.png" width="230" height="450">
        </a>
    </div>
</div>