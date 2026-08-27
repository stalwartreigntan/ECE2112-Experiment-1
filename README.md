______________________________________________________________
# ECE 2112 - Experiment 1: Introduction to Python Programming
______________________________________________________________

Name: Tan, Stalwart Reign J.

Section: 2ECE-D



This experiment introduces basic Python programming concepts, including functions, string operations, indexing, and other methods. These concepts are applied to solve three problems: Word Rotation, Username Building, and Bookend Swapping.


____________________________
# A. WORD ROTATION PROBLEM
____________________________

def rotate_word(text):
    return text[1:] + text[0]

The use of string indexing and slicing allows us to rearrange characters in a word. To define a new function in Python, we use (def) in the beginning of the code, while the name of the function is (rotate_word). This allows us to rotate the letters of each words. To allow all remaining letters, except for the first letter of the word, to remain at its order, we use the code statement (text[1:]). To move the first character of the string to the end, we apply (+ text [0]). The (return) is a keyword that allows the function to send back the result of the code.

Examples:
print(rotate_word("python"))  # ythonp
print(rotate_word("logic"))   # ogicl
print(rotate_word("Code"))    # odeC
print(rotate_word("A"))       # A

_______________________________
# B. USERNAME BUILDER PROBLEM
_______________________________
def make_username(first_name, last_name):
    first_name = first_name.lower().replace(" ", "")
    last_name = last_name.lower().replace(" ", "")
    return first_name + "." + last_name
In this problem, we have to create a function that takes a person's first name and last name, turning it as a formatted username. In order to do this, we must turn all letters to lowercase, wherein we apply (first_name.lower().replace(" ", "")) and (last_name.lower().replace(" ", "")). To remove the spaces between the first name and the last name, we join the two names using a period (.) between them, which we write as (first_name + "." + last_name).

Examples:
print(make_username("Ada", "Lovelace"))      # ada.lovelace
print(make_username("Alan", "Turing"))       # alan.turing
print(make_username("Ana Maria", "De Leon")) # anamaria.deleon

___________________________
# C. BOOKEND SWAP PROBLEM
___________________________
def swap_bookends(items):
    first, *middle, last = items
    return [last, *middle, first]
Bookend Swap creates a function (swap_bookends) that keeps the middle element in their original position, but swaps the first and the last element. To assign the elements, we use the variables "first", "middle", and "last". The code statement (return [last, *middle, first]) gives us the new list that has already swapped the first and last elements.

Examples:
print(swap_bookends([1, 2, 3, 4, 5, 6]))       # [6, 2, 3, 4, 5, 1]
print(swap_bookends(["red", "green", "blue"])) # ['blue', 'green', 'red']
print(swap_bookends([8, 3]))                   # [3, 8]
