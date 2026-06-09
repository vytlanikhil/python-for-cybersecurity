# python-for-cybersecurity

My first code: 

```python
import requests
response=requests.get('https://google.com/')

print(response.text)
if(response.status_code==200):
 response=requests.get('https://google.com/admin.php')
 if(response.status_code==200):
  print(response.status_code)
  print("vulnerable site")
 else:
  print(response.status_code)
  print("not vulnerable")
else:
 print("invalid url")

```

when i have typed and executed my first code i can understand the logic,because i know other coding languges like java,c. But when i am typing the code my own,it gives lots of indentation errors ,So i started to prepare python core first to understand indentation and for to handel exceptions

# **Python core**

---

```python
print("hello cyber world")
print("This is my first python program")
```

#### Variables in python:

variable - a container for a value, which can be changed later on (int, float, str, bool)
A variable behaves as if it was the value that it contains. The value can be of any type, and can be changed as needed.

```python
# String - a sequence of characters, enclosed in quotes (single or double)
first_name = "bro"
food = "pizza"
email= "bro@gmail.com"

print(f"My name is {first_name}")
print(f"My favorite food is {food}")
print(f"My email address is {email}")

# Integer - a whole number, positive or negative, without decimals
age = 21
quantity = 3
no_of_students = 30

print(f"I am {age} years old")
print(f"I have {quantity} items")
print(f"There are {no_of_students} students in the class")

# Float - a number with a decimal point
price = 9.99
temperature = 36.5
pi = 3.14
print(f"The price is ${price}")
print(f"The temperature is {temperature} degrees Celsius")
print(f"The value of pi is {pi}")

# Boolean - a value that can be either True or False
is_student = True
for_sale = True
is_online = False
print(f"Is the person a student? {is_student}")
print(f"Is the item for sale? {for_sale}")
print(f"Is the person online? {is_online}")

if is_student:
    print("you are a student")
else:
    print("you are not a student")

if for_sale:
    print("That item is for sale")
else:
    print("That item is not for sale")

if is_online:
    print("you are online")
else:
    print("you are offline")
```

#### Typecasting:

```python
#Typecasting - Converting a variable from one data type to another data type is called typecasting.
# str(), int(), float(), bool() are the built-in functions used for typecasting in Python. 

Name="nikhil"
age=20
gpa=8.7
ia_student=True

print(gpa) #Output: 8.7
gpa=int(gpa) #Typecasting float to int
print(gpa) #Output: 8

print(age) #Output: 20
age=float(age) #Typecasting int to float
print(age) #Output: 20.0

age=str(age) #Typecasting float to str
print(age) #Output: 20.0
#if we do age++, it will give an error because age is now a string and we cannot perform arithmetic operations on strings.
#but we can concatenate strings using the + operator. age=age+" years old"
age=age+" years old"
print("Name: "+Name)
print(age)

Name=bool(Name) #Typecasting str to bool
print(Name) #Output: True, because non-empty strings are considered True in Python.
Name=str(Name) #Typecasting bool to str
print(Name) #Output: True, because the boolean value True is converted to the string "True".
```

```python
age=20
name="nikhil"
#type() function is used to find the data type of a variable
print(type(age))
print(type(name))
```

#### input function - input() :

```python
# input() function is used to take input from the user. It reads a line from the input, converts it into a string (stripping a trailing newline), and returns that.

name = input("Enter your name: ")
age = input("Enter your age: ")

print(f"your name is {name}")
print(f"your age is {age}")

#here we cant do age=age+1 because age is a string and we cant add 1 to a string so we have to convert it into an integer first
# we cane do age=int(age) and then we can add 1 to it

age = int(age)
age = age + 1
print(f"your age after 1 year will be {age}")
```

#### Exercise 1:

```python
#area of rectangle
length=float(input("enter the length of rectangle: "))
breadth=float(input("enter the breadth of the rectangle: "))
area=length*breadth
print(f"the area of the rectangle is: {area}")
```

#### Exercise 2:

