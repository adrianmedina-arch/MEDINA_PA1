# Programming Assignment 1
## Adrian Gabriel M. Medina | 2ECE-C
## 8/27/2026

## I. Intended Learning Outcomes
At the end of this laboratory activity, the student should be able to:
1. use basic Python functions, operators, and string operations;
2. manipulate strings using indexing, slicing, and built-in string methods;
3. apply sequence unpacking to manipulate the elements of a list; and
4. construct simple Python functions that return a specified result.

## II. Programming Problems

### A. WORD ROTATION PROBLEM

`Explanation`:

* text[1:] uses string slicing to take the characters starting from the second character up to the end of the string.

* text[0] uses string indexing to access the first character of the given text.

* The + operator joins these two parts together, placing the first character after the rest of the string.

* The return statement sends the newly arranged string back as the result of the function.

* The print() statements are used to display the results of the provided test cases.

## Code
```python
def rotate_word(text):
    return text [1:] + text [0]
print(rotate_word("python"))
print(rotate_word("logic"))
print(rotate_word("code"))
print(rotate_word("A"))

ythonp
ogicl
odec
A
```

### B. USERNAME BUILDER PROBLEM

5. `Explanation`:

* The function receives two values through the parameters first_name and last_name.
* first_name.lower().replace(" ", "") converts the first name to lowercase and removes any spaces. The result is stored in a new variable called first_clean.
* The same process is applied to last_name, and the cleaned result is stored in last_clean.
* first_clean + "." + last_clean combines the two processed names and places a period between them to form the username.
* The return statement gives the completed username as the output of the function.

## Code
```python
def make_username(first_name, last_name):
    first_clean = first_name.lower().replace(" ", "")
    last_clean = last_name.lower().replace(" ", "")
    return first_clean + "." + last_clean
```
```python
(make_username("Ada", "Lovelace")
```
'ada.lovelace'
```python
(make_username("Alan", "Turing"))
```
'alan.turing'
```python
make_username("Ana Maria", "De Leon")
```
'anamaria.deleon'

### C. BOOKEND SWAP PROBLEM

`Explanation`:

* first, *middle, last = items uses extended sequence unpacking to divide the list into three parts.
* first stores the first element, last stores the last element, while *middle collects all the elements between them.
* [last] + middle + [first] creates a new list by placing the last element at the beginning and the first element at the end.
* The middle elements remain in their original order because middle is placed between [last] and [first].
* The return statement gives the newly arranged list without changing the original items list.

## Code
```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]
```
```python
print(swap_bookends([1, 2, 3, 4, 5, 6]))
```
[6, 2, 3, 4, 5, 1]
```python
print(swap_bookends(["red", "green" , "blue"]))
```
['blue', 'green', 'red']
```python
print(swap_bookends([8, 3]))
```
[3, 8]

#### READMe file version
AUG 27, 2026 - Initial Output 
