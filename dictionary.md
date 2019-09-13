# Dictionary

## Description
A **dictionary** is an abstract data type that stores a collection of
(key, value) pairs such that a given value can be accessed by its key.

## Implementations
Dictionaries are commonly implemented using hash maps.

## Interface
For a dictionary with keys of type K and values of type V:

| Name     | Type           | Description                                      |
| -------- | -------------- | -----------------------------------------------  |
| size     | Size           | The number of items contained in the dictionary  |
| insert   | K ➝ V ➝ ()     | Insert the new pair (key, value)                 |
| update   | K ➝ V ➝ ()     | Update the pair (key, oldValue) to (key, value)  |
| get      | K ➝ V          | Get the item associated with the given key       |
| has      | K ➝ Bool       | Determines whether a given key is contained      |
| delete   | K ➝ ()         | Remove the item associated with the given key    |

## Performance
Note that n is the number of (key, value) pairs in the dictionary.
With a hash map-based implementation:

| Name            | Average Complexity |
| --------------- | ------------------ |
| \<memory used\> | O(n)               |
| size            | O(1)               |
| insert          | O(1)               |
| update          | O(1)               |
| get             | O(1)               |
| has             | O(1)               |
| delete          | O(1)               |

## Examples
- Look up a library patron by their library ID.
- Store site-specific browser settings by domain name.
