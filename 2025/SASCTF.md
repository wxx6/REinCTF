# SASCTF

[official wp](https://github.com/Team-Drovosec/sasctf-quals-2025/tree/main/tasks)

## Washing Machine

> Your flag has been spoiled. Only the Holy Washing Machine can save it, but be careful, She's got a twist. 

| points: 500 | solutions: 1 |
|-------|-------|
| issolved: lock | abstract:  |

`web` | 

## Decompression

> We compressed your flag so you can use the fanciest decompressor to get it.  

| points: 487 | solutions: 8 |
|-------|-------|
| issolved: lock | abstract:  |

`zpaq压缩包`

深入研究ZPAQ格式，我们了解到它的一个关键特性是解压缩逻辑不是硬编码到二进制文件中，而是作为一种定制的字节码嵌入到归档文件中。ZPAQ可执行文件包含一个JIT编译器来执行这个字节码，它专门针对x86平台进行了优化。创建项目存放ZPAQ源码，编译然后调试exe，传参观察解压过程，在`libzpaq::ZPAQL::run`函数中能找到字节码调用，里面能看到`INVALID PASSWORD`的由来。调试倒是可以调试，但是没发现wp中提到的对`ENTER___PASSWORD`的校验，另外也没发现密钥的对应关系，通过参数传密钥在run函数前就已经报错了

## it Sova

> I wonder who should pay for the gas on the first date. 

| points: 487 | solutions: 8 |
|-------|-------|
| issolved: lock | abstract:  |

`web3` | 

## Best Team Forever

> [IMPORTANT] This challenge involves working with malicious files. While we have done our best to ensure that these files cause no malicious impact if launched accidentally, please be careful when working with them.   
> Hi! This is Bob from incident response.  
> Reaching to you regarding that ransomware attack we've had on our side-hosted server running "Windows Server 2019 Standard (17763.3650)". I was really surprised to find out MS Teams on the application list. Like, this a server, why would you need a corporate chat there?  
> That looks kinda SUS, aren't you thinking so? That being said, attaching some related artifacts. Check asap.  
> Best regards, 
> Bob Guzini, 
> Neck of IR Department. 

| points: 490 | solutions: 7 |
|-------|-------|
| issolved: lock | abstract:  |

`malware` | `asar提取` | `js混淆`

题目给的`Test.exe`是一个electron应用引擎，用来执行`./resources/app.asar`，所以需要用`asar`提取。提取完`index.js`就是关键代码了，但是发现有混淆，可以使用[synchrony](https://deobfuscate.relative.im/)进行解混淆或美化。js获取当前系统注册表特定项然后用sha256哈希作为密钥，再使用aes-cbc加密文件

```bash
npx @electron/asar extract ./resources/app.asar [destfolder]
```

## Music Speed Changer

> [IMPORTANT] This challenge involves working with malicious files. While we have done our best to ensure that these files cause no malicious impact if launched accidentally, please be careful when working with them.   
> I miss those times when discord bots had an ability to play music... With a single button press you can change speed, pitch, bass... I like some tracks to bee speedy, some to be slow, some to bang from the back.  
> I was seeking for a solution for so long, and luckily found one! Or so I thought... Yesterday my friend from a local secret service called me and said I should change my passwords. How could he know? He refused to answer :( 

| points: 498 | solutions: 4 |
|-------|-------|
| issolved: lock | abstract:  |

`malware` | `misc`

有点像misc了。出题人只给了一个文件，但是还特地搞了个域名作为恶意软件的后端并且做了个网站提供题目描述中提到的音乐变速软件下载，下载的音乐变速软件中有后门，会从后端获取文件下载到本地然后解密执行，执行的程序是pyinstaller打包的，解包后还有一层pyarmor

## A mule stealer

> [IMPORTANT] This challenge involves working with malicious files. While we have done our best to ensure that these files cause no malicious impact if launched accidentally, please be careful when working with them.   
> Is this a rabbit? Or a cat? Or a crabbit..., maybe? I'm instructed not to click on weird attachments, but this one should be my background image for real! 

| points: 478 | solutions: 10 |
|-------|-------|
| issolved: lock | abstract:  |

`malware`

给了一个钓鱼邮件，引导点击链接，链接是一个网页实现了[Fake Captcha](https://securelist.com/lumma-fake-captcha-attacks-analysis/116274/),把命令写入剪贴板试图从远程服务器下载HTA(HTML file supporting Windows scripting languages)文件并执行，HTA文件执行vba脚本从而调用powershell，powershell会下载png文件并且使用LSB算法从中提取隐写的可执行文件。关键代码在最后的可执行文件中

## Sigma DSP

> Sigma Acoustic Calibrator helps protect your hearing by playing a short reference signal and dynamic audio, letting you adjust your system volume to a safe, comfortable level. 

| points: 487 | solutions: 8 |
|-------|-------|
| issolved: lock | abstract:  |

`web` | `wasm`