```python
item=input("enter the item you want to buy: ")
price=float(input("Enter the price of your item: "))
quantity=int(input("enter the no of items you need: "))

cost=price*quantity

print(f"item {item} | price {price} | quantity {quantity} = total {cost}")
```

#### Madlibs game:

```python
# Madlibs game
# word game where you create a story
# by filling in blanks with random words

adjective1 = input("Enter an adjective (description): ")
noun1 = input("Enter a noun (person, place, thing): ")
adjective2 = input("Enter an adjective (description): ")
verb1 = input("Enter a verb ending with 'ing': ")
adjective3 = input("Enter an adjective (description): ")

print(f"Today I went to a {adjective1} zoo.")
print(f"In an exhibit, I saw a {noun1}")
print(f"{noun1} was {adjective2} and {verb1}")
print(f"I was {adjective3}!")
```

#### Maths and arithmetic:

```python
friends=5
# friends = friends + 1 # friends += 1
# friends = friends - 2 -
# friends -= 2
# friends = friends * 3
# friends *= 3
# friends = friends / 2
# friends /= 2
# friends = friends ** 2
# friends **= 2
remainder = friends % 2
print(remainder)
```

```python
#math library usage
import math
x = 9.9
# print(math.pi) 
# print(math.e)
# result = math.sqrt(x) 
# result = math.ceil(x)
result = math.floor(x)
print(result)
```

#### Circumference of a circle:

```python
import math
radius=float(input("enter the radius of a circle:"))
circumference=2*math.pi*radius
print(f"The circumference of circle is {round(circumference,2)}")
```

#### Area of the circle:

```python
import math
radius=float(input("enter the radius of a circle:"))
area=math.pi * pow(radius,2)
print(f"The area of the circle is {round(area,2)}")
#round function rounds the values
```

#### Pythagores theorem:

```python
#pythagores theorem a²+b²=c²
import math
a=float(input("Enter length of A:"))
b=float(input("Enter length of B:"))
c=math.sqrt(pow(a,2)+pow(b,2))
print(f"The length of C is {c}")
```

#### If Else Statements:

```python
age=int(input("Enter your age"))
if age>=100:
    print("You are too old to sign up")
elif age >=18:
    print("you are now signed up!")
elif age<0:
    print("you are not born yet")
else:
    print("you should be 18+ to be signed up")
```

```python
response=input("Do you want some food? (Y/N)")
if response=="Y":
    print("Have some food!")
else:
    print("No food for you")
    #what ever you typed other than 'Y' it goes to else
```

```python
name=input("Enter your name:")
if name=="":
    print("You did not entered your name yet!")
else:
    print(f"welcome {name}")
```

```python
for_sale=True
if for_sale:
    print("This item is for sale")
else:
    print("This is not for sale")

```

```python
is_online=False
if is_online:
    print("He is online")
else:
    print("He is not online")
```

#### Calculator Program:

```python
#python calc program
num1=float(input("Enter number 1:"))
num2=float(input("Enter number 2:"))
operator=input("Select operator + - * /: ")

if operator=="+":
    print(f"The sum is {round(num1+num2,3)}")
elif operator=="-":
    print(f"The difference is {round(num1-num2,3)}")
elif operator=="*":
    print(f"The product is {round(num1*num2,3)}")
elif operator=="/":
    print(f"the result is {round(num1/num2),3}")
else:
    print("You selected worng option")

```

#### weight converter:

```python
#1kg=2.205 lbs so,1Lb=1kg/2.205 
weight=float(input("Enter your weigth: "))
unit=input("Enter kg or Lbs (L/K): ")
if unit=='K':
    res=weight*2.205
    unit="Lbs"
    print(f"you are {res} {unit}")
elif unit=="L":
    res=weight/2.205
    unit="kgs"
    print(f"you are {res} {unit}")
```

#### Temperature Converter:

```python
temperature=float(input("Enter the temperature: "))
scale=input("Enter celsius or Fahrenheit (C/F)")
if scale=="C":
    res=32+(temperature*(9/5))
    print(f"your weight in F is {round(res,2)}")
elif scale=="F":
    res=(temperature-32)*5/9
    print(f"your weight in C is {round(res,2)}")
else:
    print("Invalid option,Enter C/F")
```

