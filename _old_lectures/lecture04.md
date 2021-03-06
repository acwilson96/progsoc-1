---
layout: post
title:  "Lecture 4 - Functions"
date:   2017-02-15 16:00:00 +0000
categories: old_lecture
---

# Functions

Functions in Python work similarly to ordinary mathematical ones. They transform the input they're given (in our case it's often strings,in school it might be variable x) and give out an output consisting of results that comply with the criterions we defined in the function.

## Example 1
We can start defining a function as an empty space. Like in the exaple below:
```python
sum_of_x = 0
```
Subsequently, we define a for loop that will, as explained in our last lecture, repeat the subsequent process for
values within the range specified below. 

```python
for i in range(10000):
  if i%2 == 0:  
    sum_of_x = sum_of_x + i
print(sum_of_x) 
```
The condition 'if i%2 == 0' specifies that numbers we are interested in are those, whose remainder after 
a division by two is zero. This means that we are interested in even numbers within the range specifed above.
The next command tells Python to sum all of these (even) numbers cumulatively and to print the sum.

## Example 2
We first define numbers to be an empty list. Subsequently, for all values up to 100
we append only those, whose remainders of division by 2 or 3 are zero. Ultimately we will have
a list of values containing only numbers divisible by 2 or 3.

```python
numbers = []
for n in range(100):
  if n % 2 == 0 or n % 3 == 0:
    numbers.append(n)

print('multiples of 2 or 3 ', numbers)
```
Notive how we made use of 'or' as a logical statement that allows either of the two conditions to
allocate any number that statisfies it into our empty list called numbers. 
Had we used 'and', we'd get numbers that are divisible both by 2 and 3 (e.g. 6, 12, 18....).
Next we use the function '.append' we learned in our first lecture to fill in our list with values 
satisfying our function.

# Function syntax

```python
def function_example(x):
  return x                # <- block of the function
```
Functions definition begin with keyword ``def`` then the function name and arguments in brackets. The example above defines a function that simply returns its only argument. so ``function_example(1)`` will simply be ``1``. 
The block of the function is similar to block of ``if`` or ``for``.  The function ends with ``return`` statement (or when the block ends).

You can have as many function arguments (parameters) as you want: 
try this [interactive code](https://repl.it/Fy3P/3).

Function can do anything. See [this example](https://repl.it/Fy3b/0).

## Exercise 4.1.
Try for yourself: Define a function that will return all prime numbers higher than 2 and smaller than 20.
