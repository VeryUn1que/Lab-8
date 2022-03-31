# Lab-8
Lab 8.4 CS 2420
This class creates and manages an open address hashtable data structure. Your hashtable should be implemented as an array using Quadratic Probing to resolve collisions.  It will also use a rehash() function if the capacity of the table becomes beyond a certain threshold, the default is 65 percent full.

You are welcome to modify the No-Brainer assignment and add the necessary implementation to make the hashtable be able to resize and use quadratic probing.

You will need a new private variable named loadFactorThreashold that will be used to determine how full the hashtable can be before there needs to be a rehash. 

 

Implement the following methods.  

Hashtable() //Constructs and empty hash table with a default capacity of 17 and a default load factor threshold of .65
Hashtable(int cap)//Constructs an empty hash table with the given capacity and a default load factor threshold of .65
Hashtable(int, double)//Constructs an empty hash table with the given capacity and load factor threshold values
Hashtable(const Hashtable& other)//creates a deep-copy of the given hashtable
Hashtable& operator=(const Hashtable& other)//replaces the current hashtable with a deep-copy of the given hash table
~Hashtable()//cleans up all allocated memory of the hashtable if using raw pointers
int size() const\retuns the number of items currently in the hashtable
int getCapacity() const\returns the capacity of the hashtable (i.e. the size of the array)
double getLoadFactorThreshold() const //returns the load factor threshold variable
bool empty() const//returns true if the table is empty or false otherwise
void insert(const int)//Inserts the given value into the hashtable.  When there are collisions, quadratic hashing is used instead of linear.  If the table capacity is higher than the loadFactorThreshold, then rehash the table.
void rehash(): Resize the table using the following algorithm....  double the capacity of the list and then finds the next prime number to determine the  size of the new capacity.  Rehash all the items according to the new hash algorithm.  You may need to create a temporary array in order to accomplish this.  Keep in mind with unique pointers, you must use the keyword "move" to transfer ownership of the pointer. 
static bool isPrime(int): Takes an int parameter and returns true if the number is prime.  Used in finding the next prime number.  Note: should be static for testing purposes.  To make it static, put the word static in front of the function definition in the class.  It is not added to the function implementation after the class.
static int nextPrime(int): Takes an int value and returns the next prime number.  Note: should also be static for testing purposes
void remove(int)//Removes the given value from the hashtable. If the value is not present it takes no action and throws no errors. Must use Quadratic Probing to find the element.
bool contains(int) const//Returns true if the given value is contained in the hashtable or false if the value is not in the hashtable, must use Quadratic Probing to find the element.
int indexOf(int) const//Returns the index of the given value. If the value is not in the hashtable, returns -1. This is not a normal method for a hashtable and is here solely to test that your hashtable does quadratic probing. 
void clear()//Removes all values from the hashtable, resetting it to an empty state
