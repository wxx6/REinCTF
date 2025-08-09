# L3akCTF

2025-07-12

[official wp](https://github.com/L3AK-TEAM/L3akCTF-2025-public/tree/main/rev)

## pacman

> I am more than just a man, I am PACMAN!

| points: 50 | solutions: 148 |
|-------|-------|
| issolved: ✓ | abstract:  |


## babyRev

> They always give you strings challenges, we are not the same, we do better.

| points: 50 | solutions: 665 |
|-------|-------|
| issolved: ✓ | abstract:  |

## Just Bun It

> The Buniverse is in trouble, and only the cleverest bunnies can crack the code! The secret flag is hidden, and you'll need to nibble your way through some tricky numbers to find it. Don't let this challenge carrot away from you—put on your thinking ears and get ready to bun-leash your skills!
> 
> Contestants are provided with a mysterious binary named runme and a file called input.txt containing pairs of numbers. This binary takes in two numbers as command-line arguments. For example: ./runme 4843 0.362 This will print a single character (e.g., l).
> 
> To find the whole flag, feed each pair of numbers from input.txt to the binary (one pair at a time) and collect all the characters!
> 
> Can you out-hop the rest and claim the flag? Good luck, and may your paws be swift and your guesses un-fur-gettable!
> 
> Note: The flag starts with l3ak instead of L3AK! l3ak{...}

| points: 50 | solutions: 112 |
|-------|-------|
| issolved: ✓ | abstract:  |

最后就差一个字符，差在浮点数的处理上，还是不够细

## Math Is Key

> I think reverse engineering is too hard of a category. How about we do some math problems instead? To speed up my checker, I made sure to use -O3 -flto for maximum performance, enjoy!

| points: 460 | solutions: 31 |
|-------|-------|
| issolved: lock | abstract:  |

`math`

前三层check可以通过输入输出的关系推测运算，第五层是直接比较。第四层分析不出来，有点对脑洞

```python
from sympy import symbols, interpolate
from sympy import simplify

data = [(123, 0x1FCA527), (789, 0x1FCA7C1), (545, 0x1FCA6CD)]
x = symbols('x')
poly = interpolate(data, x)
print("Simplified:", simplify(poly))

```

## Alpha

> Asked my sister her opinion about CS majors: "Akward and Smelly". Typical ME cope.

| points: 460 | solutions: 31 |
|-------|-------|
| issolved: ✓ | abstract:  |

`z3`

又是差一点，就错了一个运算顺序

## Useless VM

> JSFuck's obfuscation was way too weak, so I layered my own obfuscation on top of it! More obfuscation means more security, right?

| points: 497 | solutions: 10 |
|-------|-------|
| issolved: lock | abstract:  |

`js` | `混淆`

题解的思路是hook

## Flagdle

> Your group is on a 10 day streak! 🔥

| points: 499 | solutions: 7 |
|-------|-------|
| issolved: lock | abstract:  |

`go`

程序很复杂

## Face ID

> Facial recognition is really hard, but I managed to create facial recognition without using any depth or color! Sadly my user database got leaked, but I am pretty sure this is secure enough to not be broken into. Please put the text "EOF" on the last line of your file when you are submitting to the server.

| points: 500 | solutions: 5 |
|-------|-------|
| issolved: lock | abstract:  |

## I Did a Thing

> I like obfuscation :D
> 
> It is recommended to play rev/Useless VM as a prelude to this challenge.

| points: 500 | solutions: 3 |
|-------|-------|
| issolved: lock | abstract:  |

## Quantam Exfil

> Our security team intercepted reports of strange data being moved across the network. After a quick sweep, we discovered an odd program and an image file left behind on one of our systems. Something doesn’t add up. Can you help us figure out what happened?

| points: 500 | solutions: 0 |
|-------|-------|
| issolved: lock | abstract:  |