#### logical operators:

```python
#logical operators = evaluates multiple conditions (or,and,not)
#Or=atleast one condition must be true
#And=both conditions must be true
#Not=inverts the condition (not true,not false)

temp=float(input("Enter the temperature"))
is_raining=True
if temp<0 or temp>35 or is_raining:
    print("The event is cancelled")
else:
    print("Event is still sheduled")
    
```

```python
temp = float(input("Enter the temperature: "))
is_sunny = True

if temp >= 28 and is_sunny:
    print("It is HOT outside 🥵")
    print("It is SUNNY ☀️")

elif temp <= 0 and is_sunny:
    print("It is COLD outside 🥶")
    print("It is SUNNY ☀️")

elif 28 > temp > 0 and is_sunny:
    print("It is WARM outside 🙂")
    print("It is SUNNY ☀️")

elif temp >= 28 and not is_sunny:
    print("It is HOT outside 🥵")
    print("It is CLOUDY 🌥️")

elif temp <= 0 and not is_sunny:
    print("It is COLD outside 🥶")
    print("It is CLOUDY 🌥️")

elif 28 > temp > 0 and not is_sunny:
    print("It is WARM outside 🙂")
    print("It is CLOUDY 🌥️")
```
#### Conditional expressions:

```python
#conditional expression = A one-line shortcut for an if else statement (ternary operator)
#                         print or assign ONE OF TWO VALUES depending on the condition
#                         X if condition else Y
num = 5
a=6
b=7
temperature = 15
user_role = "admin"

#print("positive" if num > 0 else "negative")
#result= "even" if num % 2 == 0 else "odd"

# max_num = a if a > b else b
# min_num = a if a < b else b
# print(f"max: {max_num}")
# print(f"min: {min_num}")

# status="adult" if num >= 18 else "minor"
# print(status)
# weather= "hot" if temperature >= 30 else "cold"
# print(weather)

access_level = "full access" if user_role == "admin" else "limited access"
print(access_level)
```

#### String Methods:

```python
name=input("enter your full name: ")

#result=len(name)
#len(name) is the function to calculate the length of the name

# result=name.find("o")
#find() is the function to find the index of the first occurrence of a specified value. In this case, it will find the index of the first "o" in the name

#result=name.rfind("o")
#rfind() is the function to find the index of the last occurrence of a specified value. In this case, it will find the index of the last "o" in the name
#if there are no "o" in the name, it will return -1

#name=name.capitalize()
#capitalize() is the function to capitalize the first letter of the name and make the rest of the letters lowercase

# name=name.upper()
#upper() is the function to convert all the letters in the name to uppercase

# name=name.lower()
#lower() is the function to convert all the letters in the name to lowercase

# name.isdigit()
#isdigit() is the function to check if all the characters in the name are digits. It will return True if all characters are digits, otherwise it will return False

# result=name.isalpha()
#isalpha() is the function to check if all the characters in the name are alphabetic

# phone_number="1-234-567-8901"
# result=phone_number.count("-")
#count() is the function to count the number of occurrences of a specified value. In this case, it will count the number of "-" in the phone number
# print("the number of '-' in the phone number is: ",result)

# phone_number="1-234-567-8901"
# phone_number=phone_number.replace("-","")
# #replace() is the function to replace a specified value with another value. In this case, it will replace all the "-" in the phone number with an empty string, effectively removing them
# print("the phone number without '-' is: ",phone_number) 

```

#### Username Exercise:

```python
# validate user input exercise
# 1. username is no more than 12 characters
# 2. username must not contain spaces
# 3. username must not contain digits

username = input("Enter a username: ")

if len(username) > 12:
    print("Username must be no more than 12 characters.")
elif not username.find(" ") == -1:
    print("Username must not contain spaces.")  
elif not username.isalpha():
    print("Username must not contain digits.")
else:
    print(f"Welcome '{username}'.")
```

#### Indexing:

