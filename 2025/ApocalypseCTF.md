# ApocalypseCTF

[official wp](https://github.com/hackthebox/cyber-apocalypse-2025/tree/main/reversing/)

## SealedRune

> Elowen has reached the Ruins of Eldrath, where she finds a sealed rune stone glowing with ancient power. The rune is inscribed with a secret incantation that must be spoken to unlock the next step in her journey to find The Dragon’s Heart.

| points:  | solutions:  |
|-------|-------|
| files:  | issolved: ✓ |

## EncryptedScroll

> Elowen Moonsong, an Elven mage of great wisdom, has discovered an ancient scroll rumored to contain the location of The Dragon’s Heart. However, the scroll is enchanted with an old magical cipher, preventing Elowen from reading it.

| points:  | solutions:  |
|-------|-------|
| files:  | issolved: ✓ |

## EndlessCycle

> The elves have whispered to Elowen that the key to the Dragon's Heart is never directly visible; instead, there are clues in all the sounds and movements hidden in the world

| points:  | solutions:  |
|-------|-------|
| files:  | issolved: ✓ |

`random`

## Impossimaze

> Elowen has been cursed to roam forever in an inescapable maze. You need to break her curse and set her free.

| points:  | solutions:  |
|-------|-------|
| files:  | issolved: ✓ |

`lib curses`

## Singlestep

> Malakar has locked away a sacred artifact away in his dungeon. He has enchanted the locking mechanism to be self-protecting. Can you embark on a mission to free the artifact back to the people's hands?

| points:  | solutions:  |
|-------|-------|
| files:  | issolved: ✓ |

`smc` | `matrix`

## Gateway

> Malakar placed a spell on you that transported you to the Nether world. The only way to escape is to remember the enchantments of your forefathers, and unleash your ability to blast through Aether gateways...

| points:  | solutions:  |
|-------|-------|
| files:  | issolved: ✓ |

`Heaven's Gate`(天堂之门) | `linux` | `retf`

天堂之门是基于WoW64的windows技术，但也能应用在linux上。0x23表示32位模式执行，0x33表示64位模式执行，retf是切换两种模式的关键指令。如果碰上反汇编异常，可以尝试把机器码提取出来单独用在线网站反汇编。ida可以调，但是得用64位调而且得在执行64位代码前通过`Edit->Segments->Edit segment`将text段设置为64位，执行完后再改回32位。

## Heart Protector

> Deep within the arcane forges of Eldoria, an ancient construct—woven from enchanted code and sealed by cryptic sigils—guards a powerful secret. Its core holds the Heart of Eldoria, concealed within layers of illusion and deception. Only those who unravel its intricate workings can restore what was lost. Will you be the one to break its curse?

| points:  | solutions:  |
|-------|-------|
| files:  | issolved: ✓ |

`Nim Language` | `AES-GCM`