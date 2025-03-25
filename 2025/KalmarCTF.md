# KalmarCTF

## Snake I - Just One More
> It's a simple SNES game of Snake… or is it? Each apple you eat reveals a letter, but before you can spell out the full flag, the apples run out.
> 
> If only there were another way to uncover the secret… perhaps by diving into the depths of 65816 assembly and extracting the flag directly from the game's code?
> 
> Can you outsmart the limitations and claim your prize?
> 
> Note: flag submission is not case sensitive for this challenge. The flag contains underscores, but not dashes.

| points: 183 | solutions: 59 |
|-------|-------|
| files: snake.sfc | issolved: lock |

`snes`

## FlagSecurityEngine
> The Kalmar FlagSecurityEngine™'s usage of the loadall() function will surely protect the flag from reverse engineering, right?
> 
> Note: this challenge is meant to serve as an introduction to the pwn loadall.js challenge. Solving this challenge first is recommended.We've developed a new security engine that can detect flags in any file! It's so good, it can even detect flags in itself!

| points: 221 | solutions: 40 |
|-------|-------|
| files: flagsecurityengine | issolved: lock |

`Monkey Patch` | `quickjs` | `JavaScript` | `Zig`

```js
// load the Kalmar Flag Security Engine™
loadall((new Uint8Array([67, 9, 18, 117, 115, 101, 32, 115, 116, 114, 105, 112, 18, 99, 104, 101, 99, 107, 70, 108, 97, 103, 2, 95, 6, 109, 97, 112, 24, 102, 114, 111, 109, 67, 104, 97, 114, 67, 111, 100, 101, 20, 99, 104, 97, 114, 67, 111, 100, 101, 65, 116, 10, 112, 114, 105, 110, 116, 22, 87, 114, 111, 110, 103, 32, 102, 108, 97, 103, 33, 22, 82, 105, 103, 104, 116, 32, 102, 108, 97, 103, 33, 12, 0, 2, 2, 162, 1, 0, 2, 0, 3, 0, 1, 19, 0, 8, 204, 4, 227, 0, 0, 0, 203, 200, 194, 0, 21, 67, 228, 0, 0, 0, 207, 40, 12, 67, 2, 2, 200, 3, 1, 6, 1, 32, 0, 3, 219, 3, 0, 97, 4, 0, 97, 3, 0, 97, 2, 0, 97, 1, 0, 97, 0, 0, 194, 0, 77, 229, 0, 0, 0, 203, 98, 0, 0, 204, 193, 1, 205, 195, 206, 191, 98, 191, 57, 191, 35, 191, 34, 191, 42, 191, 41, 191, 104, 191, 79, 191, 18, 191, 28, 191, 29, 191, 75, 191, 55, 183, 191, 49, 191, 33, 191, 37, 191, 46, 191, 65, 191, 21, 191, 120, 191, 99, 191, 123, 191, 68, 191, 112, 191, 20, 191, 78, 191, 19, 191, 61, 191, 31, 191, 54, 191, 122, 38, 32, 0, 191, 39, 76, 32, 0, 0, 128, 191, 123, 76, 33, 0, 0, 128, 191, 23, 76, 34, 0, 0, 128, 191, 29, 76, 35, 0, 0, 128, 191, 30, 76, 36, 0, 0, 128, 191, 52, 76, 37, 0, 0, 128, 190, 76, 38, 0, 0, 128, 188, 76, 39, 0, 0, 128, 191, 103, 76, 40, 0, 0, 128, 190, 76, 41, 0, 0, 128, 191, 95, 76, 42, 0, 0, 128, 191, 127, 76, 43, 0, 0, 128, 188, 76, 44, 0, 0, 128, 191, 57, 76, 45, 0, 0, 128, 191, 58, 76, 46, 0, 0, 128, 189, 76, 47, 0, 0, 128, 191, 105, 76, 48, 0, 0, 128, 191, 84, 76, 49, 0, 0, 128, 191, 60, 76, 50, 0, 0, 128, 191, 55, 76, 51, 0, 0, 128, 191, 34, 76, 52, 0, 0, 128, 191, 44, 76, 53, 0, 0, 128, 191, 100, 76, 54, 0, 0, 128, 191, 90, 76, 55, 0, 0, 128, 191, 84, 76, 56, 0, 0, 128, 191, 100, 76, 57, 0, 0, 128, 187, 76, 58, 0, 0, 128, 191, 12, 76, 59, 0, 0, 128, 191, 59, 76, 60, 0, 0, 128, 191, 54, 76, 61, 0, 0, 128, 191, 64, 76, 62, 0, 0, 128, 191, 76, 76, 63, 0, 0, 128, 191, 92, 76, 64, 0, 0, 128, 191, 120, 76, 65, 0, 0, 128, 66, 230, 0, 0, 0, 194, 2, 36, 1, 0, 66, 92, 0, 0, 0, 195, 36, 1, 0, 197, 4, 97, 5, 0, 183, 197, 5, 98, 5, 0, 211, 235, 164, 236, 76, 98, 3, 0, 56, 155, 0, 0, 0, 66, 231, 0, 0, 0, 211, 66, 232, 0, 0, 0, 98, 5, 0, 36, 1, 0, 98, 2, 0, 191, 95, 174, 175, 36, 1, 0, 158, 17, 99, 3, 0, 14, 98, 1, 0, 98, 2, 0, 211, 66, 232, 0, 0, 0, 98, 5, 0, 36, 1, 0, 242, 17, 99, 2, 0, 14, 98, 5, 0, 146, 99, 5, 0, 14, 238, 174, 98, 3, 0, 98, 4, 0, 171, 236, 14, 56, 233, 0, 0, 0, 4, 234, 0, 0, 0, 241, 14, 41, 56, 233, 0, 0, 0, 4, 235, 0, 0, 0, 241, 14, 41, 12, 66, 2, 2, 0, 2, 1, 2, 3, 0, 0, 57, 0, 97, 0, 0, 183, 203, 98, 0, 0, 191, 16, 164, 236, 41, 211, 211, 191, 15, 162, 175, 219, 211, 191, 13, 161, 175, 219, 211, 191, 17, 162, 175, 215, 212, 211, 175, 216, 211, 212, 191, 11, 162, 175, 215, 98, 0, 0, 146, 99, 0, 0, 14, 238, 209, 211, 212, 175, 40, 6, 0, 0, 32, 241, 11, 124, 234, 65, 12, 66, 2, 2, 0, 2, 0, 2, 4, 0, 0, 16, 0, 56, 155, 0, 0, 0, 66, 231, 0, 0, 0, 211, 212, 175, 37, 1, 0])).buffer)

const originalFromCharCode = String.fromCharCode;
const charset = "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ!#$%&\'()*+,-./:;<=>?@[\\]^_`{|}~";

