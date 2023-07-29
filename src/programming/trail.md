# The Trail Language

Silly ideas about how a language should have all its syntax trailing.

## Syntax

- Keywords are capitalized letters.
    - They will look fine with syntax highlighting.
- White spaces separate tokens.
    - `a+b` is a single token, it can not involve procedure call.
- Expressions are evaluated left to right, with no operator precedence.

```lua
1 A a -- Assign `1` to `a`.
true M b -- Mutable variable.
a / 2.0 A a/2 -- Call procedure `/` with `a` and `2.0` and assign to `a/2`.
false R b -- Reassign `b`.
0..10 E { "Hey" print } -- Print "Hey" 10 times.
```

## Procedures

- The last expression is the return value.
    - No "return" keyword.
- Procedures are automatically called with the variable before it and the
    appropriate number of variables after it.
- If a procedure does not take any arguments, it should be called with `( )`.
- Limited polymorphism: the first argument of the function decides what the
    rest of the function arguments could be.

```lua
P a b { a + b } A add -- Procedure `add`.

P { "hell" ++ "o" } A greet -- Procedure `greet`.

( ) greet A hello
```

## Names

Symbols can be names.

```lua
P a b { a pow b } A ** -- Procedure `**`.
```

## Compile-time computation

The program is interpreted into a program that gets compiled.

- During interpretation, expressions marked with `C` are calculated.
- Global variables are always calculated at compile time and immutable at run
    time.
- Compile-time variables can also be declared "mutable at compile time."

```lua
32 * 32 A TWO_TO_TEN -- Compile-time.

P a b {
    b * b A b_square -- Run-time.
    a * TWO_TO_TEN + b_square -- Run-time.
} A hyperbole -- Compile-time.

P x {
    2 hyperbole 7 A C LUCKY_NUMBER -- Compile-time.
    x + LUCKY_NUMBER -- Run-time.
} A add_luck -- Compile-time.

2 M TO_BE_CHANGED -- Compile-time mutable.
0..10 E { TO_BE_CHANGED * TO_BE_CHANGED R TO_BE_CHANGED } -- Compile-time
-- `TO_BE_CHANGED` = 4294967296
```
