# C++ : Assigment 1 (12/01/2022)

For this assignement, you will implement a very specific hash table.

## Instructions :

- You need to send 2 files (HashTable.h & HashTable.cpp).
- All the keys are english words (eg. Apple).
- Hash function : the first character of the word (eg. hash of `apple` is `a`).
- Hash table contains 26 slots (`a` to `z`) (you won't need more).

<br>

- Each slot has different possible status (`NeverUsed`, `Tombstone` or `Occupied`).
- The status must be an `enum class` called `HashTableStatus`.
- Each slot contains a pointer to a struct called `HashTableElement` which contains the `HashTableStatus` and the value.
- Each element start with the status `NeverUsed` and an empty value.

<br>

- ***You must implement at least 4 public methods and 1 operator in your class :***

## - Insert
- First, check if key exists. If it does, do nothing.
- Lowercase the value and take the first character as hash value.
- If the status of the corresponding slot is not `Occupied`, put it here.
- Else, try the next slot until you find a free one. If all the table is full, throw `std::runtime_error`.

## - Delete
- Given a key, search for it to locate his slot (if it doesn't exists, do nothing).
- If found, change the status to `Tombstone`.

## - Search
- Return true if key is found, otherwise false.

## - GetData
- Return the raw array of elements pointers (std::array, std::vector, HashTableElement*, etc...).

## - Operators 

- You should override the `<<` operator to print the content of the hash map.
- Example :
``` cpp
HashTable h;
h.Insert("Saucisson");
h.Insert("Foie Gras");
h.Insert("Chapon");
h.Insert("Patates");
h.Delete("Saucisson");

std::cout << h << std::endl; // Output : Chapon Foie Gras Patates
```

## Grading scale :

- All the tests passes (12.5pts).
- Technical choices (array type, etc...) (2.5pts).
- Good practices (clean code, const usage, naming conventions...) (5pts).