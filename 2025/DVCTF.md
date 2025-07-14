# DVCTF

## Davinci Click

> My friend created a cookie clicker style game with a twist, at 10 million clicks something happens.

| points: 337 | solutions: 65 |
|-------|-------|
| issolved: ✓ | abstract:  |

`unity`

## VinciVault

> Une application oubliée a refait surface. Elle renfermerait un secret... Saurez-vous le percer ?

| points: 454 | solutions: 35 |
|-------|-------|
| issolved: ✓ | abstract:  |

`IOS`

## Synthesize_me

> Les voleurs ont obfusqué un secret dans le binaire. A vous de le retrouver.

| points: 500 | solutions: 5 |
|-------|-------|
| issolved: ✓ | abstract:  |

`ollvm`

动调应该能做，很耗时间罢了。赛后做了一整天。有混淆(指令替换、虚假控制流、控制流平坦化好像都有)，而且还有花指令，但是不影响动调无非是多按几下快捷键罢了。把所有运算提取出来，重建代码，并且把所有运算简化，就能发现非常明显的特征能感觉出来。实际上极简化，就是把输入作为大整数做a*a+a运算。。就一个一元二次方程，所以用一下求根公式就出来了

## Infected Brick

> Un des gardiens du musée a téléchargé une application suspecte peu de temps avant le vol. Nous suspectons qu’il s’agit d’une application malveillante utilisée par les voleurs pour étudier la sécurité du musée. Pouvez-vous étudier cette application et identifier les données dérobées ?

| points: 490 | solutions: 17 |
|-------|-------|
| issolved: ✓ | abstract:  |

`安卓`

最低API需要29，没法运行。jadx反编译不完全，还得用jeb。MainActivity没什么重要的，同包名下的`Tetris_lib`类有native层函数，查引用发现解密了`acca3789580d7df462935a3c`文件并且作为dex文件进行加载。native层函数静态注册，使用AES-CBC解密，key直接给出，iv是加密文件的前十六个字节。解密后发现是RC4和异或