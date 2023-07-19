# Hash Tables

##  Intro to Hash Tables
* what is a hash table?
A hash table, also known as a hash map, is a data structure used to store and retrieve data efficiently. It provides a way to associate keys with values, allowing rapid access to the values based on their corresponding keys. The fundamental idea behind a hash table is the use of a hashing function to map keys to specific indices in an array. This mapping allows for quick look-up and insertion of values, making hash tables a popular choice for many applications that require fast data access.

* Why do we use them? 
1. Hold unique values
2. Dictionary
3. Library
   
* What Are they : 
Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.
The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

* Creating a Hash
A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a simplistic hashing algorithm:

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

##  basics of hash tables

1. Hash Function: A hash function takes a key as input and computes a hash code, which is an integer that represents the index where the corresponding value will be stored in the underlying array. The hash function should be deterministic, meaning for a given input key, it always produces the same hash code.

2. Array: The underlying data structure of a hash table is an array, where each element holds a "bucket" that can store one or more key-value pairs.

3. Collisions: Since the hash function maps different keys to the same index occasionally (due to its limited range compared to the number of potential keys), collisions can occur. Handling collisions is a critical aspect of implementing a hash table.

   a. Separate Chaining: One approach to dealing with collisions is to use separate chaining. In this method, each bucket in the array contains a linked list or other data structure that holds multiple key-value pairs with the same hash code.

   b. Open Addressing: In open addressing, when a collision happens, the algorithm searches for the next available (unoccupied) slot in the array based on a predetermined strategy like linear probing or quadratic probing.

4. Load Factor: The load factor of a hash table refers to the ratio of the number of stored elements (key-value pairs) to the size of the array. A high load factor can lead to increased collisions and degrade performance. Resizing the hash table can be done when the load factor exceeds a certain threshold to maintain efficiency.

5. Operations:
   - Insertion: The process of adding a new key-value pair to the hash table.
   - Lookup/Retrieval: Finding and returning the value associated with a specific key.
   - Deletion: Removing a key-value pair from the hash table.
  
## Methods
1. set()
When adding a new key/value pair to a hashtable:
* send the key to the hash() method.
* Once you determine the index of where it should be placed, go to that index
* Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
* If something does exist, add the new key/value pair to the data structure within that bucket.
  
2. get()
The get() method takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

3. has()
The has() method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the hash() method and check the hashtable if the key exists in the table given the index returned.

4. keys()
The keys() method returns a collection (array) of unique hash keys.

5. hash()
The hash() method will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.
