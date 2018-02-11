Hash Map Implementation


A hash table is a data structure that offers very quick operations such as inserting data
and searching for data. You have used a form of a hash table when using the HashMap
class in Java. However, in this assignment you will implement your own version of a hash map.


First, you should read up on what a hash table is. Wikipedia is a good place to start:
https://en.wikipedia.org/wiki/Hash_table

At its heart a hash table (hash map) is an array that works together with a function, 
known as a hash function, that takes a key and returns an index into that array.
A critical part of writing a good hash map implementation is writing a good
(and appropriate) hash function. It must spread out values evenly based on different 
input values and needs to always produce the same value if the same element is given to it.


For this assignment, you will be implementing your own HashMap class using a hash function that
you will create. A perfect hash function is one that will produce a unique value for every unique key
given to it. This is nearly impossible so we do not expect you to do this. Your function will probably
produce some collisions. Collisions are when two different elements given to the hash function
produce the same input. That means some insertion values will have the same resulting
index in your hash table. To handle this, we will make every bucket in the array a linked
list. This is sometimes called chained hashing.

Below is an example hash table, hash function, and inserting three values into it. Notice
how we get a collision and insert the new value into the linked list at that index.