var transformationLog = [];

String.fromCharCode = function(...args) {
    //print(`fromCharCode called with: ${JSON.stringify(args)}`);
    transformationLog.push(args[0]);
    return originalFromCharCode.apply(this, args);
};

var correct_flag = 'kal'
var correct = 3;
var i = 0;

while(true){
    test_char = charset[i];
    flag = correct_flag + test_char;
    transformationLog = [];
    print("checking: " + flag)
    checkFlag(flag)
    i += 1;
    //print("log: " + JSON.stringify(transformationLog[66]));
    if (transformationLog[66 + correct] == transformationLog[correct]){
        correct += 1;
        correct_flag = flag;
        print("correct: " + correct_flag)
        i = 0;
    }
}

print(correct_flag)
// 98,56,33,33,46,44,110,72,26,21,23,64,59,13,63,46,53,63,83,6,108,118,109,83,104,13,84,8,33,2,40,101,7,90,53,62,58,17,33,34,79,46,117,84,41,20,20,41,89,101,14,4,22,25,82,109,108,93,62,55,7,11,126,115,28,57,
// 98,56,33,33,46,44,110,96,49,97,46,58,122,102,43,54,41,43,54,47,124,46
```

## Shafus
> Shafus wanted to make his SHA-256 implementation "faster" and "better." The result? A monstrous mess of inlined code, obfuscation through sheer redundancy, and a nightmare for anyone trying to read it.
> 
> Can you navigate through the tangled code and figure out how Shafus actually works? The flag awaits those who can untangle the chaos!

| points: 343 | solutions: 16 |
|-------|-------|
| files: shafus_easy | issolved: lock |

## Jormungandr
> Remember rabbit hole from last year? This one goes even deeper!

| points: 427 | solutions: 10 |
|-------|-------|
| files: jormungandr | issolved: lock |

## Snake II - Sonic Snake Fighter II
> The stakes have been raised! This time, the snake game isn't just about apples—there's a whole new dimension to explore. Hidden within the depths of this SNES game lies a secret, waiting to be uncovered by those skilled enough to decode its mechanics.
> 
> Some say there’s more happening behind the scenes than meets the eye. Only those who truly understand the inner workings of the system will uncover the flag.
>
> Note: This challenge is not about snakes and apples, you don't need to spend your time on reading 65816 disassembly, it really sounds like the flag got hadouken'd to another castle

| points: 1000 | solutions: 0 |
|-------|-------|
| files: snake.sfc | issolved: lock |

## Shafus Gone Crazy
> You thought you knew SHA-256? Think again. Somewhere in the depths of obfuscation madness, Shafus the Algorithmic Trickster decided to "improve" the standard hash function with a mix of bizarre mathematical operations, unexpected transformations, and a sprinkle of chaos.
> 
> Your task is to reverse engineer Shafus' deranged creation, understand its quirks, and break through the cryptographic maze to uncover the hidden flag.
> 
> Can you untangle the madness, or will you be left questioning reality itself?

| points: 1000 | solutions: 1 |
|-------|-------|
| files: shafus_hard | issolved: lock |

## Snake III - Hungry for Snake
> This isn't your average game of Snake. Every move matters, every apple counts, and every decision takes you deeper into the mystery. Precision and strategy are your greatest tools as you navigate through the puzzle.
> 
> Something curious happens with every apple you collect — patterns emerge, numbers grow, and the game begins to reveal its secrets. But the path ahead is anything but simple. Each action you take builds upon the last, and the hidden mechanics beneath the surface hold the key to your success.
> 
> Can you decode the clues, master the system, and uncover the hidden flag? Only those who can unravel the logic behind the puzzle will succeed in solving its mysteries. Are you one of them?
>
> Note: The solution to this is unrelated to the solution to snake 2.

| points: 1000 | solutions: 0 |
|-------|-------|
| files: snake.sfc | issolved: lock |