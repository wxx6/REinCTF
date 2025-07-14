# BlitzCTF

## PyPain

> We got hit by a ransomware, our files have now been encrypted using top grade military security, save us!

| points: 289 | solutions: 49 |
|-------|-------|
| issolved: ✓ | abstract: ✓ |

`pyinstaller` | `aes-cbc-128`

随机生成key和iv，同时输出到密文中。但是加密时没用到iv，密文长度也不对。用的是aes-cbc-128加密，随机数生成的iv长度为8并且在加密中未使用，而当`AES.new()`没接受到iv时会随机生成iv。在该函数对参数的介绍中有说，没重新赋值iv这就是这个题的脑洞之处

## C++ Pain

> Pain

| points: 394 | solutions: 35 |
|-------|-------|
| issolved: ✓ | abstract:  |

`简单vm` | `C++`

这个题也有点抽象，定长指令而且只用到两种，但是C++的函数调用很乱，表层的函数啥也没做就光搁那调用更深层的函数。能直接猜出来加解密流程

## How time flows

> Time flows like a river. Don't be fooled by things you see on the surface. There might be something dangerous below the depths

| points: 480 | solutions: 16 |
|-------|-------|
| issolved: ✓ | abstract:  |

`RC4` | `时间戳爆破`

时间戳随机数生成key，没什么难度

## Times Now

> Here's our news printing service, times now! Read latest news on Times Now! And also, I was able to extract a conversation from two of the employees of Times Now: Riya: Hey, are we still on for the trip next month? Alex: Yep, absolutely! Got everything lined up. Riya: Nice. When exactly are we leaving again? Alex: It’s a Monday, early afternoon IST. You’ll get the final itinerary soon. Riya: Perfect, I just need to let work know. Alex: I was just looking at my notes—our departure code is 1751634980 if you need to tag it for reference. 😄 Riya: Departure code? That's… oddly specific. Alex: Haha, yeah, I like using numeric tags instead of plain dates. Makes things feel more encrypted. 😎 Riya: You're such a nerd, but okay. I’ll mark it down!

| points: 500 | solutions: 2 |
|-------|-------|
| issolved: ✓ | abstract:  |

`caml` | `简单异或`

一血。如果caml编译后把所有符号删掉根本没法做。第一步就是通过函数列表找到题目对应的entry，然后才能分析。运算就是简单的异或，时间戳已经给出所以生成的异或序列是固定的，但是在获取文件内容和输出内容到文件时，数据会发生变化，幸运地猜到是乘2或除2

## IDA Pro Crack

> Your friend wanted to learn malware analysis and downloaded a cracked version of IDA Pro from the internet. At first, everything seemed fine — until Facebook sent a warning about a suspicious login.
> 
> He started getting suspicious and asked you to take a look at the file he downloaded — still sitting in his Downloads folder.
> 
> Can you find the domain where the attacker exfiltrated the data to?

| points: 500 | solutions: 4 |
|-------|-------|
| issolved: lock | abstract:  |

`malware`

附件1个多G，懒得下

## Runsomware

> I accidentally downloaded and executed an unknown program. After that, one of my important files was encrypted. Fortunately, I managed to dump the process before it stopped. Can you help me recover my file? (password: infected)

| points: 500 | solutions: 0 |
|-------|-------|
| issolved: lock | abstract:  |

`malware` | `dmp文件`

半夜上题，没来得及做。不会做，这题运行的文件一点符号都没有，只能学一点windbg的使用方式或者说命令。r register查看寄存器(不加register会显示全部)；k查看调用堆栈；u address Lnum向下反汇编num行(不加address会接着上次的地址继续，ub为向上，如ub @rip L20)；lm查看模块(这里可能会有可执行文件，然后用`.writemem`提取)。