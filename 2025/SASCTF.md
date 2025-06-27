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

`zpaqѹ����`

�����о�ZPAQ��ʽ�������˽⵽����һ���ؼ������ǽ�ѹ���߼�����Ӳ���뵽�������ļ��У�������Ϊһ�ֶ��Ƶ��ֽ���Ƕ�뵽�鵵�ļ��С�ZPAQ��ִ���ļ�����һ��JIT��������ִ������ֽ��룬��ר�����x86ƽ̨�������Ż���������Ŀ���ZPAQԴ�룬����Ȼ�����exe�����ι۲��ѹ���̣���`libzpaq::ZPAQL::run`���������ҵ��ֽ�����ã������ܿ���`INVALID PASSWORD`�����������Ե��ǿ��Ե��ԣ�����û����wp���ᵽ�Ķ�`ENTER___PASSWORD`��У�飬����Ҳû������Կ�Ķ�Ӧ��ϵ��ͨ����������Կ��run����ǰ���Ѿ�������

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

`malware` | `asar��ȡ` | `js����`

��Ŀ����`Test.exe`��һ��electronӦ�����棬����ִ��`./resources/app.asar`��������Ҫ��`asar`��ȡ����ȡ��`index.js`���ǹؼ������ˣ����Ƿ����л���������ʹ��[synchrony](https://deobfuscate.relative.im/)���н������������js��ȡ��ǰϵͳע����ض���Ȼ����sha256��ϣ��Ϊ��Կ����ʹ��aes-cbc�����ļ�

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

�е���misc�ˡ�������ֻ����һ���ļ������ǻ��صظ��˸�������Ϊ��������ĺ�˲������˸���վ�ṩ��Ŀ�������ᵽ�����ֱ���������أ����ص����ֱ���������к��ţ���Ӻ�˻�ȡ�ļ����ص�����Ȼ�����ִ�У�ִ�еĳ�����pyinstaller����ģ��������һ��pyarmor

## A mule stealer

> [IMPORTANT] This challenge involves working with malicious files. While we have done our best to ensure that these files cause no malicious impact if launched accidentally, please be careful when working with them.   
> Is this a rabbit? Or a cat? Or a crabbit..., maybe? I'm instructed not to click on weird attachments, but this one should be my background image for real! 

| points: 478 | solutions: 10 |
|-------|-------|
| issolved: lock | abstract:  |

`malware`

����һ�������ʼ�������������ӣ�������һ����ҳʵ����[Fake Captcha](https://securelist.com/lumma-fake-captcha-attacks-analysis/116274/),������д���������ͼ��Զ�̷���������HTA(HTML file supporting Windows scripting languages)�ļ���ִ�У�HTA�ļ�ִ��vba�ű��Ӷ�����powershell��powershell������png�ļ�����ʹ��LSB�㷨������ȡ��д�Ŀ�ִ���ļ����ؼ����������Ŀ�ִ���ļ���

## Sigma DSP

> Sigma Acoustic Calibrator helps protect your hearing by playing a short reference signal and dynamic audio, letting you adjust your system volume to a safe, comfortable level. 

| points: 487 | solutions: 8 |
|-------|-------|
| issolved: lock | abstract:  |

`web` | `wasm`
