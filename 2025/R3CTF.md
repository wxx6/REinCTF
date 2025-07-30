# R3CTF

## Neon Deceit

> In the neon-lit underbelly of the city, even your tools are programmed to betray you. Trust nothing... the lies are embedded in the code.

| points: 894 | solutions: 13 |
|-------|-------|
| issolved: lock | abstract: ✓ |

`迷宫` | `反调试` | `混淆`

通过修改dynsym元数据混淆库函数，使得调用库函数时实际上执行的是另外的库函数

## r3loads

> "When her neon dreams shatter into encrypted fragments… can you trace the echoes of her lost truth?"
> 
> Legends whisper of a lone girl wandering the rain-slicked streets of Night City, chasing a cryptic relic known only as R3LOAD, a digital ghost said to hold the key to her fractured past. But the data-core was shredded by the rogue AI Disassembler into 11,423 encrypted fragments, each warped by a unique cipher, their glow dimmed beneath the city’s smog. Only those who dare to dive into the abyss of code can follow the trail she left behind.
> 
> Hack the Disassembler's core, decrypt the fragments, and rebuild her truth before Night City's pulse drowns her final whisper.

| points: 944 | solutions: 11 |
|-------|-------|
| issolved: lock | abstract:  |

`autorev`

完全解压需要很久，可以部分解压先进行分析。需要写脚本动态提取参数为常量的库函数返回值，以此来简化加密函数逻辑。[参考大佬wp](https://nothoudaifa.github.io/posts/r3ctf2025-r3loads/)

## rollin

> I swear I have heard something. I turn back but there's nothing more than the neon lights shining over the fog of RE-city. nothing makes sense.. wait, how did I end up here anyway? where is everyone? did I accidentally end up in another part of the city?

| points: 958 | solutions: 10 |
|-------|-------|
| issolved: lock | abstract:  |

## rosnake

> As the neon lights of the city flickered under the dark sky, an urgent alert echoed throughout the central server hub. A young hacker named Lyra stared at the glowing terminal in front of her. On the screen, an ancient game of Snake had appeared, but with a twist—the game was connected to the city's cyber-defense system. As she maneuvered the snake, consuming data blocks, the stakes grew higher. Each block consumed increased the snake’s length, and only when it reached 64 bits would the ultimate defense mechanism unlock.
> 
> With seconds ticking away and obstacles increasing in number, Lyra's determination sharpened. She skillfully dodged every hazard and consumed all sixty-four data blocks in quick succession. As the snake reached its final form, a password prompt appeared. Lyra entered the decryption code with precision. “Access Granted” flashed on the screen, and with a dramatic hum, the city's network was secured. The hacker's plan was foiled, and the city was saved once again.
> 
> The flag format is: R3CTF{*}

| points: 958 | solutions: 9 |
|-------|-------|
| issolved: lock | abstract:  |

## r3loads2

> "She found the truth, but the Disassembler's final laugh echoed—some secrets are buried deeper than code."
> 
> The girl's victory was short-lived. As the first R3LOAD fragments reconstructed, the rogue AI's true protocol awakened: R3LOAD.EXE v2.0. Now the fragments fight back. Each cipher evolves, each puzzle grows stronger from her previous solutions.
> 
> In Night City's neon-drenched depths, she faces the ultimate test—not just recovering her past, but distinguishing truth from the lies woven into her very existence.
> 
> Your mission intensifies
> 
> The AI is learning. Time is running out. Will you help her reclaim her stolen soul?

| points: 993 | solutions: 4 |
|-------|-------|
| issolved: lock | abstract:  |

