Hey everybody, in this topic, I'm going to show you how we can accept some user input, then I have a few exercises for us to work on. We'll work on Mad Libs, a program to calculate the area of square, and a shopping cart program:

exercises:

- 1 mad libs
- 2 area calc
- 3 shopping cart

How do we accept user input? Well, we do so within our console window down here. The same we use for output. To accept some user input, we can use the input function. Within the set of parenthese, we can type a prompt to be displayed to the console window. Let's ask for somebody's name. Enter your name.

```py
input("Enter your name: ")
```

When I run this program, our program is paused in the console window until we type in something and hit enter. I'll enter my name, you can enter in your own name. Hit enter. But nothing appears to happen. We've accepted user input, but we should probably store the input somewhere. How about inside of a variable? I'll assign my variable name equal to the input that we receive. Our input will be stored within this variable, and then we can use it for something. So let's print whatever our name is, within a message. I'll use an F string, hello our variable name.

```py
name = input("Enter your name: ")

print(f"Hello {name}")
```

Let's try this again. Enter your name, I'll type in my first name. Hit enter. `Hello Bro`.

Let's ask for somebody's age this time. We'll create variable age, set this equal to input, then we'll need a prompt. Enter your age. Then we will print, using an f string, you are our variable age years old. [Run].

```py
name = input("Enter your name: ")
age = input("Enter your age: ")

print(f"Hello {name}")
print(f"You are {age} years old")
```

And to your name, I'll type my first name. And your age, I'll make up an age. Hello bro, you are 21 years old.

```py
Enter your name: Bro
Enter your age: 21
Hello Bro
You are 21 years old
```

When we accept user input, the input is always of the string data type. What if I were to increase my variable age by one. age equals age plus one.

```py
name = input("Enter your name: ")
age = input("Enter your age: ")
age = age + 1
print(f"Hello {name}")
print(f"You are {age} years old")
```

This is what would happen. `Bro`, `21`. Uh, we have a type error. Can only concatenate strings, not integers to strings. If i accept user input, and I need to use it for any sort of math, I would want to type cast that input as either an integer or a float. Based on the previous lesson on typecasting, we could write age, equals, I'll type cast my age which is a string into an integer. [run]

```py
name = input("Enter your name: ")
age = input("Enter your age: ")
age = int(age)
age = age + 1
print(f"Hello {name}")
print(f"You are {age} years old")
```

So type in your first name, and age, and that appears to work. Uh, however, I like to do this involving one line of code, in place of adding an additional line, we're typecasting. I'll take the user input and place this function within a type cast. I'll type int, then surround the input function with the set of parentheses. Then that only takes one line of code.

```py
name = input("Enter your name: ")
age = int(input("Enter your age: "))
age = age + 1
print(f"Hello {name}")
print(f"You are {age} years old")
```

So `Bro`, `21`, there we go, that also works. If we were to type cast our input as a float[3:05]
