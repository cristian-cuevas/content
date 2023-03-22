---
title: "How to concatenate Strings on Python"
subtitle: "On how to concatenate Strings in Python we explore different ways to concatenate and your choosing will depend on your style and needs."
tags: ["python"]

---


 
String concatenation is the process of adding two strings together in one. The easiest way to concatenate strings in Python would be to use the **format string** method. This method consists on adding the letter "f" before the string quote marks like this `f"Hello world"` , then you can concatenate variables by calling them between brackets `{}` inside the string quote marks. Here is an example of how to use it:

```python 
name = "4Geeks"

print(f"Hello from {name}!")
#Output -> Hello from 4Geeks!
```

In the previous example, we are using the variable `name` to concatenate it to the string.

String concatenation is a common action we, as [software developers](https://4geeksacademy.com/us/coding-bootcamps/part-time-full-stack-developer), have to deal with in almost any project. There are many ways you can concatenate strings, you can use any of them so pick the one that suits you the most.

## Concatenate strings on Python using the + operator

The most familiar way to concatenate strings for most people is the `+` operator. Check this example that explains how it works:

```python
name = "Alex"

print("Hello my name is " + name +  " and I'm a developer")
#Output-> Hello my name is Alex and I'm a developer
```

> Notice the space after `is` and before `and` , if we didn't added them, then the output would have looked like this: `Hello my name isAlexand I'm a developer`. Remember to add the spaces when needed.

## Concatenate strings using the += operator

We can use the += Operator to concatenate strings as well, it's pretty similar to using the `+` Operator, but different since what we are concatenating will modify the value of the original string.

```python
#Concatenate using the += operator
text = "Python"
str1 = "<3"
text+= str1
print(text)
#Output-> Python<3
```

Since we are "adding" string values to our variable **text**, these values will be concatenated as they are, no space will be automatically added.

### Concatenate an int or float value with text with str()

Numbers and strings are data type completely different. When we want to add a number (int, float, etc) to a string, we will need to use the `str()` to convert that number.

```python
#Concatenate using the + Operator with numbers
str1 = "Geeks"
int1 = 4
print("At " + str(int1) + " " + str1 +  " Academy we love Python! <3")
#Output-> At 4 Geeks Academy we love python! <3
```

As stated above, we are adding spaces for the render to respect writing rules (all words and numbers separated from one another).

If we would not convert the `int1` number variable to a **string**, we would receive the following error letting you know you are trying to concatenate an Integer with a String.

```python
TypeError: can only concatenate str (not "int") to str
```


## Concatenate strings on Python using the f-Strings

Python f-Strings (formatted string literals) makes writing strings in a more clear and understanding way for humans. This option was [introduced on Python](https://4geeks.com/lesson/intro-to-python) 3.6 so keep in mind backward compatibility when using it.

This is one of the most used methods among experienced developers because of the ease to insert `variables` into the **square brackets**. The variable(s) will be evaluated and a string representation will be displayed. 

Implementation: 

```python
#Concatenate using the f-Strings method
str1 = "Geeks"
print(f"Showing the str1 variable: {str1} using f-String")
#Output-> Showing the str1 variable: Geeks using f-String
```

Making use of the `f-Strings` concatenation, we don't need to convert numbers (Int, Float, etc) to string to be able to display them inside the curly brackets.

```python
#Concatenate using the f-Strings method with numbers 
str1 = "Geeks"
int1 = 4
print(f"At {int1} {str1} Academy we love Python! <3")
#Output-> At 4 Geeks Academy we love python! <3
```

## Concatenate using .format()

Another way to concatenate in Python is by making use of the `format()` method. It works similar to `f-Strings` since they both use curly brackets `{}` to insert variables but is available from version 2.7.

This method doesn't need for the number values to be converted into strings.

```python
#Concatenate using the .format() method
str1 = "Geeks"
str2 = "Academy"
int1 = 4
text = "{}{}{}".format(int1, str1, str2)
print(text)
#Output-> 4GeeksAcademy
```

As you can see, the result returned is the expected, but with spacing between words.

## Concatenate using % operator

The `%` operator is an older way to concatenate strings that work very similar to the '.format()` method. We use `%s` as placeholders for different values, as we did with the curly brackets in previous examples.

```python
#Concatenate using the % Operator
str1 = "Geeks"
str2 = "Academy"
int1 = 4
text = "%s%s%s" % (int1, str1, str2)
print(text)
#Output-> 4GeeksAcademy
```

## Concatenate using the * Operator 

The use of the `*` Operator is not a concatenation in the way we have been doing so far. The `*` Operator is used for multiplication and that's exactly what it does, multiplying for the amount given the string.

```python
#Concatenate using the * Operator
str1 = "4 Geeks Academy "
print(str1*3)
#Output-> 4 Geeks Academy 4 Geeks Academy 4 Geeks Academy 
```

If you format the **string** variable correctly (leaving a space at the end of the sentence/word), this is the best way to repeat a line of text as many times as you may need.


You can read more related topics at [4Geeks](https://4geeks.com/lesson/intro-to-python). Hope you enjoyed the reading and keep on the Geek side!