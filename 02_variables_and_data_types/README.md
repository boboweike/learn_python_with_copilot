Hey, what's going on everybody. In this topic I'm going to explain variables and data types in Python, as well as give you a few useful tips and tricks at the end of this topic. So why don't you sit back, relax, and enjoy the show.

## Variable

- A resuable container for storing a value
- A variable behaves as if it were the value it contains

Let's talk about variables. A variable is a reusable container for storing a value, a variable behaves as if it were the value it contains. Think back to algebra class back in the day, we have an equation that contains x, x is some representation of a value wherever we use x, it behaves as if it were a certain number, that's kind of the same thing with programming. Now when we crate a variable, we would like to give a descriptive and unique name of what that variable contains.

Suppose I'm working with a user's age, I could declare a variable named age. age equals then some value. Let's say my age is 21, not anymore, but I like to think it still is, guys I'm getting old. I can use this variable age and it will behave as if it were the number 21. To print a variable, you can place it within a print statement. pring(age). Run. My age is 21. If you're printing a variable, you don't need to put it within quotes, because what we're doing then is literally printing the word age and not the variable. If you need to display a variable along with some text, such as `You are age years old`, what we could do is string concatenation. Wherever you would like to include a variable, let's say here where ages, we can separate this line of text into different strings. You are, plus age, plus the text years old. [Run].

```py
age = 21

print("You are " + age + "years old")
```

So we do have an error here, type error, can only concatenate str (not "int") to str. We can't add numbers to strings directly. We would need to do what is called typecasting. To display a number along with some text, we would need to cast this variable which is a number into text, a string. To do that, we can precede the variable name with `str`, then surround the variable with a set of parentheses. If I were to run this again, this would display `You are21years old`.

```py
print("You are" + str(age) + "years old")
```

But you do have to pay attention to your spaces. I'm going to add a space after are, as well as before the word years. Run this again, you are 21 years old.

```py
print("You are " + str(age) + " years old")
```

Another way to display a variable along with some text, is to separate the text and variables in two separate arguements. print, then write our text within quotes, You are, whatever you would like to add a variable, add a comma, then the variable name, if you have more text that follows, add another comma, then add some additional text. "You are ", age, " years old".

```py
print("You are " + str(age) + " years old")
print("You are ", age, " years old")
```

So what we've done is separated our strings and variables into different arguments, each separated with a comma, but if you separate your variables and text into separate arguments, you'll include a space automatically. So I'm going to get rid of the space after are and before the word years. [Run].

```py
print("You are " + str(age) + " years old")
print("You are", age, "years old")
```

So spacing is pretty important depending on which method you use, these two print statements will output the same thing, `You are 21 years old`.

The third way to print a variable[3:21] along with some text, and this is becoming the more popular way of doing things is to use what is called an f-string. print, a set of quotes, precede your quotes with f. u r whatever you would like to insert a variable, add a set of curly braces. The curly braces are acting as a placeholder for a value or variable. We will place our variable age within the curly braces. [run]

```py
print("You are " + str(age) + " years old")
print("You are", age, "years old")
print(f"You are {age} years old")
```

So yeah, those are three different ways to output a variable along with some text. As of the filming of this video, fstrings are becoming much more popular for output. For the rest of the series, we will be using fstrings. But you should still be aware of the existence of these other two methods as well.

I need to discuss different data types, there's four basic data types in Python. There's still more but these are four for beginners.

- INTEGER
- FLOAT
- STRING
- BOOLEAN

We have integers, floats, strings and booleans. Let's begin with integers. We'll create 3 integer variables. For example, we have age, another whole number could be, maybe players, or users. You're are not going to have half a player right? or nine tenths of a player, it's going to be a while number. You have one two three or more players, all whole numbers. Then maybe quantity, maybe somebody is buying something quanity equals five, you wouldn't have like half a product right? It would be a whole number.

```py
age = 21
players = 2
quanity = 5
```

Then let's display some of these variables. print, we'll use fstrings, because we like fstrings. You are {age} years old. This is the same from the previous example.

```py
print(f"You are {age} years old")
```

Let's use players. There are {players}, then the word players online.

```py
print(f"There are {players} players online")
```

Then quantity, let's use this, You would like to buy, our variable {quantity} items.

```py
print(f"You would like to by {quantity} items")
```

Let's run this, `You are 21 years old`. `There are 2 players online`. `You would like to buy 5 items`.

So those are integers, they're just whole numbers. I'm going to turn these lines into comments, and then we can continue.

Let's move on to floats. A float is a number that contains a decimal portion. For example, maybe a GPA, that's usually a decimal. my GPA is 3.2. What about a distance? this could be kilometers miles whatever, 2.5 kilometers. Um price, price could be a float. price equals 10.99.

```py
gpa = 3.2
distance = 2.5
price = 10.99
```