```python
#indexing = accessing elements of a sequence by their position using []
#           [start:stop:step]

credit_number="1234-5678-9012-3456"
# print(credit_number[0]) #1
# print(credit_number[5]) #-
# print(credit_number[-1]) #6
# print(credit_number[0:4]) #1234
# print(credit_number[5:9]) #-567
# print(credit_number[::2]) #1357902468

last_four_digits=credit_number[-4:]
print(last_four_digits) #3456

#to reverse a string we can use slicing with a step of -1
print(credit_number[::-1]) #6543-2109-8765-4321

```

#### format specifiers:

```python
# format specifiers = {value:flags} format a value based on what
#                              flags are inserted

# .(number)f = round to that many decimal places (fixed point)
# :(number) = allocate that many spaces
# :03 = allocate and zero pad that many spaces
# :< = left justify
# :> = right justify
# :^ = center align
# :+ = use a plus sign to indicate positive value
# := = place sign to leftmost position
# :  = insert a space before positive numbers
# :, = comma separator

price1=3.14159
price2=-9870.65
price3=1200.34

print(f"price 1 is {price1 :.1f}")
print(f"price 2 is {price2 :.2f}")
print(f"price 3 is {price3 :.3f}")
#.1f rounds to 1 decimal place, .2f rounds to 2 decimal places, .3f rounds to 3 decimal places

print(f"price 1 is {price1 :10}")
print(f"price 2 is {price2 :10}")
print(f"price 3 is {price3 :10}")
#10 allocates 10 spaces for the value of price1, which is right justified by default

print(f"price 1 is {price1 :010}")
#10 allocates 10 spaces and 0 pads with zeros instead of spaces

print(f"price 2 is {price2 :<10}")
print(f"price 3 is {price3 :<10}")  
#< left justifies the value within the allocated spaces

print(f"price 2 is {price2 :>10}")
print(f"price 3 is {price3 :>10}")
#> right justifies the value within the allocated spaces

print(f"price 2 is {price2 :^10}")
print(f"price 3 is {price3 :^10}")
#^ center aligns the value within the allocated spaces

print(f"price 1 is {price1 :+}")
print(f"price 2 is {price2 :+}")
# + adds a plus sign to indicate positive values

print(f"price 1 is {price1 : ,}")
print(f"price 2 is {price2 : ,}")
print(f"price 3 is {price3 : ,}")
# , adds a comma separator for thousands

print(f"price 1 is {price1 :+,.2f}")
print(f"price 2 is {price2 :+,.2f}")
print(f"price 3 is {price3 :+,.2f}")
# combines multiple format specifiers: + adds a plus sign for positive values, , adds a comma separator for thousands, and .2f rounds to 2 decimal places
```

#### While loop:

```python
#while loop-executes a block of code as long as a specified condition is true

name=input("enter your name: ")

while name=="":
    print("you did not enter your name")
    name=input("enter your name: ")
print("hello "+name)
```

```python
age=int(input("Enter your age: "))

while age<0:
    print("Invalid age. Please enter a non-negative number.")
    age=int(input("Enter your age: "))
print("Your age is: ", age)
```

```python
food=input("What is your favorite food? ")
print("enter q to quit")

while not food=="q":
    print("I like "+food+" too!")
    food=input("What is your favorite food? ")
    print("enter q to quit")

print("Goodbye!")
```

```python
num=int(input("Enter a number between 1 and 10: "))

while num<1 or num>10:
    print(f"The number {num} is invalid. Please enter a number between 1 and 10.")
    num=int(input("Enter a number between 1 and 10: "))
print(f"The number {num} is valid.")
```

#### compound intrest calculator:

```python
#compound intrest calculator
principal = 0
rate = 0
time = 0

while principal<=0:
    principal = float(input("Enter the principal amount: "))
    if principal<=0:
        print("Principal amount must be greater than 0. Please try again.")

while rate<=0:
    rate = float(input("Enter the interest rate (as a decimal): "))
    if rate<=0:
        print("Interest rate must be greater than 0. Please try again.")

while time<=0:
    time = float(input("Enter the time (in years): "))
    if time<=0:
        print("Time must be greater than 0. Please try again.")

total=principal*pow((1+rate/100),time)
print(f"The total amount after {time} years is: {total:.2f}")
```
#### For loop:

