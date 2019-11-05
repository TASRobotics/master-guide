# Miscellaneous

Miscellaneous stuff.

# @Override

Always use the `@Override` annotation when you are overriding a superclass method or implementing an interface method.

```java
class SomeClass {
    public void superclassMethod() {
        // ...
    }
}

interface SomeInterface {
    void interfaceMethod();
}

class AnotherClass extends SomeClass implements SomeInterface {

    @Override
    public void superclassMethod() {
        // ...
    }

    @Override
    public void interfaceMethod() {
        // ...
    }

}
```
