# Codenotes

## You Don't Know JS - Ch1 + Ch2
Although JavaScript falls under the general category of 'dynamic' or 'interpreted' languages, it is, in fact, a compiled language. -> Not in advance, but at runtime (JustInTime-compiler, JIT).

The JavaScript engine is far more complex than just parsing and generating. For instance, JavaScript engines don't have the time to optimize ahead of build time.

There are 3 main players:
1. Engine: compilation and execution of JS programs

2. Compiler: parsing and code generation

3. Scope: collects and maintains a look-up list of all declarations and enforces a strict set of rules for accessing these declarations

## What is scope?
Scope is the context in which you are writing code. 

It is like a set of rules that determines where and how a variable can be looked up within a program by the Engine For instance, a function has it's own scope like this:

```js
// This is outside the function scope, in this case the global scope

function sayHello() {

    // This is the function scope
}
```
### Lexical Scope
 This is referred to as the **_Lexical Scope_** which a lot of programming languages use, so it is very common. To sum this up into 1 sentence: Lexical scope means that a variable is only accessible within the scope in which it has been declared.

And to make it a bit more clear:

```js
// The const name is not available here
console.log(name) // undefined

function sayHello() {
    // The const name is only available within this block

    const name = 'Tristan'
    console.log(name)
}
```
