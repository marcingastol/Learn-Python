# Python Basics


Navigating Jupyter Notebook:

Create a new cell in your Jupyter notebook and run:


## Import the os module, which allows interaction with the operating system
```python
import os
```

## List all files and directories in the current directory ('.')
```python
os.listdir('.')
```

#### Explanation:

import os: This imports Python's built-in os module.
os.listdir('.'): Lists all files and folders in the current directory (.).

#### Exercise:

Use os.listdir('/content') to list files in a different directory.

## Check Your Working Directory:


## Get the current working directory
```python
os.getcwd()  ## This will return the current directory path as a string.
```

#### Explanation:

os.getcwd(): Returns the path of the current working directory, useful for knowing where you are.
#### Exercise:

Use os.chdir('/content') and then run os.getcwd() again to see how it changes.

## Changing the Working Directory:

```python
# Change the working directory to '/content'
os.chdir('/content')

# Verify that you've changed directories by getting the current working directory again
print(os.getcwd())
```

#### Explanation:

os.chdir('/content'): Changes the current directory to the specified path.
print(os.getcwd()): Prints the current directory to confirm the change.

#### Exercise:

Change the directory back to your home directory (os.chdir('/content')) and verify it using os.getcwd().

## Create Directories:

```python
# Create a new directory called 'python_files'
os.makedirs('python_files')

# Create nested directories 'python_files/nested_directory'
os.makedirs('python_files/nested_directory')
```

#### Explanation:

os.makedirs('python_files'): Creates a new folder named python_files.
os.makedirs('python_files/nested_directory'): Creates a folder inside python_files named nested_directory.
#### Exercise:

Create a new nested directory python_files/nested/inside.

## Check if a Directory Exists:

```python
# Check if 'python_files' exists in the current directory
os.path.exists('python_files')  ## Returns True if the path exists, otherwise False.
```

#### Explanation:

os.path.exists('python_files'): Checks whether the specified path exists.
#### Exercise:

Try checking if a non-existent path, like 'non_existent_folder', exists.

## Create and Write to a File:

```python
# Open a file named 'example.txt' in write mode ('w')
with open('python_files/example.txt', 'w') as file:
    ## Write some text to the file
    file.write('Hello, Python!\nWelcome to the basics of Python.')
```

#### Explanation:

with open('python_files/example.txt', 'w') as file: Opens a file for writing, creating it if it doesn't exist.
file.write(...): Writes the specified string to the file.


#### Exercise:

Try creating a new file and writing different text into it.

## Read from a File:

```python

# Open the file 'example.txt' in read mode ('r')
with open('python_files/example.txt', 'r') as file:
    ## Read the entire content of the file
    content = file.read()
    ## Print the content of the file
    print(content)
```

#### Explanation:

with open('python_files/example.txt', 'r') as file: Opens the file for reading.
file.read(): Reads the entire content of the file into a variable.
#### Exercise:

Try reading the file line by line using file.readline().

## Appending to a File:

```python

# Open the file 'example.txt' in append mode ('a')
with open('python_files/example.txt', 'a') as file:
    ## Add more content to the file
    file.write('\nAppending more content to the file.')

# Verify the new content by reading the file again
with open('python_files/example.txt', 'r') as file:
    print(file.read())
```

#### Explanation:

with open(..., 'a'): Opens the file in append mode, adding content at the end without overwriting.
file.write(...): Adds a new line to the existing file content.
#### Exercise:

Try appending multiple lines of text and then reading them.

## List All Files with a Specific Extension:

```python

# List all files in 'python_files' that end with '.txt'
txt_files = [f for f in os.listdir('python_files') if f.endswith('.txt')]

# Print the list of text files
print(txt_files)
```

#### Explanation:

[f for f in ...]: This is a list comprehension that iterates over all files in python_files.
f.endswith('.txt'): Checks if a file name ends with .txt.

#### Exercise:

List all files in a directory that end with .py.

## Copying Files:

```python

# Import the shutil module for file operations
import shutil

# Copy 'example.txt' to 'copy_of_example.txt' in the same directory
shutil.copy('python_files/example.txt', 'python_files/copy_of_example.txt')
```

#### Explanation:

shutil.copy(...): Copies the specified file to a new location.

#### Exercise:

Copy the file to a new directory and verify if it exists using os.path.exists().

## Moving Files:

```python

## Move 'copy_of_example.txt' to the nested directory
shutil.move('python_files/copy_of_example.txt', 'python_files/nested_directory/copy_of_example.txt')
```

#### Explanation:

shutil.move(...): Moves a file from one location to another.
#### Exercise:

Move the file back to the python_files directory.

## Delete Files and Directories:

```python
# Delete the file 'copy_of_example.txt'
os.remove('python_files/nested_directory/copy_of_example.txt')

# Remove an empty directory
os.rmdir('python_files/nested_directory')

# Remove the entire 'python_files' directory and its contents
shutil.rmtree('python_files')
```

#### Explanation:

os.remove(...): Deletes a single file.
os.rmdir(...): Deletes an empty directory.
shutil.rmtree(...): Deletes a directory and all its contents.
#### Exercise:

Try to delete a non-empty directory with os.rmdir() and observe the error. Then use shutil.rmtree() to delete it.
## Using Environment Variables:

```python

## Set a new environment variable named 'MY_VAR'
os.environ['MY_VAR'] = '12345'

## Retrieve and print the value of the environment variable
print(os.environ.get('MY_VAR'))

```
#### Explanation:

os.environ['MY_VAR'] = '12345': Sets an environment variable.
os.environ.get('MY_VAR'): Retrieves the value of an environment variable.

#### Exercise:

Set a new environment variable with your name and retrieve it.
