# asnk-vas1
cryptographic algorithm for encrypting text, salt-based
<br>
<a href="https://marshallovski.github.io/asnk-vas1/playground/">Live playground</a>

## Salt variants
you can use any other salt-generator, see other methods in `./utils/salt`
<br>
also, you can write your own, but important thing is - salt must be a number 

## Possibilities
`vas-1` can be used in a browser, or a server.
<br>
Vas-1 uses `String.charCodeAt` and `String.fromCharCode` to transform characters. All characters could be encrypted (maybe).

# Usage example
```js
// in browser, don't forget to add `type="module"` to your <script>
const asnk = new Asnk('vas-1');

import { cryptoRandomNumber } from "./utils/salt/cryptoRandomNumber.js"; 

const text = 'Hello, World!';
const salt = await cryptoRandomNumber();

const encryptedText = await asnk.encrypt({ text, salt });
console.log(encryptedText);
```

<b>Also, see `index.js`</b>
