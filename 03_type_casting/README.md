All right, welcome back everybody. In this topic I'm going to explain type casting. Type casting is the process of converting a value of one data type to another. We can convert integers to floats. Floats to integers, strings to booleans, booleans to strings, floats to strings, strings to integers, integers to booleans. I think you get the idea, why might you want to use typecasting? When we get to the lesson on accepting user input, the user input is always a string. If somebody were to type in a number, and we need to perform math involving that number, we would want to convert it to either an integer or float. Another example is that if we had a floating point number, and we need to round that number to an integer. One possible way is to cast it as an integer. We can truncate the decimal portion.

There are two different ways we can do this, explicitly and implicitly.

```py
# typecasting = The process of converting a value of one data type to another.
#               (string, integer, float, boolean)
#               Explicit vs Implicit
```

Let's cover some explicit type casting. I have four variables. We need a string, let's say name, type in your first name. age, that's good. Float, how about a grade point average? GPA for short. my GPA will be a solid um 1.9, then we'll need a boolean, uh, what about student, are we a student, if we're a student, that would be true, if not, that would be false.

```py
name = "Bro"
age = 21
gpa = 1.9
student = True
```

Here's four variables of the four basic data types. We have a string, an integer, a float and a boolean.

If you ever need a data type of a variable, you can use the built-in type function. type the word type, followed by a set of parentheses. Place a variable within a set of parentheses, `type(name)`, however, when I run this, we can't see anything, so we need to place this stement within a print statement. I'm going to type print, add a set of parentheses. We will cut this line of code, and paste it within the print statement.

```py
print(type(name))
```

So we are printing the type of my variable name, `<class 'str'>` and that is str which means it's a string. Let's do that with age GPA and student, just so you're more familiar with using the type function. We have age, gpa, and student.

```py
print(type(name))
print(type(age))
print(type(gpa))
print(type(student))
```

Here we are, python says the data type of name is a string, str. age is an integer, int means integer. gpa is a float. Then student is bool, which means boolean.

```py
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
```

Let's do some explicit conversion. I need to convert my variable age into a floating point number. I could take my variable age, i could reassign this a value by using equals. Then I will explicitly cast age into a float by typing float, a set of parentheses. add my variable to be typecasted within the set of parentheses. Then let's print whatever age currently is. [Run]

```py
age = float(age)
print(age)
```

Look at that, age is now 21.0. You can tell it's a float, because it has a decimal portion. If I were to use that type function again. We can see what the data type of age is now.

```py
age = float(age)
print(type(age))
```

And my variable age is a floating point number: `<class 'float'`. That's how to cast a value as a float. You type float, add a set of parentheses. Place your value or variable within that set of parentheses. Then you may need to reassign it to something. Here we're just reassigning our variable age. [clear_2_lines]

We know how to convert a value to a float, let's try an integer. I'll convert my GPA into an integer. I'll take GPA, set this equal to type int, set of parentheses, place my variable within the parentheses.

```py
age = int(gpa)
print(gpa)
```

The I will print whatever my GPA is. my GPA is now 1. So an integer, it's a whole number, we can't contain that decimal portion, so it's truncated. That's how to convert a value into an integer.

Let's convert a value into a string. How about this boolean? So student, equals, to convert a value or variable into a string, type `str`, add a set of parentheses. Place your value or variable within that set of parentheses. Then let's print whatever our variable is after we reassign it. [run]

```py
student = str(student)
print(student)
```

So student still says true. It appears the same as it did before, but now it's treated as a series of characters, rather than a boolean. Just to prove to you that student is a string, let's use the type function and surround our student variable when we print it.

```py
student = str(strudent)
print(type(student))
```

Student is now a string`<class 'str'>`. So to convert a value or variable into a string. You can use the built-in string function, just type str, set of parentheses, add your value or variable, boom there you go. [clearn_2_lines].

All right, lastly, we can convert a value or variable into a boolean. So a boolean can only be true or false. What if we were to convert a number into a boolean? What would happen? So let's take age equals to cast the value or variable into a boolean. You type bool, set of parentheses, add your value or variable. I'll place age, within the set of parentheses. Then let's print whatever age is.

```py
age = bool(age)
print(age)
```

Do you think the result is going to be true or false? [Run]. Um, it's actually True. When converting a number to a boolean, if that number is anything but zero, it will always be true. Let's say age is like a million, well`age = 10000`, [Run], well, it's still going to be true. What about negative 1 million`age = -10000`? that is still True. But if age were zero`age = 0`, then it's false[5:31].

Why would casting something as a Boolean be useful? Let's say we ask a user to enther in their name, I need to check to see if they enthered in something. Let's type cast my name as a Boolean.

```py
name = bool(name)
print(name)
```

That is true, but if this was an empty string(`name = ""`), that would be false. Even a space registers as true(`name = " "`). Like I said, we could use typecasting to check to see if somebody typed in their name or not. If we cast the name as a Boolean, and it's true that means they typed in something. We'll have more practice with that later.

That is explicit typecasting. All explicit typecasting is manually converting a value or variable into a different data type, by using one of these cast keywords. We only covered four: strings, integers, floats and booleans. [Clear_all_code]

## Implicit typecasting

All right, now let's go over implicit typecasting. Implicit typecasting is when a value or variable is converted into a different data type automatically. For example, let's say we have x, x = 2. Then we have y, y equals, how about 2.0. What if I were to reassign x and set x equal to x divided by y. Well, we're dividing an integer by a float. So what's the result going to be? Is x going to be an integer or a float? So let's print whatever x is.

```py
x = 2
y = 2.0

x = x / y

print(x)
```

[Run], result is `1.0`. x is now a float even though we assigned it to be an integer originally, a whole number. So that's implicit typecasting. A variable's data type, can be converted when you perform certain operations on it. Such as arithmetic expressions like this(`x = x / y`).

All right everybody, so that is typecasting. It's the process of converting a value of one data type to another, you can convert strings to integers, integers to floats, floats to booleans, booleans to strings, any combination of those. And there's still more data types we didn't cover. But that's the general idea.

So that is typecasting. Hey, if you found this video helpful, please be sure to smash that like button. Leave a random comment down below and subscribe if you'd like to become a fellow bro.
