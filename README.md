# C Sharp-Herency-work-Unity

Inheritance in C# is a powerful feature that allows you to create a new class that reuses, extends, and modifies the behavior defined in another class. In the provided code, inheritance is used to create a specialized enemy class EnemyFind that extends the base class EnemyScript.

Here's a detailed explanation of how inheritance is used in this context:

## Base Class: EnemyScript
The EnemyScript class is the parent class for all enemy types. It contains properties and methods that are common to all enemies.

https://github.com/Yceballos/C-Sharp-Herency-work-Unity/blob/main/Code/C%23_Scripts_Yasmin%20Ceballos.rar

## Derived Class: EnemyFind
The EnemyFind class is a specialized type of enemy that inherits from EnemyScript. This class adds new behavior to the enemy, such as pursuing the player when within a certain range.

## Key Points of Inheritance Usage
### Extending Functionality:
EnemyFind extends EnemyScript to inherit its properties and methods, enabling it to use the common functionality provided by EnemyScript.

### Protected Members:
EnemyScript uses protected access modifiers for members like Rigidbody2D, Animator, and Horizontal. This allows EnemyFind to access and use these members directly.

### Overriding Methods:
While not explicitly shown in this example, you can override methods in the derived class to provide specific implementations. For instance, EnemyFind could override a method from EnemyScript if it needed different behavior.

+-----------------+ +-----------------+
| EnemyScript | | EnemyFind |
+-----------------+ +-----------------+
| - Rigidbody2D | | - isVisible |
| - Animator | | - player |
| - speed | | - posPlayer |
| - MaxHealth | | - rangeXToActivate |
| - damage | | - rangeYToActivate |
+-----------------+ +-----------------+
| + Start() | | + search() |
| + Update() | +-----------------+
| + FixedUpdate() |
| + Hit() |
| + Die() |
+-----------------+


### Calling Base Class Methods:
You can call base class methods using the base keyword if you need to extend or modify the behavior of inherited methods without completely replacing them. Other way to see how Inheritance works:

![image](https://github.com/Yceballos/C-Sharp-Herency-work-Unity/assets/90511756/17baa29a-53d3-415e-bb81-a41bf37ab47b)

Inheritance allows for code reuse and the creation of more complex behavior by building on existing functionality, making the codebase easier to manage and extend.
