# BYUCTF

[official wp](https://github.com/BYU-CSA/BYUCTF-2025/tree/main/rev/)

## u

> u

| points: 50 | solutions: 460 |
|-------|-------|
| files:  | issolved: ✓ |

`变量名混淆`

## LLIR

> Checker? I hardly know her!

| points: 50 | solutions: 290 |
|-------|-------|
| files:  | issolved: ✓ |

`llvm字节码` | `clang`

## Baby Android 2

> If you've never reverse engineered an Android application, now is the time!! Get to it, already!! Learn more about how they work!!

| points: 61 | solutions: 248 |
|-------|-------|
| files:  | issolved: ✓ |

`安卓native`

## Baby Android 1

> If you've never reverse engineered an Android application, now is the time!! Get to it, already!! Learn how they work!!

| points: 241 | solutions: 191 |
|-------|-------|
| files:  | issolved: ✓ |

`安卓layout`

## Bank Vault

> This bank is totally secure. No way you can break your way into the vault or recover the password. We have a special key system that is unbreakable.

| points: 375 | solutions: 133 |
|-------|-------|
| files:  | issolved: ✓ |

`C++ vector`

## moooo

> Moo, mooo mooo mooo. Mooo mooo moooo moo moo moooooooooo moo moooo
> 
> (When you have the flag, the program will run printing "gotem")

| points: 481 | solutions: 53 |
|-------|-------|
| files:  | issolved: ✓ |

`abstract` | `COW语言(brainfuck变体)`

[COW](https://esolangs.org/wiki/COW)语言，很抽象，官方wp里给了解释脚本`moo.py`或者在线解释器[cow-interpreter](https://frank-buss.de/cow.html)。可以在开头的死循环处打印状态，从而观察数据变化。输入长度为39，前33个字符在经过`MOo`指令减法之后应该为2，最后6个字符在经过`MOo`减法或者`MoO`加法后等于`gotem`