# Conditional Statements

## 1. If Statement - Basic Check
python

## Define a variable to store age
age = 18

## Check if the person is old enough to vote
if age >= 18:
    print("You are eligible to vote.")  ## Output: 'You are eligible to vote.'
Explanation:

The if statement checks if age is greater than or equal to 18.
If the condition is True, the message is printed.
Exercise:

Define a variable temperature and print "It's hot!" if the temperature is above 30.
2. If-Else Statement - Two-Way Decision
python

## Define a variable to store the score
score = 75

## Check if the score is passing

```python
if score >= 60:
    print("You passed the test!")  ## Output: 'You passed the test!'
else:
    print("You failed the test.")
```
Explanation:

if checks if score is 60 or higher.
else executes if the condition is False.
Exercise:

Define a variable hours_of_sleep. Print "You are well-rested" if hours_of_sleep is 7 or more, otherwise print "You need more sleep".
3. If-Elif-Else Statement - Multiple Conditions
python

## Define a variable to store time in hours
time = 14

## Determine the part of the day
if time < 12:
    print("Good morning!")  ## Will not run since time is 14
elif time < 18:
    print("Good afternoon!")  ## Output: 'Good afternoon!'
else:
    print("Good evening!")
Explanation:

if checks if time is less than 12.
elif checks if time is less than 18.
else executes if all previous conditions are False.
Exercise:

Define a variable grade. Print "Excellent" if the grade is 90 or above, "Good" if it's between 75 and 89, "Needs Improvement" if between 60 and 74, and "Failing" if below 60.
4. Using Comparison Operators
python

## Define two numbers
a = 10
b = 20

## Check if a is greater than b
if a > b:
    print("a is greater than b.")
else:
    print("a is not greater than b.")  ## Output: 'a is not greater than b.'
Explanation:

> checks if a is greater than b.
The condition fails since 10 is not greater than 20.
Exercise:

Create variables x and y. Print "x and y are equal" if they have the same value, otherwise print "x and y are not equal".
5. Checking Multiple Conditions with and and or
python

## Define variables for weather conditions
is_sunny = True
is_warm = False

## Check if it is both sunny and warm
if is_sunny and is_warm:
    print("It's a perfect day for the beach!")
else:
    print("It might not be a good beach day.")  ## Output: 'It might not be a good beach day.'
python

## Check if it is either sunny or warm
if is_sunny or is_warm:
    print("You can go outside without a jacket.")  ## Output: 'You can go outside without a jacket.'
else:
    print("Better take a jacket.")
Explanation:

and requires both conditions to be True for the overall condition to be True.
or requires only one of the conditions to be True.
Exercise:

Define two variables is_weekend and has_free_time. Print "Go for a hike!" if both are True, otherwise print "Stay in and relax".
6. Nested If Statements
python

## Define a variable for age
age = 16

## Check if age is over 13
if age > 13:
    ## Inside this block, check if age is under 18
    if age < 18:
        print("You are a teenager.")  ## Output: 'You are a teenager.'
    else:
        print("You are an adult.")
else:
    print("You are a child.")
Explanation:

The outer if checks if the age is greater than 13.
The nested if checks if the age is less than 18 within the first condition.
Exercise:

Define a variable weight and height. If weight is above 50, check if height is also above 160. If both are true, print "You qualify", otherwise print "You don't qualify".
7. Using in with Conditionals
python

## Define a list of available fruits
fruits = ["apple", "banana", "cherry"]

## Check if 'banana' is in the list
if "banana" in fruits:
    print("Banana is available.")  ## Output: 'Banana is available.'

## Check if 'orange' is not in the list
if "orange" not in fruits:
    print("Orange is not available.")  ## Output: 'Orange is not available.'
Explanation:

in checks if an element exists in a list or other iterable.
not in checks if an element does not exist in the list.
Exercise:

Create a list of allowed_colors and a variable selected_color. Print "Color is allowed" if selected_color is in allowed_colors, otherwise print "Color is not allowed".
8. Ternary Conditional Statements
python

## Define a variable for speed
speed = 55

## Use a ternary operator to determine if speed is too high
status = "Speeding" if speed > 60 else "Within speed limit"
print(status)  ## Output: 'Within speed limit'
Explanation:

A ternary operator allows for a compact if-else statement.
The condition (speed > 60) determines which of the two options is chosen.
Exercise:

Define a variable temperature and use a ternary operator to print "Too hot" if temperature is above 35, otherwise print "Just right".
9. Comparing Strings in Conditionals
python

## Define a username
username = "admin"

## Check if the username matches a specific value
if username == "admin":
    print("Welcome, administrator!")  ## Output: 'Welcome, administrator.'
else:
    print("Welcome, user.")
Explanation:

== is used to compare strings for equality.
This checks if username is exactly "admin".
Exercise:

Define a variable password and check if it matches a given string. Print "Access granted" if it matches, otherwise "Access denied".
10. Using is for Checking Identity
python

## Define a variable with a value of None
user = None

## Check if the user is None (no user is logged in)
if user is None:
    print("No user logged in.")  ## Output: 'No user logged in.'
else:
    print("User is logged in.")
Explanation:

is checks if two references point to the same object (useful for None checks).
Exercise:

Define a variable session and set it to None. Use an if statement to check if session is not None and print a message accordingly.
