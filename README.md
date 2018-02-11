# PA5-HashMapImpl-Key
Key and initial writeup draft for PA5.

## Learning Objectives

The goal of this assignment is to use two or more datastructures
in a coordinated way to solve a problem.

The problem to be solved in this assignment is to implement a 
HashMap.  Therefore an additional learning objective is to 
increase your skill level with HashMaps from just being able 
to use them to understanding how to implement them.

The dictionary abstract data type can be used to solve many
programming problems and therefore questions about hash tables 
frequently occur in job interviews.

## The Assignment

You will be redoing PA2-HashMap with your own HashMap implementation.

### The New

####Hash Map Implementation

A hash table is a data structure that offers very quick operations such as inserting data
and searching for data. You have used a form of a hash table when using the HashMap
class in Java. However, in this assignment you will implement your own version of a hash map.


First, you should read up on what a hash table is. [Wikipedia](https://en.wikipedia.org/wiki/Hash_table) is a good place to start.

At its heart a hash table (hash map) is an array that works together with a function,
known as a hash function, that takes a key and returns an index into that array. We
usually call the elements in the array buckets. A critical part of writing a good
hash map implementation is writing a good (and appropriate) hash function. It must
spread out values evenly based on different input values and needs to always produce
the same value if the same element is given to it.


There are multiple ways to implement a hash map, here are a three:
- An array that contains a linked list
- A linked list that holds an other linked list (2d linked list)
- An array that contains another array (a 2d array)

**YOU MUST IMPLEMENT AT LEAST TWO OF THESE!!**


For this assignment, you will be implementing your own HashMap class using the following hash function.
**[TODO: FIND A USABLE HASH FUNCTION THAT GIVES LOW NUMBER OF CONFLICTS]**



You will create a class called MyHashMap that maps keys to values. This hash map will use chaining to handle the collisions of elements. You will need to implement the following public methods:


h(k) == the value produced by putting k into the hash function listed above 

You must implement the following methods
```
insert(k, v)
	Adds the value, v, to the table at the index h(k). If there is no value here, place the value, v,
	in this index, if there is a value here, replace that value.

remove(k) 
	Removes the value from the table at the index of string k, if it's there. If not, this does nothing. 

getValue(k) 
	Returns the value from the table that is mapped to key k, if there is a value associated with k.
	If there is no such, then it should return -1 for any numeric value or NULL for any object value.
	(Note: It's good practice to return something that indicates the key was empty)

contains(k)
	Returns true if there is a value in the table associated with key k, and false otherwise.

size() 
	Returns the number of values currently being stored in the table.

capacity()
	Returns the number of buckets (size of the array) being used by the structure.
	(Note size() returns how many things are currently being stored and capacity
	returns how many buckets there are to store things.)

printTable() 
	Prints out the elements of your table. The output for this method is specified below.
	This method is used for debugging purposes to help you.

Two constructors
	One with no parameters that creates a table with an internal
	array of default size 100. One that takes an integer n as a parameter and creates
	an array of size n to be used by the structure.

```

**NOTES**:

If the number of elements in the hash table ever equals the size of the table, then you should **double**
the table's size. (If using an array what must you do to the emelements already in the table?)

The printTable method should print out every entry in the table. You can print
the information however would like as long as it makes sense to you and you
explain it via commenets.

The following in an example of one way to print the information:

	Index 0: null
	Index 1: 11 -> 44
	Index 2: 22



You will also be comparing and contrasting the two implementations that you have
chosen. This will all be written in the README.md file in your PA5 folder.
Stuff to think about:
- What are some benefits in using these specific data structures?
- What are some weaknesses.
- Which implementation is faster for indexing? 
- Which implementation is faster for deletion?
- Which implementation do you think was more difficult to implement?
  - Why?


### The Old

See [the PA2 Writeup](https://github.com/UACS210Spring2018/PA-and-Section-Writeups/tree/master/PA2-HashMap-Writeup)

