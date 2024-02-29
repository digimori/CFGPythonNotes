# CFGPythonNotes
Study notes for Python

## The Basics:
### Comments:
```
# This is a comment

You can also make a multi line comment by using this:
"""
This is
A
Multiline
"""

```

### Print:
```
print('This is like console.log in JS')
print(VariablesGoHereToo)
```

- You can output multiple values at once using comma separated values:
```
x = 'Cats'
y = 'Dogs'
z = 'Bunnies'

print(x, y, z) # Will output: 'Cats', 'Dogs', 'Bunnies'
```

- For strings, you can use the + operator, however this will not work for numbers and will instead add them together.
```
print(x + y + z) # Will output: 'Cats', 'Dogs', 'Bunnies'

x, y, z = 5, 10, 20
print(x + y + z) # This will output 35 as it adds the values together in a mathematical sense
```

- Trying to combine a string and a number with the + operator will throw an error.
- Due to the + operator causing issues in this way, it's better practice to use commas.

## Indentation:
- Python is fussy (But it does breed good practice indentation habits) with indentation as it's used to define code blocks as opposed to other languages where blocks are often defined through brackets be it curly{}, square[] or curved().
- Python uses these brackets too (Like above for Print statements), but not for block purposes like languages like JS.
- Indentation also requires consistency. Common practice is often either a tab OR spaces (4 spaces is equal to a tab, but you're better off picking one and sticking with it).

## Data types:
- Finding Data types of the printed element. This is like typeOF() in JS:
```
print(type(Variable))
```

## Defining Variables:
- Different to JS, we don't need to use Let/Const/Var:
```
ThisIsAVariable = 'Strings and things'
```
### Variable casting:
- Like Typescript (And to be honest, most lower level languages), Python allows for casting, which is where you define the data type of the variable when it is declared:
```
x = str(3)    # x will be '3' as str means String
y = int(3)    # y will be 3 will be a number or 'integer'
z = float(3)  # z will be 3.0 is a float which is used for decimal points
```

- Strings can be defined either by single or double quotes, but be consistent about it!

### Case Sensitivity:
- Variable names are case sensitive, so as an example:
```
a = sen
A = "Sen"
#A will not overwrite a as A and a are considered two separate variables (But be more descriptive otherwise readability will suffer)
```

## Naming conventions and best practices:

### Variable naming:
- A variable name must start with a letter or the underscore character
- A variable name cannot start with a number
- A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
- Variable names are case-sensitive (age, Age and AGE are three different variables)
- A variable name cannot be any of the [Python reserved keywords](https://www.w3schools.com/python/python_ref_keywords.asp).

### Cases:
- Camel Case: Each word after the first will start with a capital letter:
```
thisIsAnExample = 'ofCamelCase'
```

- Pascal Case: Every word starts with a capital letter:
```
ThisIsPascalCase = 'PascalCaseWheee'
```
  
- Snake Case: Each word in Snake case is separated by an underscore:
```
this_is_snake_case = 'incase_you_were_wondering'
```
### Multiple Values:
- This is very much like deconstruction in JS:
- Multiple values can be assigned to different variables on a single line:
```
x, y, z = 'Cats', 'Dogs', 'Bunnies'
print(x) # 'Cats'
print(y) # 'Dogs'
print(z) # 'Bunnies'

Essentially we have just written:
x = 'Cats'
y = 'Dogs'
z = 'Bunnies'

But by only using one line instead of 3.
```

- You can also assign One-To-Multiple in the same way, but only assigning one value to several variables at once:
```
x, y, z = 'Cats'
print(x) # 'Cats'
print(y) # 'Cats'
print(z) # 'Cats'

```

### Unpacking objects:
- This is like deconstruction again:
```
fruits = ['apple', 'banana', 'cherry']
x, y, z = fruits
print(x) # 'apple'
print(y) # 'banana'
print(z) # 'cherry'

So this is like saying that the variables x, y, z are equal to the values in the fruits array.
They will unpack in the same order due to indexing.

```




