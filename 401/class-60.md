# Class 30

## Hash Tables

Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

- used to store a key and quickly retrieve the value

- Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity

| Term      | Description |
| ----------- | ----------- |
|Hash|A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.|
|Buckets|A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.|
|Collisions|A collision is what happens when more than one key gets hashed to the same location of the hashtable.|
