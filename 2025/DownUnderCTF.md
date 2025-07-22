# DownUnderCTF

2025-07-19

## rocky

> An underdog boxer gets a once-in-a-lifetime shot at the world heavyweight title and proves his worth through sheer determination.

| points: 100 | solutions: 522 |
|-------|-------|
| issolved: ✓ | abstract:  |

`md5` | `aes-cbc-128`

## skippy

> Skippy seems to be in a bit of trouble skipping over some sandwiched functions. Help skippy get across with a hop, skip and a jump!

| points: 100 | solutions: 313 |
|-------|-------|
| issolved: ✓ | abstract:  |


`aes-cbc-128`

## SwiftPasswordManager: ClickMe

> This password manager app has a button labeled "Flag" but it doesn't seem to be clickable...

| points: 165 | solutions: 115 |
|-------|-------|
| issolved: ✓ | abstract:  |

`swift应用`

主要是搜索按钮文本以查找对应的初始化函数或者对应的按钮事件，得用搜索字节序列的方法找，字符串列表里没有。这个题搜`Flag`对应的字节序列能找到View.disabled函数，将参数一从1改为0即可

## godot

> Vladimir and Estragon converse on various topics while they wait for a man named Godot. While they wait, Pozzo is on his way to the market to sell his slave, Lucky.

| points: 180 | solutions: 96 |
|-------|-------|
| issolved: ✓ | abstract:  |

`godot` | `pck加密`

根据godot源码[FileAccessPack](https://github.com/godotengine/godot/blob/71a9948157dc2d5cc71fcb456c9d96656678757d/core/io/file_access_pack.cpp#L472)类的构造函数中的字符串在exe中定位到该构造函数，然后对照源码查找key的赋值

## bilingual

> Two languages are better than one!

| points: 47 | solutions: 241 |
|-------|-------|
| issolved: ✓ | abstract:  |

`cdll` | `rc4`

python加载dll，C与Python的交互

## SwiftPasswordManager: LoadMe

> I used the app to save a password before realising that the Load button doesn't do anything... Can you help me load my passwords? The master password is DUCTF2025!.
> 
> NOTE: This challenge uses the same handout app as "SwiftPasswordManager: ClickMe"

| points: 253 | solutions: 41 |
|-------|-------|
| issolved: ✓ | abstract:  |

`aes-gcm`

这个题搜`SPM1`对应的字节序列就能定位到处理函数

## SwiftPasswordManager: CrackMe

> If you choose a good password, you might get a flag!
> 
> NOTE: This challenge uses the same handout app as "SwiftPasswordManager: ClickMe"

| points: 308 | solutions: 21 |
|-------|-------|
| issolved: ✓ | abstract:  |

主要就在于怎么定位到关键函数，剩下的都是小case。re拿到一个题，最怕的就是没地方下手在无关紧要的地方死转圈，其次就是看不懂算法本质只能说数学不会就是不会。这个题搜`Generate`对应的字节序列能找到password编辑框的Binding.onChange函数