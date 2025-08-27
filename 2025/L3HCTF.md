# L3HCTF

2025-07-12

[official wp](https://hust-l3hsec.feishu.cn/wiki/WjlUwIAahiXhlykwIe7c5V57nPb)

## TemporalParadox

> One day I made a request, but I forgot what it was. Can you help me find it?

| points: 350 | solutions: 38 |
|-------|-------|
| issolved: ✓ | abstract:  |

`C++` | `md5`

函数名不正常是因为c++编译器对函数名进行的编码规则(Name Mangling)，解决方法(7.7版本ida)是`Options -> Demangled Names -> 勾选 Assume GCC v3.x names`。可以正常分析生成函数，也可以爆破

## ez_android

| points: 363 | solutions: 36 |
|-------|-------|
| issolved: ✓ | abstract:  |

`tauri框架`

照着[tauri静态资源提取方法](https://blog.yllhwa.com/2023/05/09/Tauri%20%E6%A1%86%E6%9E%B6%E7%9A%84%E9%9D%99%E6%80%81%E8%B5%84%E6%BA%90%E6%8F%90%E5%8F%96%E6%96%B9%E6%B3%95%E6%8E%A2%E7%A9%B6/)提取出加密的js,然后使用脚本解密。关键代码在js最底部，js主要是前端控件，处理逻辑还是在so里面

```python
import brotli

content = open("test.bin", "rb").read()
decompressed = brotli.decompress(content)
open("test1.js", "wb").write(decompressed)
```

## 终焉之门

> 输入正确的密钥，证明你是命运选中的解码者
Enter the correct password to prove that you are the chosen decoder of fate.

| points: 465 | solutions: 24 |
|-------|-------|
| issolved: ✓ | abstract:  |

`vm` | `raylib` | `着色器(shader)`

重点是提取出vm部分

## easyvm

> 朴实无华的虚拟机

| points: 500 | solutions: 21 |
|-------|-------|
| issolved: ✓ | abstract:  |

`vm` | `自动化调试` | `xtea`

运算是裸露在外的，可以用idc脚本自动化调试，具体就是使用如下脚本和断点的配合(类似插桩)，即在每一个运算符处以及vm运行完处下断点，运行脚本即可得到所有的运算，分析可知是魔改xtea

```C
auto i,op;
auto events_code;
auto f=fopen("test.txt","w");
for(i=0;i<10000;i=i+1){
    events_code=wait_for_next_event(WFNE_CONT|WFNE_SUSP,20);
    if(events_code==BREAKPOINT){
        if(rip==0x00007FF7B35F1ACD){
            break;
        }
        auto mnem=GetMnem(rip);
        if(mnem=="shr"){
            fprintf(f,"0x%08X >> %d = 0x%08X\n",edx,cl,(edx>>cl)&0xffffffff);
        }else if(mnem=="xor"){
            op=Dword(rbp+0x4c);
            fprintf(f,"0x%08X ^ 0x%08X = 0x%08X\n",eax,op,(eax^op)&0xffffffff);
        }else if(mnem=="add"){
            fprintf(f,"0x%08X + 0x%08X = 0x%08X\n",eax,edx,(eax+edx)&0xffffffff);
        }else if(mnem=="sub"){
            op=Dword(rbp+0x1c);
            fprintf(f,"0x%08X - 0x%08X = 0x%08X\n",eax,op,(eax-op)&0xffffffff);
        }else if(mnem=="shl"){
            fprintf(f,"0x%08X << %d = 0x%08X\n",edx,cl,(edx<<cl)&0xffffffff);
        }
    }
}
fclose(f);
Message("\nsuccess\n");
```

## obfuscate

> 平平无奇的混淆
a fairly standard obfuscation

| points: 555 | solutions: 17 |
|-------|-------|
| issolved: lock | abstract:  |

`RC5魔改` | `混淆`

RC5有两个常量`0xB7E15163`和`0x9E3779B9`，轮数通常为12轮。这个题用了指令替换和虚假控制流来进行混淆，再加上一点反调试

## snake

> I’ve already written the flag—you can just go find it.

| points: 666 | solutions: 11 |
|-------|-------|
| issolved: lock | abstract:  |

`go`

go程序而且加了混淆，go常用混淆器[garble](https://github.com/burrowers/garble)，[gostringungarbler](https://github.com/mandiant/gostringungarbler)可以dump被混淆后的字符串

## AWayOut2

> find a way out!

| points: 869 | solutions: 4 |
|-------|-------|
| issolved: lock | abstract: ✓ |

`黑盒maze`