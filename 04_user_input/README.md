欢迎回来，今天我们学习如何获取用户输入，然后我们会做一些相关的练习。练习有三个，一个是 Mad Libs，一个计算正方形面积，还有一个购物车程序。

三个练习:

- 练习一, mad libs
- 练习二, 面积计算
- 练习三, 购物车

那么我们该如何接收用户输入呢？其实，我们是通过控制台窗口输入的，当然输出也是在控制台窗口。为了接受用户输入，我们要使用`input`函数。在这对括号中，我们可以给一个输入提示。比方说，我们要求用户输入名字，请输入你的名字。

```py
input("请输入你的名字：")
```

当我运行这个程序，程序会停在这边，控制台提示用户输入。我输入我的名字`波波`，回车。结果没有输出。我们接收了用户输入，但是我们应该把用户的输入存在某个变量中。我们用户输入存在`name`变量中。然后我打印输出这个变量，使用 f 字符串，`你好{name}`。

```py
name = input("请输入你的名字: ")

print(f"你好{name}")
```

再次运行，请输入你的名字，"波波"，回车，结果输出`你好波波`。

我们再让用户输入年龄。我们新建一个变量 age，它等于 input，然后加一个提示，请输入你的年龄。然后我们使用 f 字符串打印输出：`你的年龄是{age}岁`。运行。

```py
name = input("请输入你的名字: ")
age = input("请输入你的年龄: ")

print(f"你好{name}")
print(f"你的年龄是{age}岁")
```

我输入我的名字，波波，然后是我们的年龄，假设我 28 岁。回车，结果输出，你好波波，你的年龄是 28 岁。

```sh
请输入你的名字: 波波
请输入你的年龄: 28
你好波波
你的年龄是28岁
```

当我们接收用户输入的时候，用户输入的总是字符串数据类型。假设我们要讲年龄加一岁，age = age + 1。

```py
name = input("请输入你的名字: ")
age = input("请输入你的年龄: ")
age = age + 1
print(f"你好{name}")
print(f"你的年龄是{age}岁")
```

这次的运行结果会怎样呢？我输入`波波`,`28`。结果显示有一个类型错误。只能由字符串相互拼接，整数不能和字符串不能直接拼接。如果我接收一个用户输入，然后我要对它做一些数学运算，那么我就需要将输入转成一个整数或者浮点数。根据我们之前学过的类型转型，我们可以写 age，等于，然后我要把字符串形式的 age 转成一个整数。再运行。

```py
name = input("请输入你的名字: ")
age = input("请输入你的年龄: ")
age = int(age)
age = age + 1
print(f"你好{name}")
print(f"你的年龄是{age}岁")
```

然后我输入名字，年龄，结果可以正常输出。当然我还可以简化一下代码，我把这行(`age = int(age)`)去掉，我们可以直接对用户输入进行转型，也就是对这个 intput 的输出直接进行转型。我输入`int`，再将 input 函数用括号括起来，这样我就只需要一行代码。在运行。

```py
name = input("请输入你的名字: ")
age = int(input("请输入你的年龄: "))
age = age + 1
print(f"你好 {name}")
print(f"你的年龄是{age}岁")
```

我输入“波波”，"28"，结果能正常工作。如果我把用户输入转型成一个浮点数。

well then my input would be a floating point number. It has that decimal portion.

So, when you accept user input, it's always of the string data type. If you are going to use your input with any sort of math, you'll probably want to typecast it as either a float or an integer. And that's how to accept user input. Let's go over a few exercises.

## 1. mad libs

The first we'll create a Mad Libs game. [Clearl_all]. All right everybody, for our first practice program, we're going to create a Mad Libs game. Mad Libs is where you have a story but the user gets to submit nouns, verbs and adjectives within your story. So let's think of a story, feel free to come up with your own, I'll use f strings. print, today I went to a, we'll insert an adjective here, an adjective is a quality of a thing, zoo. So what kind of zoo, an expensive Zoo, a cheap Zoo, a dirty Zoo, a clean Zoo, that's an adjective, it's a quality of a noun.

```py
print(f"Today I went to a {adjective} zoo.")
```

Our second line, let's say is, in an exhibit, I saw, then a noun, a noun is a person placer thing.

```py
print(f"In an exhibit, I saw {noun}")
```

Our noun was, then an adjective, and a verb. A verb is an action, I would like two different adjectives. Let's rename this first adjective as adjective one, the second adjective will be adjective two. After our verb, I'll add ing that means that this verb is current tense. It's currently happening.

```py
print(f"{noun} was {adjective2} and {verb}ing)
```

print, this will be an f string, I was, then let's add a third adjective, adjective three. We just need to declare and assign these variables.

```py
print(f"I was {adjective3}")
```

We hav adjective1, our noun, adjective2, our verb, then adjective3.

```py
adjective1 =
noun =
adjective2 =
verb =
adjective3 =
```

We'll accept user input, input will ask the user to enter an adjective. Let's copy this line, add that to adjective2, and adjective3. For noun, we'll input, Enter a noun. Our verb will be, Enter a verb.

