# ECE-2112-PA-1
Made by: Franz Justin M. Corpuz | 2ECE-D

The content of this repository contains the Programming Assignment 1 for our course ECE2112 Advanced Computer Programming. This project has three problems referring to Module 1.

# 1. WORD ROTATION PROBLEM 
**Objective:** Move the first character of a string to the end while preserving both the original capitalization and the order of the remaining letters.

The word rotation problem is solved using string slicing and indexing. Python uses zero-based indexing, which means text[0] extracts the first character, while text[1:] extracts characters from the second onward to the last. By concatenating("adding") text[1:] + text[0], the first character is instantly attached to the last index, making it the last character. This technique only rearranges the characters, not altering each one, thus preserving their characteristics, such as capitalization.

Below is the function:
```python
def rotate_word(text):
    return text[1:] + text[0]
```


# 2. The Username Builder Problem
**Objective:** Process a first and last name into a standardized username format that is entirely lowercase, contains no spaces, and is separated by a single period.

To solve this problem, two strings (first_name and last_name) need to be passed to two methods. The methods were .lower(), which converts all letters to lowercase, and .replace(" ",""), which removes all spaces. After the two methods, the strings are concatenated with a period to form the username string. 

Below is the function:
```python
def make_username(first_name, last_name):
    cleanfirst = first_name.lower().replace(" ", "")
    cleanlast = last_name.lower().replace(" ", "")
    return cleanfirst + "." + cleanlast
```


# 3. Bookend Swap Problem
**Objective:** Swap the first and last elements of a list without modifying the original input list or disrupting the order of the middle elements.

Extended sequence unpacking is needed to solve this problem. Since it assigns "first", "*middle", and "last" to your variables, which makes Python know where each is located, an asterisk is also used in the "*middle" to let Python know to collect all variables in between first and last. To create the list, first and last switched places, and *middle stays the same.

Below is the function:
```python
def swap_bookends(items):
    first, *middle, last = items
    return last, *middle, first
```
README FILE VERSION HISTORY
August 25, 2026 - Uploaded the Finished version of the Code

August 25, 2026 - Started with the README file

August 26, 2026 - Finished the README file

August 27, 2026 - Added the README FILE VERSION HISTORY