```python
# For loop- executes a block of code a specified number of times
#          you can iterate over a range,string,sequence,etc..

for x in range(1,11,2): #start,stop,step
    print(x)

#couting backwards
for x in range(10,0,-1):
    print(x)
#or
for x in reversed(range(1,11)):
    print(x)

credit_card_number = "1234-5678-9012-3456"
for x in credit_card_number:
    print(x)

for x in range (1,21):
    if x==13:
        continue
    else:
        print(x)
```

#### Countdown timer program:

```python
#Timer program
import time
sec=int(input("Enter the time in seconds: "))
for x in range (sec,0,-1):
    sc=x%60
    min=int(x/60)%60
    hr=int(x/3600)
    time.sleep(1)
    print(f"{hr}:{min}:{sc}")
print("Time is up!") 
```

#### Nested loops:

```python
rows=int(input("Enter the number of rows: "))
columns=int(input("Enter the number of columns: "))
symbol=input("Enter the symbol to use: ")

for x in range(rows):
    for y in range(columns):
        print(symbol, end="")
    print()
```

#### Lists,Sets and tuples:

```python
# collection = single "variable" used to store multiple values

#   List  = [] ordered and changeable. Duplicates OK
#   Set   = {} unordered and immutable, but Add/Remove OK. NO duplicates
#   Tuple = () ordered and unchangeable. Duplicates OK. FASTER

fruits = {"apple", "orange", "banana", "coconut"}

# print(dir(fruits))
# print(help(fruits))
# print(len(fruits))
# print("pineapple" in fruits)

print(fruits)

# for fruit in fruits:
#     print(fruit)

# fruits[0] = "pineapple"
# fruits.append("pineapple")
# fruits.remove("apple")
# fruits.insert(0, "pineapple")
# fruits.sort()
# fruits.reverse()
# fruits.clear()
# print(fruits.index("apple"))
# print(fruits.count("pineapple"))

print(fruits)
```

```python
#   Sets

fruits = {"apple", "orange", "banana", "coconut"}

# print(dir(fruits))
# print(help(fruits))
# print(len(fruits))
# print("pineapple" in fruits)

fruits.add("pineapple")
fruits.remove("apple")
fruits.pop()
fruits.clear()
print(fruits)
```

```python
#   Tuples in Python
#   Tuples are immutable sequences, typically used to store collections of heterogeneous data. They are similar to lists, but they cannot be modified after they are created. Tuples are defined using parentheses ().

fruits = ("apple", "orange", "banana", "coconut","coconut")

# print(dir(fruits))
# print(help(fruits))
# print(len(fruits))
# print("pineapple" in fruits)

print(fruits.index("banana"))
print(fruits.count("coconut"))

print(fruits)

for fruit in fruits:
    print(fruit)
```

#### **2D Collections:**

2D List:-

```python
fruits=["apple","mango","pineapple","grape"]
veggies=["drumstick","bitterguard","beans"]
drinks=["thumbsup","sprite","maaza","fizz"]

gloceries=[fruits,veggies,drinks]

#we can also insert gloceries-[["apple","mango","pineapple","grape"],
#                                   ["drumstick","bitterguard","beans"],
#                               ["thumbsup","sprite","maaza","fizz"]]

# for items in gloceries:
#     print(items,end=" ")

for items in gloceries:
    for eatable in items:
        print(eatable)
```

2D Tuples:-

```python
num_pad=((1,2,3),(4,5,6),(7,8,9),("*",0,"#"))

for line in num_pad:
    for num in line:
        print(num,end=" ")
    print()
```

#### **Quiz game:**

