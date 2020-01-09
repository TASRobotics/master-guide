# Formatting

[go back](README.md)

# Line length limit

If you have a line with more than **100 characters** in it, you should break it up into multiple lines. This is called line wrapping. [Javadoc comments](javadoc.md) should be line wrapped as well.

Exceptions:
- Package declaration and imports
- Things that cannot be split like long URLs

Note: Feel free to break up statements into multiple lines even if they don't exceed 100 characters. It often increases readability.

When wrapping lines, don't just break at the point closest to the limit. You should break the line in a way that it is easy to read.

Most editors have a "ruler" setting that can be enabled to show a vertical line at the line length limit.

# Braces (`{}`)

## Places where braces are optional

**Use braces even when they are optional**, such as in `if` and `for` statements where there is only one statement in the body.

Omitting braces when they are optional is a possible source of bugs.

```java
// GOOD

if (condition) {
    doSomething();
} else {
    doSomethingElse();
}

while (true) {
    println("This will loop forever");
}

// BAD

if (condition)
    doSomething();
else
    doSomethingElse();

while (true)
    println("This will loop forever");
```

## Positioning of braces

```java
public class someClass { // opening brace on the same line

    public void someMethod() { // same for methods

        for (int i = 0; i < 100; i++) { // same for control structures
            println(i);
        } // closing brace on its own line

        if (condition) {
            doSomething();
        } else { // closing brace of if combined with else
            doSomethingElse();
        }

    }

}
```

For a more formal definition, this is from [Google's style guide](https://google.github.io/styleguide/javaguide.html):

> - No line break before the opening brace.
> - Line break after the opening brace.
> - Line break before the closing brace.
> - Line break after the closing brace, only if that brace terminates a statement or terminates the body of a method, constructor, or named class. For example, there is no line break after the brace if it is followed by `else` or a comma.

If a method is empty, you can put it all on one line.

```java
public void emptyMethod() {}
```

## Array initializers and enums

If you have a short array initializer you can format it like this:

```java
int[] x = { 1, 2, 3 };
```

But if you have a long array initializer you can also format it like a block.

```java
int[] x = {
    calculateFirstElement(),
    calculateSecondElement(),
    calculateThirdElement()
};
```

The same thing applies to enum declarations.

# Spacing

## Blank lines

You can add blank lines in between statements to group them logically. This is useful for long methods or if a class has many instance variables.

Also, there should be one blank line in between:
- [each of these sections](structure.md#order-of-top-level-declarations-in-a-file)
- [each of these sections](structure.md#order-of-declarations-in-classes)
- constructors/methods

as well as before the first thing in a class and after the last thing.

## Spaces

There should be no extra spaces at the end of a line.

For inside the line, put one space:

- Between any keyword and opening parenthesis (`(`), e.g. `if`, `for`
- Before any opening brace (`{`)
    - Except if it is preceded by another opening brace (when you are initializing a matrix)
- Inside both braces of an array initializer
- Between any closing brace (`}`) and keyword, e.g. `else` (see also [Positioning of braces](#positioning-of-braces))
- Before and after binary or ternary operators
    - Except the `.` operator
- After `,` or `;`
- After `//` that starts a comment
- Before `//` if there is code before it

```java
public void someMethod(int x, int y) {
    if (x == y) { // this is a comment
        someObject.methodCall(1, 2, 3);
    } else {
        int z = 0;
        for (int i = 0; i < x; i++) {
            z += y * i + 1;
        }
    }
}
```

# Decimals

Always put a `0` in front of the `.` if it is optional.

```java
0.1
-0.1
```
