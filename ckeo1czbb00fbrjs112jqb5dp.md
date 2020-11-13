## Nim for beginners - Introduction & Basics

## What is Nim?

The best way to describe Nim, is just by quoting their own description.

> Nim is a statically typed compiled systems programming language. It combines successful concepts from mature languages like Python, Ada and Modula.

Nim is an not so common language that have been recently released its 1.0 version. I've been playing with it on my freetime, just to geek out a bit, and I find it very well structured with a nice community around it.

## How to install?

The easiest way to install it is just by using the package manager of your operating system/distribution. In my case I installed it in OSX with brew:

```
brew install nim
```

On my Windows machine I installed it with:

```
choco install nim
```

For other instructions on how to install, simply go to the  [downloads page](https://nim-lang.org/install.html)  on Nim's website. When you're done installing, we can check if everything is installed properly by check the version on the terminal with the following commands:

```js
// Get installed version of Nim
nim -v

// Version of Nim package manager
nimble -v
```

## Hello World example

Start by creating a file with `.nim` extension, for example `hello.nim`. In Nim to print something we can simple use the `echo` procedure for this. Functions are called procedures in Nim.

```nim
echo "Hello World"
```

This reminds me a little of PHP, with the exception that here we don't need to end the line with the `;` symbol. To run your code, use the following command:

```
nim c -r hello
```

The `c` command stand for "compile", the `-r` flag stands for "run" and the `hello` argument is the name of the binary to run after compilation.

The `echo` procedure is actually a bit different than other procedures, since it can take an unspecified number of arguments, so the next expression would also be correct.

```nim
echo "Hello World"
echo "My name is Rafael ", "I am 26."
```

This will print two lines, one with `Hello World`, and another line containing `My name is Rafael. I am 26.`. Feel free to test more on your own.