```py
adjective1 = input("Enter an adjective: ")
noun = input("Enter a noun: ")
adjective2 = input("Enter an adjective: ")
verb = input("Enter a verb: ")
adjective3 = input("Enter an adjective: ")
```

All right, we're ready to run our Mad Libs game. [Run]. An adjective describes a quality of a person place or thing, like fast, slow, uh, what about suspicious? or I'll just say sus for short. Enter a noun, Mark Zuckerberg, a noun is a person Placer thing. Enter an adjective, berserk. Enter a verb, a verb is an action, how about screech? Enter an adjective, amazed. All right, here's our story.

```py
Today I want to a sus zoo.
In an exhibit, I saw Mark Zuckerburg.
Mark Zuckerburg was bersert and screeching
I was amazed
```

All right, that is our first exercises. I'd like to see what you wrote, post your results in the comment section down below, because I would like to read it. [Clear_all]

## 2 area calc

All right, let's move on to the second exercise. For this next exercise, we will calculate the area of a rectangle. We'll need two variables, length and width. We'll take length equal to accept some user input, Enter the length of a rectangle. Then we'll need th width. width, Enter the width of a rectangle. We will take our area variable, set this equal to length times width, then let's display whatever the area is. The area is, colon space, I'll insert our area variable, depending on the unit of measurement, you can set this two inches, centimeters or something else. I'll just say centimeters. I believe that centimeters squared technically. Okay, let's try it.

```py
length = input("Enter the length of a rectangle: ")
width = input("Enter the width of a rectangle: ")

area = length * width

print(f"The area is: {area}cm^2")
```

The length will be 9, the width is 15. We have a problem, type error, `can't multiply sequence by non-int of type 'str'. What we're missing here is we need to typecast our user input as either a floating point number or an integer. We're using these variables in arithmetic equations. So let's typecast our length and our width as a floating point number. Let's try this again.

```py
length = float(input("Enter the length of a rectangle: "))
width = float(input("Enter the width of a rectangle: "))

area = length * width

print(f"The area is: {area}cm^2")
```

```sh
Enter the length of a rectangle: 9,
Enter the width of a rectangle: 15,
The area is: 135.0cm^2
```

Hey, if this were a 3D rectangle, we could add height, height equals, I'm going to copy all this, enter the height of a rectangle. Volume equals length times width, times height. The volume is our volume centimeters cubed technically. [Run].

```py
length = float(input("Enter the length of a rectangle: "))
width = float(input("Enter the width of a rectangle: "))
height = float(int("Enter the height of a rectangle: "))

volume = length * width * height

print(f"The area is: {volume}cm^3")
```

9, 15, 7, I'm just making up numbers here. The volume is 945.0 centimeters cubed.

All right, that is the second exercise. We have calculated, well, I guess both the area of a rectangle, and the volume of a three-dimensional rectangle.

## 3 shopping cart

Okay, we have one more exercise. A shopping cart program. We have 3 variables, item, a price of the item, then a quanity.

```py
item =
price =
quanity =
```

We'll ask the user what item they're buying. input, what item would you like to buy? Then a price, input, What is the price? Then a quantity, input, how many would you like? If we're working with a string, we don't need to do any type casting.

```py
item = input("What item would you like to buy?: ")
price = float(input("What is the price?: "))
quanity = input("How many would you like?: ")
```

a price, with a price that could include a decimal, we should type cast our input as a floating point number. I'll surround our input with a type cast to a float. And with a quantity those are typically integers, they're whole numbers, I'll type cast our input as an integer.

```py
item = input("What item would you like to buy?: ")
price = float(input("What is the price?: "))
quanity = int(input("How many would you like?: "))
```

So surround our input with an int cast. Then we can do some calculations. total, equals, our price multiplied by our quantity. Then we'll display a message to the user. print, we'll use an f string, You have bought, our quantity variable, times, whatever the item is that we're trying to buy. Then I'll add slash s, because they might buy more than 1 items. Then we'll display the total. Your total is colon space, then our total. I should probably precede the total with some currency, maybe a dollar sign.

```py
item = input("What item would you like to buy?: ")
price = float(input("What is the price?: "))
quanity = int(input("How many would you like?: "))

total = price * quanity

print(f"You have bought {quantity} x {item}/s")
print(f"Your total is: ${total}")
```

Okay, let's run this program. What item would you like to buy? I would like to buy a pizza. What's the price? Maybe a pizza is 4.99. How many would like to buy, I would like to buy nine 9 pizzas.

All right, here is the total 44.91, we can truncate everything up to two decimal places, and here's how. There is a built-in round function, I'm going to surround our total within a round function. Then after our variable, I'll add comma, then the amount of decimal places to round to. Let's try this again.

```py
item = input("What item would you like to buy?: ")
price = float(input("What is the price?: "))
quanity = int(input("How many would you like?: "))

total = price * quanity

print(f"You have bought {quantity} x {item}/s")
print(f"Your total is: ${round(total, 2)}")
```

Let's try this again. What item would like to buy? a pizza. the price is 4.99. How many would like to buy? I'd like nine pizzas, your total is 44.91. Like I said, to truncate everything after two decimal places, you could use the built-in round function, then set teh amount of decimal places you would like to round to.

All right everybody, that is the third exercise, we have made a small shopping cart program.
