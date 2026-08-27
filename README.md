# ECE-2112-PA1

**By: James Eon M. Santiago | 2ECE-B**

This Repository Contains the Programming Assignment #1 for the Course "Advanced Computer Programming and Algorithms", which includes three python problems related to Module 1 - Base Computing with Python.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **(A) Alphabet Soup Problem**

Create a function named **rotate_word()** that accepts a non-empty string. Move the *first character* of the string to the *end* while keeping all remaining characters in their original order. Preserve the capitalization of every character.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

1. An input prompt is needed, in order for the user to input any text.

```python
text = input("Enter a Word")
```
2. To calculate the length of a given text by the user, this can be done by using the len() function.

```python
text = input("Enter a Word")
length = len(text)
```
3. Define a function named **rotate_word()** that rearranges the letters by slicing.
   
   
   The function slicing is formatted as [start:stop:step]
   

   The start function indicates the index position where it should begin its slicing. The first letter or number on a string is always indexed as 0.
   

   The stop function indicates where the slicing should stop.
   

   The step function indicates how many positions it would step forward each time.
   

   The "+" symbol allows us to concatenate strings.
   

Using this, we can define the function as:


```python
def rotate_word(text):
  return (text[1:length:1) + (text[0,1,1])
```


  "(text[1:length:1)" - allows us to slice the rest of the word excluding the first character of the string.
  
  
  "(text[0,1,1])" - slices the first character of the string.
  

  Returning these functions and concatenating them respectively would yield a string that has the first character rotated to the end of the string.
  

Therefore, the final code should look like: 


```python
text = input("Enter a word")
length = len(text)

def rotate_word(text):
    return (text[1:length:1])+(text[0:1:1])

rotate_word(text)
```

  
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# **(B) Username Builder Problem**


Create a function named "make_username()" that accepts two strings: first name and last name. The function must:

   
  • Converts all letters to *lowercase*
  
   
  • Removes *all spaces* from the first and last names.
  
   
  • Joins the processed first and last names using one period (.)
  

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


1. Add an input prompt in order for the user to input any first name and last name.
   

```python
first_name = input("Enter First Name: ")
last_name = input("Enter Last Name: ")
```


2. To define a function named "make_username()" which satisfies the 3 conditions, "*.lower()*" and "*.replace()*" and concatenation must be used. To display the username, the "*print()*" function must be used as well.


   The ".lower()" function allows any inputted uppercase letters to be transformed into lowercase ones.


   The ".replace()" function allows any spaces in the user-input to be removed.


Combining all these would result to a defined function:


```python
def make_username(first_name, last_name):

    lower_first_name = first_name.lower().replace(" ","")

    lower_last_name = last_name.lower().replace(" ", "")

    username = lower_first_name + "." + lower_last_name

    print(username)
```


The final code should look like:


```python
first_name = input("Enter First Name: ")
last_name = input("Enter Last Name: ")

def make_username(first_name, last_name):

    lower_first_name = first_name.lower().replace(" ","")

    lower_last_name = last_name.lower().replace(" ", "")

    username = lower_first_name + "." + lower_last_name

    print(username)

make_username(first_name, last_name)
```


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **(C) Bookend Swap Problem**


Create a function named swap bookends() that accepts a list containing at least two elements. Unpack the list into three variables:


  • first – the first element;
  
  
  • middle – a list containing everything between the first and last elements; and
  
  
  • last – the last element.

  
Using these variables, return a new list in which the first and last elements have exchanged positions. The elements in middle must remain in their original order. Do not modify the input list.


---


1. Add an input prompt in order to accept multiple items from the user. The "*.split()*" function splits the string into a list of items.
   

```python
items = input("Please Input Items, Numbers, etc: ").split()
```


2. In order to make sure that there are at least 2 user inputs, an if-else statement would be used.


```python
if len(items) <2:
        print("Please Input Atleast 2!!!")
else:

    print ("Swapped Bookends: " , swap_bookends(items))
```


3. Define a function named "*swap_bookends()*" that uses the "*" symbol to extract the first, middle and last elements.
   

    The "*first*" variable grabs the first element on the list.


    The "**middle*" variable grabs the elements between the first and the last on the list and maintains their positions.


    The "*Last*" variable grabs the last element on the list.


    Using concatenation, we can make a list where the last is placed at the front, and the front is placed at the last; while keeping the middle the same.


Combining this would give us a defined function:


```python
def swap_bookends(items):
    
    first, *middle, last = items
    return [last] + middle + [first]
```


The final code should look like:


```python
items = input("Please Input Items, Numbers, etc: ").split()

if len(items) <2:
        print("Please Input Atleast 2!!!")
else:

    print ("Swapped Bookends: " , swap_bookends(items))
    

def swap_bookends(items):
    
    first, *middle, last = items
    return [last] + middle + [first]
```


Thanks for reading.


Access the code at 
https://github.com/jamesesantiago/ECE2112-PA1/blob/main/James%20Eon%20M.%20Santiago%202ECE-B%20PA1.ipynb
Download and open on Jupyter Notebook to run the python notebook.
