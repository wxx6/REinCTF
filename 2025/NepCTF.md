# NepCTF

## Realme

> Seeing is not necessarily believing, can you recognize the real me?

| points:  | solutions:  |
|-------|-------|
| issolved: ✓ | abstract:  |

`反调试` | `smc` | `魔改RC4`

通过ida标红的代码段可以定位到反调试函数以及实际的加密函数

## Crackme

> inkey最近在学校上学时，老师安排了一个任务，而有一款软件可以很快地梭哈完成，但是支付需要高额的费用。 于是同学们都来拜托inkey，希望能他能破解出软件的注册码，并发给他们每个人。 （靶机网页登录上去后，提交每个用户名对应的注册码，全部正确即可得到flag）

| points:  | solutions:  |
|-------|-------|
| issolved:  | abstract:  |


libcrypto文件应该是出题人自己写的，sign函数像是md5，但是应该有魔改。。后续aes部分都懒得看了

## reboot

> 勇敢的MK.99获取到了boot文件，让帮MK.99解锁权限吧。

| points:  | solutions:  |
|-------|-------|
| issolved:  | abstract:  |