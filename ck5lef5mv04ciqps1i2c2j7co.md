## How to Make First Letter Uppercase in Javascript

If you have the need to uppercase just the first letter of a string in JavaScript like I did, just keep reading this article, because this is for you. There are multiple ways to achieve this, so I'll try to document them the best way I can.

The quick and dirtiest way, uses three common functions and basically selects the first letter and makes it uppercase, while leaving the rest untouched.

```
const greet = "hello world!";
const greetCapitalized = greet.charAt(0).toUpperCase() + greet.slice(1);
```

What this does is basically isolate the first letter of the string, `h` in this case and transform it into an uppercase `H` with the help of `.toUpperCase()`. After this is done, we need to concatenate with the rest of the string using `.slice()` . Notice that we start on position 1 instead of position 0, and this is basically because position 0 is the `h` , its actually the first letter.

The expression above could be translated to this:

```
const greetCapitalized = "H" + "ello world!";
```

If you need to use this logic multiple times, the best way would be to create a a function and keep reusing it everywhere you need it.

```
const capitalize = function(s) {
    if (typeof s !== 'string') return '';
    return s[0].toUpperCase() + s.slice(1);
}

capitalize('hello world!') // 'Hello world!'
capitalize('h')      // 'F'
capitalize(0)        // ''
capitalize({})       // ''
```

In this function you can notice that I used `s[0]` instead of `s.charAt(0)` but use this only if you are not targeting older versions of IE.