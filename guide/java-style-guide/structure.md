# Structure

[go back](README.md)

# Order of top-level declarations in a file

Each file should have declarations in the following order:

1. Package statement
2. Import statements
3. Class/interface/enum

```java
package org.usfirst.frc.team4253.robot;

import edu.wpi.first.wpilibj.SampleRobot;
import edu.wpi.first.wpilibj.SmartDashboard;

public class Robot extends SampleRobot {
    // ...
}
```

# Order of declarations in classes

Declarations in classes should generally have the following order:

1. Constants
2. Static variables
3. Instance variables
4. Constructors
5. Methods
6. Nested classes/interfaces

The methods should be ordered in some logical way. Don't just always add new methods to the bottom of the class. Also, overloads of a method should always be next to each other.

The order specified here is just a general rule. If there is a good reason to put something somewhere else, then do it.
