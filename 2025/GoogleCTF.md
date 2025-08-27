# GoogleCTF

## multiarch-1

> Stacks are fun, registers are easy, but why do one when you can do both? Welcome to the multiarch.

| points: 136 | solutions: 90 |
|-------|-------|
| issolved: ✓ | abstract:  |

`vm`

程序实现定长指令和变长指令两种，校验一共有三层，做法就是硬调。shift+F1打开Local Types窗口Insert插入结构体，如果结构体中间有多出来的字节可以通过右键->Shrink struct type。

## cgb

> A game I found in a developer's drawer, it looks like an unfinished game about a character jumping rocks?

| points: 288 | solutions: 22 |
|-------|-------|
| issolved: lock | abstract:  |

`GameBoyColor`

Game Boy Color是Game Boy加强版，可以用[mame](https://www.mamedev.org/)运行，mame有文档。`-d(-debug)`可以进入调试状态

## Asteroids Redux

> To win the game you will have to be as good as our best player (who is frankly not that good...)

| points: 298 | solutions: 20 |
|-------|-------|
| issolved: lock | abstract:  |

`raylib`

用图形库写出来的游戏。操作分为加减速和转弯以及射击(不说谁知道。。)。逻辑藏得不深，但是分数相关不是很清晰。解密逻辑是分数相关先sha256哈希，然后哈希值分两组分别对两组密文进行aes-ecb-128解密，分数相关最大为7字节。本质是分析程序缩减爆破范围

## chess

> Stuck between a rook and a hard place...

| points: 308 | solutions: 18 |
|-------|-------|
| issolved: lock | abstract:  |


## circo

> The best engineers don't wait. They iterate.
> 
> Our Circo-SDK and cloud simulator give you an unfair advantage, allowing you to test more ideas, find flaws faster, and perfect your designs while the competition is still waiting for their software to load.
> 
> Activate your unfair advantage. Start building TODAY.
> 
> Note: flag.txt and config.circo are different on the server.

| points: 420 | solutions: 5 |
|-------|-------|
| issolved: lock | abstract:  |


## fluffy

> I don’t trust anyone anymore... I have written my own App to protect my secrets. I also used my own encryption algorithm, because I believe security by obscurity is the best. But, I didn’t have time to implement the decryption functionality yet. My friend from Switzerland told me to not bother myself with it as he was able to recover my secrets in 5 minutes... How is this even possible?

| points: 347 | solutions: 12 |
|-------|-------|
| issolved: lock | abstract:  |

`flutter`

blutter的脚本可以给以后写frida脚本提供参考，frida启动命令行也要记一下。这个题得用ida调试so，光静态分析和hook看不出来，真要做出来还得想办法爆破

```bash
frida -U -f com.example.app -l blutter_frida.js
```

```js
var libapp = null;
function onLibappLoaded() {
    Interceptor.attach(libapp.add(0x2d3cd0), {
        onEnter: function () {
            init(this.context);
			console.log(`CustomEncrypt::encrypt Enter with: `)
			for (let i=0;i<2;i++)
			{
				let objPtr = getArg(this.context, i);
				const [tptr, cls, values] = getTaggedObjectValue(objPtr);
				console.log(`${cls.name}@${tptr.toString().slice(2)} =`, JSON.stringify(values, null, 2));
			}
        },
		onLeave: function(retVal) {
			console.log(`CustomEncrypt::encrypt Return: `)
			const [tptr, cls, values] = getTaggedObjectValue(retVal);
			console.log(`${cls.name}@${tptr.toString().slice(2)} =`, JSON.stringify(values, null, 2));
		}
    });
}
function tryLoadLibapp() {
    try {
        libapp = Module.findBaseAddress('libapp.so');
    } catch (e) {
        if (e instanceof TypeError && e.message === "not a function") {
            libapp = Process.findModuleByName('libapp.so');
            if (libapp != null) {
                libapp = libapp.base;
            }
        } else {
            throw e;
        }
    }
    if (libapp === null)
        setTimeout(tryLoadLibapp, 500);    
    else
        onLibappLoaded();
}
tryLoadLibapp();
```

## puzzlepuzzle

> puzzlepuzzlepuzzlepuzzlepuzzlepuzzlepuzzlepuzzle

| points: 406 | solutions: 6 |
|-------|-------|
| issolved: lock | abstract:  |

