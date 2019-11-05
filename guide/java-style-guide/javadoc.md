# Javadoc

[go back](README.md)

Javadoc comments are a way to document Java code.

```java
/**
 * Adds two numbers.
 *
 * @param a the first number
 * @param b the second number
 * @return the sum of the two numbers
 */
public int add(int a, int b) {
    return a + b;
}
```

To start a Javadoc comment, just put your cursor on the line above a method, or whatever you want to document, then type `/**` and press tab to autocomplete. VSCode will insert the rest of the comment automatically, including any necessary tags.

# Where to use

Javadoc comments should be present for the following things:

- Top-level classes, interfaces, and enums
- Public methods
    - Except if the method overrides or implements another method
- Public constructors
- Public variables, constants, and inner classes/interfaces/enums of a class

Exception: You can omit Javadoc comments if the thing you are documenting has a self-explanatory name, and there is not much to say in the comment.

The list above is just where Javadoc comments are required. You are welcome to add Javadoc comments for other things, such as private methods, if you want to.

# Content

The Javadoc comment should start with a short description.

If more documentation is needed, you can add more paragraphs. For example:

```java
/**
 * Adds two numbers.
 *
 * <p>This method is pretty useless actually. You probably won't ever call this method. You could
 * just use the + operator directly to add two numbers.
 *
 * <p>In fact, the only reason this method exists is to demonstrate how to write Javadoc comments.
 * In this example, there are multiple paragraphs in the comment. Notice how you can split the
 * paragraph onto multiple lines. You should do this if your paragraph is too long.
 *
 * @param a the first number
 * @param b the second number
 * @return the sum of the two numbers
 */
public int add(int a, int b) {
    return a + b;
}
```

For each parameter, there should be a `@param` tag. The first word after it is the name of the parameter. Then, after the name is the description of that parameter.

If the method returns something, i.e. not `void`, there should be a `@return` tag, followed by a description of what it returns.
