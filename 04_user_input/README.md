欢迎回来，今天我们学习如何获取用户输入，然后我们会做一些相关的练习。练习有三个，一个是 Mad Libs，一个计算矩形的面积，还有一个购物车程序。

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

我输入“波波”，"28"，结果能正常工作。

所以，当你获取用户输入的时候，你所获取到的总是字符串类型。如果你想把用户输入用作数学运算，那么你通常需要先把它转型成浮点数或者整数。以上就是如何获取用户输入的相关内容。下面我们来做一些练习题，巩固所学内容。

## 1. Mad Libs 游戏

第一个练习是`Mad Libs`游戏。在编程中，"Mad Libs" 程序通常指的是一个简单的程序，它会提示用户输入一系列词语，然后将这些词语插入到一个预设的故事模板中，生成一个新的、有趣的故事。这是一个非常适合初学者的项目，因为它可以帮助我们熟悉字符串操作和用户输入。

所以我们来设计一个故事，我使用 f 字符串。print, 今天我去了一个{adjective}动物园，`adjective`形容词用来形容事物的一种特性。这是怎样的一个动物园呢？一个高档的动物园，一个普通的动物园，一个脏兮兮的动物园，一个干净的动物园，这些就是形容词，它用来对名词进行形容。

```py
print(f"今天我去了一个{adjective}动物园。")
```

第二行，比方说，在一个展览中，我看到了{noun}，`noun`名次表示人，地点或事物。

```py
print(f"在一个展厅前，我看到了{noun}")
```

`{adjective}{noun}正在{verb}`。一个 verb 表示一个动作。看起来我需要两个形容词。我们将第一个形容词重命名为`adjective1`，第二个形容词重命名为`adjective2`。在动词`verb`前，我们加`正在`，表示当时正在进行时。

```py
print(f"{adjective2}{noun}正在{verb}")
```

再 print，我觉得太{adjective3}了，这边添加了第三个形容词。

```py
print(f"我觉得太{adjective3}了")
```

所以我们需要声明并给这些变量赋值。我们需要声明`adjective1`，`noun`，`adjective2`，`verb`，然后是`adjective3`。

```py
adjective1 =
noun =
adjective2 =
verb =
adjective3 =
```

我们要获取用户输入，input，请输入一个形容词。我们拷贝这一行，分别添加`adjective2`和`adjective3`。对于`noun`，input，请输入一个名词。对于`verb`，请输入一个动词。

```py
adjective1 = input("请输入一个形容词: ")
noun = input("请输入一个名词: ")
adjective2 = input("请输入一个形容词: ")
verb = input("请输入一个动词: ")
adjective3 = input("请输入一个形容词: ")
```

好，现在我们可以运行 Mad Libs 游戏了。[运行]。形容词描述一个人，地点或者事物的特性，比方说快，慢，这边我输入`神奇的`。输入一个名词，`马云`，名词就是一个人，地点或者事物。再输入一个形容词，`兴高采烈的`。再输入一个动词，动词表示正在做某个动作，比方说我输入`尖叫`。最后再输入一个形容词，`不可思议`。好，这就是我们创作的故事情节。

```py
今天我去了一个神奇的动物园。
在一个展厅前，我看到了马云。
兴高采烈的马云正在尖叫。
我觉得太不可思议了。
```

好，这就是我们的第一个练习。如果你创作了一个好玩的故事情节，记得贴在视频下方的评论区。

[Clear_all]

## 2 计算矩形面积

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
