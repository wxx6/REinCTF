# NoHackNoCTF

## flag checker

> You are doing a mission and you need to find out the secret

| points: 100 | solutions: 91 |
|-------|-------|
| issolved: ✓ | abstract:  |

`float浮点运算`

动调取值即可

## b@by_r3v3rs3

> my friend send me this file I don't know what he want to say can you help me solve this problem?

| points: 432 | solutions: 31 |
|-------|-------|
| issolved: lock | abstract:  |

`wasm` | `aes-cbc`

wasm还是很难看懂。想办法找到更好的反汇编甚至反编译工具或方法，wabt或者ida9的反汇编根本没法看，因为数据以及函数之间的索引完全没法看

## Yep Another Snake Game

> The only game I made in CTFs is Snake Game!

| points: 449 | solutions: 27 |
|-------|-------|
| issolved: ✓ | abstract:  |

`godot`

网页版的godot游戏。有点sb，做题没注意到pck文件，原来可以直接从pck中提取

## Encrypted(?

> This suspicious executable encrypted my files.I don't know how to recover. Can you help me recover them? They included some of my favorite memes and an image containing the flag you need for this challenge. I spent like half an hour hand-drawing it, and now it's gone 😭😭😭

| points: 490 | solutions: 12 |
|-------|-------|
| issolved: ✓ | abstract:  |

`mmap` | `signal` | `vm`

vm题型，使用ud2指令触发信号handler函数，但是代码不完全在vm里，一直在程序代码和vm代码之间切换。需要注意判断语句

## ICED-SHELL

> Dear M,
I just heard that we got hacked, but actually...
I sniffed all our networks so that those hackers messages might be revealed!
Best Regards, James Bond

| points: 495 | solutions: 9 |
|-------|-------|
| issolved: lock | abstract:  |

`nodeJS` | `pkg打包`

不会解包。。