---
layout: post
title:      "Pass By Reference Vs. Pass By Value"
date:       2019-06-07 20:50:57 +0000
permalink:  pass_by_reference_vs_pass_by_value
---


In many computer languanges we learn to use a fundamental skill of assigning a value to a variable and then we learn to create arrays. The two tasks seem smiliar but at their cores are completely diferent. 

<h3><b>Pass By Value</b></h3>

Assiging a variabe to a value is known as pass by value. This includes strings, numbers, other variables and nulls. The computer creates an arrow that points to a specific memory space or address. An example would best demonstrate this:

When you create a variabe called my_num and assign it to equal 5.

```
my_num = 5
```

You have assigned a memory address (a specific byte of memory) to with the binary that creates the value 5.

When you create another variable called my_other_num and set it equal to my_num

```
my_other_num = my_num
```

You are assigning my_other_num to equal 5 but the memory address is different that that of the 5 in my_num

When reassigning the value of the variable my_num to any value, lets say 6, the arrow which points to the memory address holding the first 5 is removed and a new arrow is created to point to a different memory address which will now hold the value 6.

```
my_num = 6
```

In addition, the value for my_other_num would remain 5 and be the memory address would be the same unless you rerun the assignment function:

```
my_other_num = my_num
```

Likewise should we update my_other num, the value and memory address of my_num would not be changed. 

![](http://i66.tinypic.com/2s0lrsx.png)

<h3><b>Pass By Reference</b></h3>

Pass by reference involves data types or arrays, hash/dictionaries.  The computer creates an arrow which points to a specific memory address but you may edit the contents of that memory address without recreating arrows.

Creating an array called my_array and setting the values to be 1, 2, 3.

```
my_array = [1.2.3]
```

Then creating another array set to the equal my_array

```
my_other_array = my_array
```

The memory address for both my_array and my_other_array are the same. Chaning any of the values of my_array will update my_other_array, and any changes done to my_other_arrray will be shows in my_array because the memory address are the same. 

![](http://i65.tinypic.com/ogdshw.png)

<h3><b>Why is this important?</b></h3>

The pass by value and pass by reference methods show us how physical memory (memory addresses) work and explains how a lot of cool tech works. 

If you've ever deleted an image on accident and wanted to retrieve it there is software to do so, but how? 

When you delete a file, you aren't exactly getting rid of the information, instead you are getting rid of the arrow which points to that file. The only way to truly get rid of the file apart from destroying your hard drive is to find the memory address and overwrite it with new content or junk that cannot be understood by your computer. Software that recovers deleted files instead scans your machine for content with no arrows pointing to them and tries to interpet it. Spitting back images of your ex that you've deleted months ago, government secrets and your assignments that you didn't save but will save your neck. 

This is how programs like app cleaner for mac works, it find the files that have arrows which stem from the application you're trying to delete, deletes the arrows and overwrites the memory specific to those memory addresses. 
