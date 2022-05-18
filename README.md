# caesars-cipher

A library that provides a simple interface to the ceasers cipher with a large range.

Uses the legal range of UTF-8 instead of the regular alphabet: **0x80** _(128)_

`caesars-cipher/base64`: Converts to base64 then shifts them.
`caesars-cipher/uri-encoded`: Encodes as uri then shifts them.

![image](https://user-images.githubusercontent.com/34271483/169030025-f58720e8-6800-4bab-921e-c1a12565b895.png)

You can try it out at the widget at [berkekaragoz.com](https://berkekaragoz.com).

## Usage

```ts
import { caesarsCipher, caesarsDecipher } from "caesars-cipher/base64";
// OR
import { caesarsCipher, caesarsDecipher } from "caesars-cipher/uri-encoded";

caesarsCipher("Cipher", 10); // Mszro|
caesarsDecipher("Mszro|", 10); // Cipher
```

Types:

```ts
type CaesarsCipher = (text: string, shiftAmount: number) => string;
type CaesarsDecipher = (cipheredText: string, shiftAmount: number) => string;
```
