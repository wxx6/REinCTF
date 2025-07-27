# NepCTF

## Realme

> Seeing is not necessarily believing, can you recognize the real me?

| points: 200 | solutions: 93 |
|-------|-------|
| issolved: ✓ | abstract:  |

`反调试` | `smc` | `魔改RC4`

通过ida标红的代码段可以定位到反调试函数以及实际的加密函数

## Crackme

> inkey最近在学校上学时，老师安排了一个任务，而有一款软件可以很快地梭哈完成，但是支付需要高额的费用。 于是同学们都来拜托inkey，希望能他能破解出软件的注册码，并发给他们每个人。 （靶机网页登录上去后，提交每个用户名对应的注册码，全部正确即可得到flag）

| points: 512 | solutions: 20 |
|-------|-------|
| issolved:  | abstract:  |

`PyQt`

libcrypto文件应该是出题人自己写的，sign函数像是md5，但是应该有魔改。。后续aes部分都懒得看了

## QRS

> 选手最终得到的是NepCTF{}之间的字符串，提交需加上NepCTF{}

| points: 555 | solutions: 17 |
|-------|-------|
| issolved:  | abstract:  |

## SpeedMino-Warlock

> Into realms beyond heaven and earth.
Find the true Secret FLAG

| points: 833 | solutions: 5 |
|-------|-------|
| issolved:  | abstract:  |

## FlutterPro

> Not Easy, Not Baby, it is PRO!

| points: 1000 | solutions: 1 |
|-------|-------|
| issolved:  | abstract:  |

## XSafe

> 一行代码也能逆向吗？xiaoji回答：能的兄弟，能的。
> 
> 解题要求：
> 
> 在非调试的环境中，加载驱动，驱动返回0表示加载成功，此时运行exe文件可以校验输入的flag。
驱动只进行了测试签名，请自行解决加载问题（驱动不会对操作系统进行任何破坏性操作，请放心加载）。
必须使用64位Win10-Win11 22H2系统解题。
flag格式：NepCTF2025{uuid}

| points: 1000 | solutions: 0 |
|-------|-------|
| issolved:  | abstract:  |

## reboot

> 勇敢的MK.99获取到了boot文件，让帮MK.99解锁权限吧。

| points: 1000 | solutions: 0 |
|-------|-------|
| issolved:  | abstract:  |