Let's display some of these. print, let's print our gpa, You gpa is {gpa}. Let's print distance, you ran distance then I'll add km for kilometers. print, The price is, I'm going to add a dollar sign, then our placeholder, with price. And that should be good. [Run]

```py
print(f"Your gpa is {gpa}")
print(f"You ran {distance}Km")
print(f"The price is ${price}")
```

`Your gpa is 3.2`. `You ran 2.5Km`. `The price is $10.99`. So those are floats, they're numbers that contain a decimal portion, even if the decimal had point zero. It would still be considered a float. Whereas this(gpa = 3) would be an integer. So those are floats. I'm going to turn these lines into comments, then we can move on.

Now we have strings. A string is just a series of text. For example, maybe a username, name equals type in your first name, it's just a series of characters, those are strings. How about food, what's your favorite food? I like pizza. I'll add that to my variable food. Then what about email? email equals, make up some email, `Bro123@gmail.com`. Now with strings, they can contain numbers, but we treat them differently than integers and floats. Integers and floats we can use with arithmetic equations, here they're more or less just characters. So a string is just a series of characters within quotes, these can be sinple quotes or double quotes.

```py
name = "Bro"
food = "pizza"
email = "Bro123@gmail.com"
```

Then let's display these for pratice. Let's say: Hello, our variable name. You like, our variable food. Your email is our email variable. [Run]

```py
print(f"Hello {name}")
print(f"You like {food}")
print(f"You email is: {email}")
```

[8:37]`Hello Bro`, `You like pizza`, `Your email is: Bro123@gimail.com`. So those are strings, it's a series of text.

Okay, then lastly we have booleans. A boolean is either true or false, it's binary. It's kind of like a light switch. A boolean variable can have only one of two states, it's true or false. Typically booleans are used internally within a program. For example, maybe we have a boolean variable named online, if somebody is online, this can be set to true. If they're offline, it could be false, let's set that to true. What if something is for sale? `for_sale`, if it's available we could say true, if not, it's false. It only has two states. Then what about running, is some process running? Running equals true, or false.

```py
online = True
for_sale = False
running = True
```

Then let's print these. print, what could we say with oline? Are you online? then let's print our variable online. print, Is the item for sale? {for_sale}. print, perhaps running refers to a game, is the game running? Game running, colon space, our runing variable. [Run]

```py
print(f"Are you online?: {online}")
print(f"Is the item for sale? {for_sale}")
print(f"Game running: {running}")
```

So, `Are you online?: true`, `Is the item for sale?: False`, `Game running: True`.

Typically with booleans, you use these internally. It's not common to print them directly, usually we would use these with if statements. Such as if then the Boolean, if some process is running, print The game is running, else, print, The game is over. I'm just going to turn these into comments. [Run]

```py
if running:
    print("The game is running")
else:
    print("The game is over")
```

So if running is true, the game is running. If it's false, you would do something else. The game is over, but I'll discuss this more when we reach if statements, you don't need to know them at this point in time, just understand for now, a boolean is either true or false. Oh, here's another thing, a common mistake that people do with booleans is that they may put them within quotes.

```py
online = "True"
```

You can see that the color scheme changed. This is technically a string, it's within quotes. So that's a common mistake that people might make, if you're writing a boolean, make sure it's not within quotes. And the first letter is capital. [Clear_code]

Before I wrap things up, I'm going to show you a few tips and tricks with variables. Suppose we have 3 variables. x equals 1, y equals 2, z equals 3. Then I'll print these variables directly. print(x), print(y), print(z). [Run]. This would result in 1/2/3.

```py
x = 1
y = 2
z = 3

print(x)
print(y)
print(z)
```

Another possibility, in place of assigning these variables on separate lines, you could doe so all on one line. We could write x comma y comma z, equals, one comma two comma three, that would do the same thing, and it only takes one line of code. This is referred to as multiple assignment.

```py
x, y, z = 1, 2, 3

print(x)
print(y)
print(z)
```

If you ever need to set multiple variables to the same value, this is what you could do. I need to set x, y and z, all to zero, maybe they are coordinates or something. What I would instead type is x equals y, equals z, equals zero or some other value. [run]

```py
x = y = z = 0

print(x)
print(y)
print(z)
```

So x y and z are all zero. If were to change this number to 1, [Run], well, they all equal one. That's how to set multiple variables to the same value. variable one equals variable two equals, however many more variables you have.

All right everybody, those are variables, variable is a reuseable container for storing a value. A variable behaves as if it were the value it contains. We discussed for data types. Which are whole numbers. Floats, which are numbers that contain a decimal portion. strings, which are a series of text like a name or an email, and booleans which are either true or false. They are binary.

So yeah, that's an introduction to variables in python. In the comments section, why don't you post four variables. An integer, a float, a string and a boolean. Try and think of a unique example that I din't cover alreay. So yeah, those are variables in python.
