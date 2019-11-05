# Naming

# Camel case

```java
UpperCamelCase
lowerCamelCase
```

If there is an acronym:

```java
PIDController // UpperCamelCase
pidController // lowerCamelCase
```

# Classes

- `UpperCamelCase`
- Typically nouns or noun phrases

# Interfaces

- `UpperCamelCase`
- Typically nouns or noun phrases or adjectives or adjective phrases

# Enums

- `UpperCamelCase`
- Typically nouns or noun phrases

# Enum values

- `UpperCamelCase`

# Methods

- `lowerCamelCase`
- Typically verbs or verb phrases

## Getters

The getter for a variable `var` should be called `getVar`.

Except if the variable is a boolean, then it can start with `is`, like `isOpen` for `open`.

## Setters

The setter for a variable `var` should be called `setVar`.

# Constants

- `CONSTANT_CASE`
- Typically nouns or noun phrases

# Variables and parameters

- `lowerCamelCase`
- Typically nouns or noun phrases

## Parameters of setters

If you have a setter to set some instance variable and you have nothing meaningful to name the parameter, just give it the same name as the instance variable. When you are assigning it you can use `this` to reference the instance variable.

The same applies to constructors which behave like setters.

```java
// GOOD
public void setValue(int value) {
    this.value = value;
}

// BAD
public void setValue(int theValue) { // theValue doesn't proivde any extra meaning
    value = theValue;
}
```

## Exceptions

Exception objects (i.e. anything that is an instance of either Exception or a subclass of Exception) should be named `andrew`.

```java
try {
    // do stuff
} catch (Exception andrew) {
    // handle exception
}
```

# Special prefixes

Don't use special prefixes.

```java
// GOOD
someMember
SOME_CONSTANT
SomeClass

// BAD
m_someMember
kSomeConstant
CSomeClass
```
