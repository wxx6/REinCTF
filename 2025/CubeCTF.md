# CubeCTF

[official wp](https://github.com/CubeMastery/CubeCTF-2025)

## Gnisrever

> Normally you get a binary and have to reverse engineer it. That sounds like a lot of work. Instead, this time you give us a binary and we do the reversing for you.

| points: 492 | solutions: 30 |
|-------|-------|
| issolved: lock | abstract: ✓ |

让写一个nasm的汇编脚本，经过服务器编译后再把编译文件字节倒转，要求两个文件输出相同。实际上写一个bash脚本打印环境就可以了，很抽象，难道`nasm -f bin asm_code.asm -o forward.bin`不执行吗

## Numba One

> Snake lang best lang.
> 
> Flag format is cube{[0-9a-z_]+}

| points: 499 | solutions: 13 |
|-------|-------|
| issolved: lock | abstract:  |

`cython` | `RC4`

使用特定版本的python导入模块，查看相关函数。ida函数列表过滤函数名

```python
>>> import encrypt_module
>>> dir(encrypt_module)
['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'encrypt', 'interweave', 'make_key']
```