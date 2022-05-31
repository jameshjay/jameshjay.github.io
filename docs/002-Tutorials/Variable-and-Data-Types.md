---
layout: default
title: • Variabels and Data Types
parent: Tutorials
grand_parent: 
nav_order: 9
description: "What are variables in Swift"
permalink: /swift-variables/
image: 
author: James H. Jay
---

### Swift Programming 
{: .no_toc }

Swift Programming
{: .label .label-green }

Xcode
{: .label .label-blue }

iOS
{: .label .label-purple }

![MCS](/assets/images/var/var_banner.png)

<center> Designed for Absolute Beginners </center> 

# Variables and Data Types
{: .no_toc }

### Variables allow you to store simple information in your code.
{: .no_toc }

```swift
//Variable Syntax Structure 
var name: dataType = value 
```


---
## Learning Objectives
{: .no_toc }

In this lesson, you'll learn:



## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}



---
## What are variables

<details closed>
<summary><strong><code>Video Overview</code></strong></summary>
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/698494455?h=73b3bc708c#t=0m6s&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Variables in Swift _ Part 1"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
</details> 



In programming, you can think of a variable as a container that stores simple data for us.
This container is given a unique name and whenever we want to use that piece of data in our program, we simply refer to the variable name. 

For example:

```swift
var number = 100 
```

The variable `number` stores the integer value 100.

<i> ( We can use Swift's `print` function to view the value stored in `number`)<i>

```swift 
print(number)
// Output: 100
```


---
## How to create variables 

Let's take a quick  look at the syntax structure of creating a variable. 
*(Don't worry if any of this sounds confusing, we'll be going through each part one by one).*


<details closed>
<summary><strong><code>Video Walkthrough</code></strong></summary>
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/698495385?h=9f2b906a12&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Syntax Structure _ Part 2"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
</details>
<br>
#### Here's the basic syntax structure of a variable
{: .no_toc}

```swift
// variable declaration
Var name: dataType = value 
```


Let's break it down piece by piece:

- `var` tells the compiler we are creating a variable: 
```swift
var 
```

- `username` is the unique name we have given our variable
```swift
var username
```

- `:` is our separator that is placed between our variable name and data type.
```swift
var username: 
``` 

- `String` specifies the type of data this variable will contain: 
```swift
var username: String 
```

- `=` is our assignment operator 
```swift
var username: String = 
```

- And `"Billy"` is the value we assigned to our variable.
```swift
var username: String = "Billy"
```
**That's it!** <br>
Now everytime we refer to the variable name `username`, we get returned the String `"Billy"`. <br>
```swift
print(username)
// Output: "Billy"
```

This makes it much more memorable and easy to read as you'll see when we get to a real world example below.





#### Deeper look
{: .no_toc}

<details open>
<summary><code> Keywords</code><br></summary>
<blockquote><code>Keywords</code> such as <code>var</code>, <code>func</code>, <code>switch</code> are examples of keywords in Swift that are reserved and serve a purpose. Be careful not to use these words when creating variable or argument names as it may result in an error when you try to build your application.<br> <br>

You'll notice the keywords in Swift will turn a specific color that will alert you a keyword is being used. In my example, I am using the midnight dark theme and so my key words show up in Pink. We'll cover the major ones throughout these lessons, so don’t worry about this for now.</blockquote>
</details>



<details closed>
<summary><code>Naming Conventions</code></summary>
<blockquote>When creating variable names, we want to put some extra care into choosing a name that is descriptive but also short and concise. Anyone reading your code should immediately know what is being stored. <br><br>

To help with readability, be sure to use camel casing -- lowercase the first letter of the first word and uppercase any following words in the name for readability. Remember to use camel casing with no whitespace and remember it cannot begin with a number.<br>

<blockquote> (e.g. exampleOfCamelCasing) </blockquote>



</blockquote>
</details>
 


---
## Data Types in Swift
Swift is a type safe language meaning Swift wants you to be clear of what types of values your code can work with. If you declare your variable to be a data of type Int (which can only store Integers), we cannot pass it a series of text (which is of data type String) without causing an error. 

Here are some of the most common data types you’ll find yourself using: 

```swift 
var someInteger: Int = 123
var someString: String = “add some text here”
var someBool: Bool = true
var someDouble: Double = 92.23
var someCharacter: Character = “C”
```

To view the full list, see <a href="https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html#ID317"> Swift's data types</a>




---
### Using Type Inference 
Now the Swift Programming Language supports <i> type inference. <i> 
Instead of having to manually declare the  data type of every variable we create, the compiler is able to figure out on its own if we provide the default value upon creation. <br>

Let's take a look at an example:

```swift 
Var temperatureOne: Double = 98.7
// results are the same 
Var temperatureTwo = 98.7
```

```swift 
print(temperatureOne) //Output: 98.7
print(temperatureTwo) //Output: 98.7
```






Let's look at a practical example:

---

## Real World Example:

Let's say we're creating an app where the user is requested to enter their: <br>
- "name" <br>
- "age"  <br>
- "address" <br>
- select if "new user" <br>

we might create a 4 new variables to store our users information:
1.  `userName`of type <b>String</b>
2. `userAge` of type <b>Int</b>
3. `userAddress` of type <b>String</b>
4. `newUser` of type <b>Bool</b> 


![MCS](/assets/images/var/phone_entry.png)

Our code may look something like this:
```swift
var userName: String = "James"
var userAge: Int = "22"
var userAddress: String = "123 1st Street"
var newUser: Bool = true 
```

### And that's it! 
{: .no_toc}

By now, I hope this lesson gave you a solid understanding of what variables are and more importantly how they can be used when developing your own programs. 

---

## What's Next

In the next lesson, we’ll cover the differences between variables and constants and most importantly the 'why' we want to use one over the other.  

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


<!-- 🟧 Old home?
---
layout: default
title: Home
nav_order: 1
description: "Just the Docs is  responsive Jekyll theme with built-in search that is easily customizable and hosted on GitHub Pages."
permalink: /
---

![MCS](/assets/images/big_banner.png)

<center><h1 style="font-size:4vw">Tutorials @ MakeCodeStick</h1></center>
<center><i><h4 style="font-size:4vw">⭐️ Update In Progress</h4></i></center>

 <center><a href = "mailto:contact@makecodestick.com">contact@makecodestick.com</a></center>

[Video](https://www.makecodestick.com/){: .btn .btn-purple } 
[Tutorials]( ){: .btn .btn-blue } 
[Docs](){: .btn .btn-green }

-->

