# String Interpolation

## Objectives

1. Use string formatting using the `.format()` function
2. Use string interpolation using `%`.

## String Formatting and Interpolation
String interpolation lets us pass different data into a string, which is faster and more convenient than keeping track of different pieces of string and concatenating them ourselves. There are two ways to do string interpolation: With the `.format` method and with `%`. Let's take a look at the difference.

### Interpolation with **`.format()`**
This is the newer version of using variables within strings in Python. The method `.format()` is chained to the end of a string. The arguments of `.format()` are substituted into the placeholders of the string. The placeholders start and end with curly brackets. The placeholders can contain a named variable, a number, or nothing at all.

#### Keyword Variables

For readability, keyword variables generally make the most sense in interpolation placeholders. In the example below, the string has one keyword argument, 'reading_materials', which is assigned to a global variable, 'magazine'.
```python
>>>magazine = "The Atlantic"
>>> "I am always behind on {reading_material}".format(reading_material=magazine)
'I am always behind on The Atlantic'
```
The hobby example uses two keyword arguments: 'name' and 'hobby', which are assigned to strings within .format()
```python
>>>"{name} is the best at {hobby}".format(name='Charlie', hobby='playing piano')
'Charlie is the best at playing piano'
```
#### Positional Variables
There is also an option to use positional arguments. The advantage is that this is  a bit shorter to type, but harder for others to interpret.
```python
>>>"There are {0} students at CSSI in {1}!".format(30, "New York")
'There are 30 students at CSSI in New York!'
```

You could also not include any value in the placeholder and achieve the same effect.
```python
>>>"There are {} students at CSSI in {}!".format(28, "Cambridge")
'There are 28 students at CSSI in Cambridge!'
```

### String Interpolation with ***%s***
The older way to use variables in strings and uses the % operator.

```python
>>> "The %s have %d %s championships in %d years" %("Chicago BlackHawks",3, "NHL", 3)
The Chicago Black Hawks have 3 NHL championships in 3 years
```

Again, you'll note that our whole string is in quotes. 

The placeholder for the variable is the `%` sign and a letter showing the datatype that is being inserted. The entire string is followed by a percent sign and the data that is being inserted, separated by commas. 

```python
>>> "The %s have %d %s championships in %d years" %("Chicago BlackHawks",3, "NHL", 3)
The Chicago Black Hawks have 3 NHL championships in 3 years
```

# References
[Python String Interpolation Guide] (https://mkaz.com/2012/10/10/python-string-format/)



