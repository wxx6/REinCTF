# NahamConCTF

## FlagsFlagsFlags

> Did you see the strings? One of those is right, I can just feel it.

| points: 147 | solutions: 267 |
|-------|-------|
| issolved: ✓ | abstract:  |

`upx` | `go`

## What's a base amongst friends?

> What's a base amongst friends though, really?

| points: 310 | solutions: 196 |
|-------|-------|
| issolved: ✓ | abstract:  |

`rust` | `base32`

## Deflation Gangster

> Like American Gangster, but for other stuff.

| points: 372 | solutions: 161 |
|-------|-------|
| issolved: ✓ | abstract: ✓ |

`misc`

这题和re没什么关系。题目解压会得到一个快捷方式，里面偷偷启动powershell执行脚本，脚本内容是找一个与快捷方式同名的zip压缩包，然后匹配压缩包二进制序列`UUUU`向后读53个字符。但是实际上这个压缩包并不存在，存在的是题目给的压缩包，里面有一串base64。。

## No! Not again!

> Yeah, so... It's a crackme... It's in your FAVORITE language to Reverse Engineer!

| points: 424 | solutions: 125 |
|-------|-------|
| issolved: ✓ | abstract:  |

`简单运算`

## It's Locked

> This bin looks locked as a crypt to me, but I'm sure you can work some magic here.
All I know is that this came from a machine with a cryptic ID of just 'hello'.

| points: 458 | solutions: 93 |
|-------|-------|
| issolved: ✓ | abstract:  |

`bash`

执行bash脚本可以加上-x标志来打印脚本的执行过程。比较复杂，对bash不是很熟，但是能够结合gpt做

```bash
bash -x ./flag.sh
```

## It's one syscall, Michael

> What could it cost, $10?

| points: 499 | solutions: 16 |
|-------|-------|
| issolved: lock | abstract:  |