```python
questions=("How may elements are there in periodic table?: ",
           "which animal lays the largest egg: ?",
           "what is the most abundent gas in the earths atmosphere?: ",
           "how many bones are there in humand body?: ",
           "which planet in the solar system is the hotest?: ")

options=(("A.116 ","B.117 ","C.118 ","D.119 "),
         ("A.Whale ","B.Crocodile ","C.Elephant ","D.Ostrich "),
         ("A.Nitrogen ","B.Oxygen ","C.Carbon dioxide ","D.Hydrogen "),
         ("A.206 ","B.207 ","C.208 ","D.209 "),
         ("A.Mercury ","B.Venus ","C.Earth ","D.Mars "))

answers=("C","D","A","A","B")
gussess=[]
score=0

question_num=0

for question in questions:
    print("----------------------------------------")
    print(question)
    for option in options[question_num]:
        print(option)
    guess=input("Enter you answer (A/B/C/D))")
    gussess.append(guess)
    if guess==answers[question_num]:
        score+=1
        print("Correct!")
    else:
        print("Incorrect!")
        print(f"{answers[question_num]} is correct answer")
    question_num+=1

print(F"Your score is {score}.")

print("|------------------|")
print("|-----results------|")
print("|------------------|")

print("Correct answers: ")
for answer in answers:
    print(answer,end=" ")
print()

print("Guessed answers: ")
for guess in gussess:
    print(guess,end=" ")    
```

#### Dictionaries:

```python
#dictonaries - a collection of key value pairs
#               ordered, changeable, no duplicates {key : value} pairs
capitals = {
    "USA": "Washington DC",
    "India": "New Delhi",
    "China": "Beijing",
    "Russia": "Moscow",
}

# print(capitals["USA"]) #accessing a value by key
# print(capitals.get("USA")) #another way to access a value by key
# print(capitals.get("Germany")) #returns "None" if key is not present
#print(capitals.get("Germany", "Not Found")) #returns "Not Found" if key is not present

if capitals.get("Germany") is None: #checking if a key is in the dictionary
    print("Germany is not in the dictionary")
else:
    print("Germany is in the dictionary")

capitals.update({"Germany": "Berlin"}) #adding a new key-value pair to the dictionary
print(capitals)

keys = capitals.keys() #returns a view object of the keys in the dictionary
print(keys)

for key in capitals.keys(): #iterating through the keys in the dictionary
    print(key)

```

#### Concession stand Program:

```python
menu={  "pizza":3.00,
        "hamburger":2.50,
        "salad":1.50,
        "soda":1.00,
        "water":0.00,
        "ice cream":2.00,
        "chicken nuggets":2.50,
        "french fries":1.50,
        "hot dog":2.00 
}

# print(menu.get("ice cream")) This gets the rate of the ice cream,if ice cream is not found it throes "None"
# print(menu.items()) This get the all elements in the list 

cart=[]

total=0

print("---------Menu----------")
for key,value in menu.items():
    print(f"{key:15} {value:.2f}")
print("------------------------")

while True:
    food=input("Enter item").lower()
    if food=="q":
        break;
    elif menu.get(food) is not None:
        cart.append(food)

print(cart)

for value in cart:
    total=total+menu.get(value)

print(f"Total cart value is {total}")
```

#### import random function:-

```python
import random

low=1
high=100

options=["rock","paper","scissors"]

cards=["2","3","4","5","6","7","8","9","10","J","Q","K","A"]

# number=random.randint(low,high)

# number=random.random() # 0.0 to 1.0
# print(number)
# choice=random.choice(options)
# print(choice)

random.shuffle(cards)
print(cards)
```

#### number guessing game:-

```python
import random

low=1
high=100
number=random.randint(low,high)
guess=0
is_guessing=True
#print(number) #This displays randomly generated number 
while is_guessing:
    print(f"Guess the number from {low} to {high}")
    entered_number=input("Enter you number")
    if entered_number.isdigit():
        entered_number=int(entered_number)
        if entered_number < low or entered_number > high:
            print(f"Enter number should be between the {low} and {high}")
    else:
        print("Invalid guess")
        print("You should not enter strings")
        
    guess+=1
    if entered_number==number:
        print(f"yah you guessed it in {guess} tries!")
        is_guessing=False
```

#### Rock Paper Scissors  game:-

