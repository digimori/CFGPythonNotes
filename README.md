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
- Format strings using the format() method.
```
print(x + y + z) # Will output: 'Cats', 'Dogs', 'Bunnies'

x, y, z = 5, 10, 20
print(x + y + z) # This will output 35 as it adds the values together in a mathematical sense

# Formatting example:
cats = 2
cost_of_cats = 0.75
total_costs = cats * cost_of_cat
output = str(cats) + " cats will cost £" + str(total_cost) + " to feed."

print(output) # '2 cats will cost £1.5 to feed.' as a string.
We can format this string in a way that substitutes placeholders ({}) for values.
ie, the above string again:
output = "{} cats will cost £{} to feed".format(cats, total_costs) #  This will place the values in the parameters into the placeholders in the order they are written.

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

### Global Variables and Scope:
- These are variables that are created outside of a funcrion and can be used everywhere in the code file, both inside functions and outside of them.
```
x = 'This is a global variable'

def myFunction():
  print(x) // 'This is a global variable'

myFunction() // This will call myFunction which prints the string assigned to it. 
```
- As for function scope, this will be a local scope and therefore only useable by the function itself.

```
def newFunction():
  x = 'This is function scoped'
  print(x)

newFunction() // This will output 'This is function scoped'
```

- If you want the function scoped variable to be accessible outside of the function, the global keyword can be used, though not considered best practice.
- It can also be used in reverse, to re-assign a global variable inside a function:
```
def newFunction():
  global x
  x = 'This is function scoped'
  print(x)

```

## Data Types extended:
- There are many data types in Python and variables can store data of these types.

### Built-In Data Types.
- Text Type:	'str' or String
- Numeric Types:	int, float, complex or Integer, Floating Decimal and Complex number
- Sequence Types:	list, tuple, range
- Mapping Type:	dict or Object
- Set Types:	set, frozenset
- Boolean Type:	bool
- Binary Types:	bytes, bytearray, memoryview
- None Type:	NoneType

### Setting Data types:
- Getting was explained above in the Basics.
- Data types are set when values are assigned to variables based on their syntax.
- The following examples use constructor functions.

```
# str
string_type = str("I am a string type")

# int, float, complex
integer_type = int(20)
floating_type = float(0.65)  
complex_type = complex(1j)

# list, tuple, range
list_type = list(("Like", "An", "Array")) // Output : ["Like", "An", "Array"]
tuple_type = tuple(("This", "Is", "Tuple"))
range_type = range(5)

# dict
dictionary_type = dict((key="value"))

// Output {"Key": "Value"}

# set, frozenset
set_type = set(("kinda", "like", "an", "array")) // Output {"kinda", "like", "an", "array"}
frozenset_type = frozenSet(("frozen", "set", "type"))

# bool
bool_type_true = bool(5) // Checking if the value of 5 is true

# bytes, bytearray, memoryview
bytes_type = b"Hello"
bytearray_type = bytearray(5)
memoryview_type = memoryview(bytes(5))

# NoneType
nonetype_type = None
```

## Numbers:

### Type conversion with Numbers:

## Casting types:

## Strings:
### join() method:
- The join() method takes all items in an iterable and joins them into one string. A string must be specified as the separator.
```
dictExample = {"name": "Cee", "country":"Wales"}
separatorString = "Seperates"

x = separatorString.join(dictExample)
# Output would be: nameSeparatescountry
# When using a dictionary as an iterable, the returned values are the keys, not the values.

# If we were to do this with a Tuple instead:
tupleExample = ("Sparkle", "Acheron", "Robin")
x = "THEN".join(tupleExample)

print(x)
# Output: SparkleTHENAcheronTHENRobin

```

### Slicing:
- [start:stop:step] // Very much like splice in JS. Step is defaulted to 1 but can be omitted.
- Stop number is not included due to zero basing.

```
S[3:11] // Indexes 0-3 will not be used, nor will anything after index 10. It is between these values.
# The step is like an iterator, so if we use 2 as the step count, it will get each other number
S[2: 9: 2] will produce 3, 5 and 7. It will not give 8 as 9 is the stopping point and we stop just before. 
```

## Booleans:

## Operators:

## Lists:

## Tuples:

## Sets:

## Dictionaries:

## Loops
### If Else:

### While:

### For:

## Functions:

## Lambdas:

## Arrays:

## Classes/Objects:

## Inheritance and Meta classes:

## Iterators:

## Polymorphism:

## Scope:

## Modules:

## Dates:

## Math:

## JSON:

## RegEx:

## PIP:

## Try...Except:

## User Input:

## String formatting:

## File Handling:

### CRUD:

## Modules:
### NumPy
### Pandas
### SciPy

## Matplotlib:
### The Basics:

### Pyplot:
### Plotting:
### Markers:
### Line:
### Labels:
### Grid:
### Subplot:
### Scatter:
### Histograms:
### Bars:
### Pies:

## Python with MySQL:
### Database Creation:
### Create Table:
### Insert:
### Select:
### Where:
### Order By:
### Delete:
### Drop Table:
### Update:
### Limit:
### Join:



