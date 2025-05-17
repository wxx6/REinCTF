# TAMUCTF

[official wp](https://github.com/tamuctf/tamuctf-2025)

## What It Does

> What does it do? Does it do what it does?

| points: 100 | solutions: 126 |
|-------|-------|
| files:  | issolved: ✓ |

`nim`

## OTP

> I heard one-time pads are unbreakable, so it should be impossible to recover the flag, right?

| points: 100 | solutions: 48 |
|-------|-------|
| files:  | issolved: ✓ |

`core dump` | `gdb`

## Brainrot

> This challenge is only solvable in Ohio 😂😂.
> 
> Note: This challenge requires -k to run properly.

| points: 100 | solutions: 73 |
|-------|-------|
| files:  | issolved: ✓ |

`matrix mul`

## Xorox

> Today I will xor my flag with a key.
> Note: Only the correct flag will make the binary print Yup

| points: 100 | solutions: 65 |
|-------|-------|
| files:  | issolved: ✓ |

## Backdoored

> I set up this Spigot server to play with my friends, but it got hacked! Can you help me recover my world please?

| points: 456 | solutions: 11 |
|-------|-------|
| files:  | issolved: ✓ |

`minecraft server` | `base64` | `xxtea`

## Simple Check

> I've given you a binary that allows you to read any file on the system. So, go ahead and read the flag. If you need to debug anything, I've put a helpful call logger on the remote.
> Hint 1: It's easier than you think. No binary payload or shellcoding required, I promise.
> Hint 2: Don't waste your time reversing async Rust. Just figure out what the call logger does to log calls.

| points: 479 | solutions: 8 |
|-------|-------|
| files:  | issolved: ✓ |

`eBPF` | `0xcc断点`

eBPF会插入硬件断点即0xff从而附加到进程，所以可以修改变量的值为0xcc，尤其是能将bool类型的值从False变为True

## FastFlagChecker

> My flagchecker is so fast, I give every bit its own thread!

| points: 493 | solutions: 5 |
|-------|-------|
| files:  | issolved: ✓ |

`多线程` | `Semaphore信号量`