```python
import random
options=("rock","paper","scissor")

running=True

while running:
    player=None
    computer=random.choice(options) #print(computer)

    while player not in options:
        player=input("Enter you choice: ")
    
    print(f"player - {player}")
    print(f"computer - {computer}")

    if player==computer:
        print("Its a tie!")
    elif player=="rock" and computer=="scissor":
        print("you win")
    elif player=="paper" and computer=="rock":
        print("you win")
    elif player=="scissor" and computer=="paper":
        print("you win")
    else :
        print("you lose")

    if not input("Do you want to play y/n: ").lower() =="y":
        break

print("Thanks for playing")
```
#### Python Dice Roller

```python
import random

dice_art = {
    1: ("┌─────┐",
        "│     │",
        "│  ●  │",
        "│     │",
        "└─────┘"),
    2: ("┌─────┐",
        "│●    │",
        "│     │",
        "│    ●│",
        "└─────┘"),
    3: ("┌─────┐",
        "│●    │",
        "│  ●  │",
        "│    ●│",
        "└─────┘"),
    4: ("┌─────┐",
        "│●   ●│",
        "│     │",
        "│●   ●│",
        "└─────┘"),
    5: ("┌─────┐",
        "│●   ●│",
        "│  ●  │",
        "│●   ●│",
        "└─────┘"),
    6: ("┌─────┐",
        "│●   ●│",
        "│●   ●│",
        "│●   ●│",
        "└─────┘")
}
dice = []
total=0
no_of_dice = int(input("Enter the number of dice: "))

for _ in range(no_of_dice):
    dice.append(random.randint(1, 6))

for die in dice:
    total+=die
    for line in dice_art[die]:
        print(line)
    print()  # blank line between dice

print(total)

for line in range(5):
    for die in dice:
        print(dice_art.get(die)[line],end=" ")
    print(" ")
```
### **Functions:-**

```python
# Function - functions are reusable code blocks
def happybirthday(name,age):
    print(f"happy birthday {name}")
    print(f"you are {age} years old")
    print(f"Happy birthday to you !")

happybirthday("nikki",20)
happybirthday("steve",20)
happybirthday("raviteja",20)
```

```python
def display_invoice(username,amount,due_date):
    print(f"hello {username}")
    print(f"your bill is of {amount:.2f} is due on {due_date}")

display_invoice("nikhil",500,"1/3/2026")
```

```python
def create_name(first,last):
    first=first.capitalize()
    last=last.capitalize()
    return first +" "+last

print(create_name("nikhil","vytla"))
```

#### Default arguments:-

```python
#default arguments- A default value for certain parameters
#                   default is used when that argument is omitted
#                   make your functions more flexible,reduces # of arguments
#                   1. positional, 2. Default 3.keyword 4. arbitrary

def net_price(list_price, discount=0,tax =0.05):
    return list_price*(1-discount) *(1+tax)

print(net_price(500))
print(net_price(500,0.1))
print(net_price(500,0.1,0))
#normally we we pass 3 parameters if we skip passing even one that throws error
#so here we have default arg,we give them while defining function ,even if we skip the default values will be fetched and used

```

```python
import time
def counter(end,start=0):
    for x in range(start,end+1):
        print(x)
        time.sleep(1)
    print("Done!")

counter(10)
```

#### Keyword arguments:-

```python
#keyword arguments = an argument preceeded by an identifier
#                   helps with readability
#                   order of arguments doesnt matter
#                   1.positional 2.default 3.keyword 4.arbitrary

def hello(greeting, title,first,last):
    print(f"{greeting} {title} {first} {last}")

hello("Hello" ,title="Mr.",last="nikhil",first="vytla")
#just we will give parameter name when we are passing the arguments ,we can alter the order,no problem with that when we are using keyword args
```

#### *args and **kwargs:-

```python
# *args =allows you to pass multiple non-key arguments
# **kwargs= allows you to pass multiple keyword-arguments
#           * unpacking operator
#           1. positional 2.default 3.keyword 4.arbitary

def add(*nums):
    total=0
    for num in nums:
        total+=num
    return total

print(add(1))

#this saves data in tuples format while **kwargs stores data in dictonary format
```

```python
def display_name(*args):
    for arg in args:
        print(arg,end=" ")
    
display_name("Dr. ", "spongebob","Harold","squarepants")
```