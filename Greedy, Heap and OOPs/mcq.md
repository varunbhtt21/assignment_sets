# Greedy, Heap and OOPs - MCQ Questions
## (Java Object-Oriented Programming Concepts)

---

### Q1.

What is a class in Java?

A. A runtime entity

B. A blueprint or template for creating objects

C. A method

D. A variable

**Answer:** B

**Explanation:** A class is a blueprint or template that defines the properties (fields) and behaviors (methods) that objects created from the class will have. It's a logical construct that doesn't consume memory until objects are instantiated.

---

### Q2.

What is an object in Java?

A. A class definition

B. An instance of a class

C. A method

D. A data type

**Answer:** B

**Explanation:** An object is an instance of a class. It's a runtime entity that has state (values of instance variables) and behavior (methods). Objects are created using the `new` keyword.

---

### Q3.

Which keyword is used to create an object in Java?

A. class

B. object

C. new

D. create

**Answer:** C

**Explanation:** The `new` keyword is used to create an object (instance) of a class. For example: `MyClass obj = new MyClass();` creates a new object of MyClass.

---

### Q4.

What is encapsulation in Java?

A. Hiding implementation details and exposing only necessary information

B. Creating multiple classes

C. Inheritance of properties

D. Method overloading

**Answer:** A

**Explanation:** Encapsulation is the bundling of data (fields) and methods that operate on that data within a single unit (class), and restricting direct access to some components. It's achieved using access modifiers like private, protected, and public.

---

### Q5.

Which access modifier makes a member accessible only within the same class?

A. public

B. protected

C. private

D. default

**Answer:** C

**Explanation:** The `private` access modifier restricts access to members (fields and methods) to only within the same class. It's the most restrictive access level and is fundamental to encapsulation.

---

### Q6.

What is inheritance in Java?

A. A mechanism where one class acquires properties and behaviors of another class

B. Creating multiple objects

C. Hiding data

D. Method overloading

**Answer:** A

**Explanation:** Inheritance is an OOP concept where a new class (subclass/child class) is created based on an existing class (superclass/parent class), inheriting its fields and methods. It promotes code reusability.

---

### Q7.

Which keyword is used to inherit a class in Java?

A. inherits

B. extends

C. implements

D. super

**Answer:** B

**Explanation:** The `extends` keyword is used for class inheritance in Java. For example: `class Dog extends Animal` means Dog inherits from Animal class.

---

### Q8.

Does Java support multiple inheritance through classes?

A. Yes

B. No

C. Only with interfaces

D. Depends on the compiler

**Answer:** B

**Explanation:** Java does NOT support multiple inheritance through classes to avoid the "diamond problem". However, Java supports multiple inheritance through interfaces (a class can implement multiple interfaces).

---

### Q9.

What is polymorphism in Java?

A. Having multiple forms or behaviors

B. Creating multiple classes

C. Data hiding

D. Code encryption

**Answer:** A

**Explanation:** Polymorphism means "many forms". In Java, it allows objects to be treated as instances of their parent class, and methods can behave differently based on the object type (method overriding) or parameters (method overloading).

---

### Q10.

What are the two types of polymorphism in Java?

A. Static and Dynamic

B. Compile-time and Runtime

C. Method overloading and Method overriding

D. Both B and C are correct

**Answer:** D

**Explanation:** Polymorphism has two types: Compile-time (static/early binding) achieved through method overloading, and Runtime (dynamic/late binding) achieved through method overriding. Options B and C describe the same concepts using different terminology.

---

### Q11.

What is method overloading in Java?

A. Multiple methods with the same name but different parameters in the same class

B. Redefining a method in a subclass

C. Hiding a method

D. Creating abstract methods

**Answer:** A

**Explanation:** Method overloading (compile-time polymorphism) occurs when multiple methods in the same class have the same name but different parameter lists (different number, types, or order of parameters).

---

### Q12.

What is method overriding in Java?

A. Creating multiple methods with same name

B. Providing a specific implementation in a subclass for a method already defined in the parent class

C. Method hiding

D. Abstract method implementation

**Answer:** B

**Explanation:** Method overriding (runtime polymorphism) occurs when a subclass provides its own implementation of a method that is already defined in its parent class. The overridden method must have the same signature.

---

### Q13.

Which annotation is used to indicate method overriding in Java?

A. @Overload

B. @Override

C. @Inherit

D. @Polymorphic

**Answer:** B

**Explanation:** The `@Override` annotation is used to indicate that a method is intended to override a method in the superclass. While optional, it helps catch errors at compile-time if the method doesn't actually override anything.

---

### Q14.

Can we override static methods in Java?

A. Yes

B. No, static methods are hidden, not overridden

C. Only with @Override annotation

D. Depends on access modifier

**Answer:** B

**Explanation:** Static methods cannot be overridden in Java; they can only be hidden. Method overriding is based on dynamic binding at runtime, while static methods are bound at compile-time based on the reference type.

---

### Q15.

Can we override private methods in Java?

A. Yes

B. No, private methods are not inherited

C. Only in the same package

D. Only with reflection

**Answer:** B

**Explanation:** Private methods cannot be overridden because they are not inherited by subclasses. They are only accessible within the class where they are defined.

---

### Q16.

What is an interface in Java?

A. A class with all concrete methods

B. A reference type containing only abstract methods (before Java 8) and constants

C. A data type

D. An object

**Answer:** B

**Explanation:** An interface is a reference type that contains abstract method declarations (and constants). From Java 8+, interfaces can also have default and static methods with implementations. Interfaces define a contract that implementing classes must follow.

---

### Q17.

Which keyword is used to implement an interface in Java?

A. extends

B. implements

C. inherits

D. uses

**Answer:** B

**Explanation:** The `implements` keyword is used when a class wants to implement an interface. For example: `class MyClass implements MyInterface`. A class can implement multiple interfaces.

---

### Q18.

Can a class implement multiple interfaces in Java?

A. No

B. Yes

C. Only if interfaces don't have common methods

D. Only abstract classes can

**Answer:** B

**Explanation:** Yes, a class can implement multiple interfaces in Java. This is how Java achieves multiple inheritance of type. For example: `class MyClass implements Interface1, Interface2, Interface3`.

---

### Q19.

What is an abstract class in Java?

A. A class that cannot be instantiated and may contain abstract methods

B. A fully implemented class

C. An interface

D. A final class

**Answer:** A

**Explanation:** An abstract class is declared with the `abstract` keyword, cannot be instantiated directly, and may contain abstract methods (methods without implementation) that must be implemented by subclasses.

---

### Q20.

Which keyword is used to declare an abstract class in Java?

A. interface

B. abstract

C. virtual

D. final

**Answer:** B

**Explanation:** The `abstract` keyword is used to declare an abstract class. For example: `abstract class Animal { }`. Abstract classes can have both abstract and concrete methods.

---

### Q21.

Can an abstract class have a constructor in Java?

A. No

B. Yes

C. Only if it has no abstract methods

D. Only protected constructors

**Answer:** B

**Explanation:** Yes, abstract classes can have constructors. They are called when a subclass is instantiated. The constructor is used to initialize the abstract class's fields.

---

### Q22.

What is the difference between an abstract class and an interface?

A. Abstract class can have constructors; interface cannot

B. Abstract class can have concrete methods; interface can only have abstract methods (before Java 8)

C. A class can extend one abstract class but implement multiple interfaces

D. All of the above

**Answer:** D

**Explanation:** All statements are correct. Abstract classes can have constructors, concrete methods, and fields. A class can extend only one abstract class (single inheritance) but implement multiple interfaces. From Java 8+, interfaces can have default and static methods.

---

### Q23.

Can an interface extend another interface in Java?

A. No

B. Yes, using extends keyword

C. Yes, using implements keyword

D. Only if both are abstract

**Answer:** B

**Explanation:** Yes, an interface can extend another interface using the `extends` keyword. An interface can even extend multiple interfaces. For example: `interface C extends A, B { }`.

---

### Q24.

What is the default access modifier for interface methods (before Java 9)?

A. private

B. protected

C. public

D. default

**Answer:** C

**Explanation:** Before Java 9, all methods in an interface were implicitly public and abstract. From Java 9+, interfaces can also have private methods.

---

### Q25.

Can we declare a constructor in an interface?

A. Yes

B. No

C. Only static constructors

D. Only with default keyword

**Answer:** B

**Explanation:** No, interfaces cannot have constructors because they cannot be instantiated. Interfaces define contracts for behavior, not state initialization.

---

### Q26.

What is the `super` keyword used for in Java?

A. To refer to the immediate parent class object

B. To call parent class constructor

C. To access parent class methods and variables

D. All of the above

**Answer:** D

**Explanation:** The `super` keyword is used to refer to the immediate parent class. It can be used to call parent class constructor (`super()`), access parent class methods (`super.method()`), and access parent class variables (`super.variable`).

---

### Q27.

What is the `this` keyword used for in Java?

A. To refer to the current class instance

B. To call current class constructor

C. To pass current object as parameter

D. All of the above

**Answer:** D

**Explanation:** The `this` keyword refers to the current object instance. It's used to access instance variables (`this.variable`), call constructors (`this()`), call instance methods (`this.method()`), and pass the current object as a parameter.

---

### Q28.

Can a final class be inherited in Java?

A. Yes

B. No

C. Only by abstract classes

D. Only within the same package

**Answer:** B

**Explanation:** No, a final class cannot be inherited. The `final` keyword with a class prevents inheritance. For example, the String class in Java is final.

---

### Q29.

Can a final method be overridden in Java?

A. Yes

B. No

C. Only with @Override annotation

D. Only in abstract classes

**Answer:** B

**Explanation:** No, a final method cannot be overridden by subclasses. The `final` keyword with a method prevents method overriding, ensuring the method's implementation cannot be changed.

---

### Q30.

What happens if we don't provide a constructor in a Java class?

A. Compilation error

B. The compiler provides a default no-argument constructor

C. The class cannot be instantiated

D. Runtime error

**Answer:** B

**Explanation:** If no constructor is explicitly defined, Java compiler automatically provides a default no-argument constructor that initializes object fields to default values (null for objects, 0 for numbers, false for boolean).

---

### Q31.

Can we overload constructors in Java?

A. No

B. Yes

C. Only in abstract classes

D. Only with same number of parameters

**Answer:** B

**Explanation:** Yes, constructors can be overloaded (multiple constructors with different parameter lists) in the same class. This allows creating objects in different ways.

---

### Q32.

What is constructor chaining in Java?

A. Creating multiple constructors

B. Calling one constructor from another constructor in the same or parent class

C. Inheriting constructors

D. Overriding constructors

**Answer:** B

**Explanation:** Constructor chaining is the process of calling one constructor from another. Within the same class, use `this()`. To call parent class constructor, use `super()`. This must be the first statement in the constructor.

---

### Q33.

Can constructors be private in Java?

A. No

B. Yes

C. Only in abstract classes

D. Only static constructors

**Answer:** B

**Explanation:** Yes, constructors can be private. Private constructors prevent direct instantiation from outside the class. This is used in Singleton pattern and utility classes.

---

### Q34.

What is a static method in Java?

A. A method that belongs to the class rather than instances

B. A method that cannot be overridden

C. A method that can be called without creating an object

D. Both A and C

**Answer:** D

**Explanation:** A static method belongs to the class itself, not to any specific instance. It can be called using the class name without creating an object. Static methods can only access static members directly.

---

### Q35.

Can we call a non-static method from a static method in Java?

A. Yes, directly

B. No, we need an object instance

C. Only with this keyword

D. Only in abstract classes

**Answer:** B

**Explanation:** No, we cannot call a non-static (instance) method directly from a static method because static methods don't have access to instance context. We need to create an object instance first, then call the non-static method on that object.

---

### Q36.

What is the purpose of the `final` keyword with a variable in Java?

A. The variable becomes a constant and cannot be reassigned

B. The variable can be inherited

C. The variable becomes static

D. The variable is hidden

**Answer:** A

**Explanation:** The `final` keyword with a variable makes it a constant - its value cannot be changed once assigned. For primitive types, the value is fixed. For reference types, the reference cannot point to a different object (but the object's state can still change).

---

### Q37.

What is the instanceof operator used for in Java?

A. To create an instance

B. To test if an object is an instance of a specific class or implements an interface

C. To compare two objects

D. To delete an instance

**Answer:** B

**Explanation:** The `instanceof` operator is used to test whether an object is an instance of a specific class, subclass, or implements an interface. It returns a boolean value. For example: `obj instanceof MyClass`.

---

### Q38.

What is composition in Java?

A. A "has-a" relationship where one class contains objects of other classes

B. An "is-a" relationship

C. Method overloading

D. Interface implementation

**Answer:** A

**Explanation:** Composition is a design principle representing a "has-a" relationship. One class contains instances of other classes as its members. For example, a Car "has-a" Engine. It promotes code reusability without inheritance.

---

### Q39.

What is the difference between composition and inheritance?

A. Composition is "has-a"; Inheritance is "is-a"

B. Composition is more flexible; Inheritance is tightly coupled

C. Composition allows changing behavior at runtime; Inheritance is static

D. All of the above

**Answer:** D

**Explanation:** All statements are correct. Composition represents "has-a" relationships (Car has-a Engine), while inheritance represents "is-a" (Dog is-a Animal). Composition is more flexible, supports runtime changes, and creates looser coupling than inheritance.

---

### Q40.

Can an interface have fields in Java?

A. No

B. Yes, but they are implicitly public, static, and final

C. Only private fields

D. Only protected fields

**Answer:** B

**Explanation:** Yes, interfaces can have fields, but they are implicitly `public static final` (constants). For example: `int MAX_VALUE = 100;` in an interface is automatically public, static, and final.

---

### Q41.

What is method hiding in Java?

A. Making methods private

B. When a static method in a subclass has the same signature as a static method in the parent class

C. Method overriding

D. Abstract methods

**Answer:** B

**Explanation:** Method hiding occurs when a subclass defines a static method with the same signature as a static method in the parent class. Unlike overriding, the method called is determined by the reference type at compile-time, not the object type at runtime.

---

### Q42.

What is a default method in an interface (Java 8+)?

A. An abstract method

B. A method with implementation in an interface using the `default` keyword

C. A private method

D. A static method

**Answer:** B

**Explanation:** From Java 8, interfaces can have default methods - methods with implementation defined using the `default` keyword. This allows adding new methods to interfaces without breaking existing implementations.

---

### Q43.

Can we create an object of an interface?

A. Yes

B. No, but we can create anonymous implementations

C. Only with new keyword

D. Only if it has no methods

**Answer:** B

**Explanation:** We cannot directly instantiate an interface, but we can create anonymous implementations or use lambda expressions (for functional interfaces in Java 8+). For example: `MyInterface obj = new MyInterface() { /* implementation */ };`.

---

### Q44.

What is a functional interface in Java?

A. An interface with multiple abstract methods

B. An interface with exactly one abstract method

C. An interface with only default methods

D. An interface with static methods only

**Answer:** B

**Explanation:** A functional interface has exactly one abstract method (SAM - Single Abstract Method). It can have multiple default or static methods. Functional interfaces can be implemented using lambda expressions. Annotated with `@FunctionalInterface`.

---

### Q45.

What is the purpose of the `@FunctionalInterface` annotation?

A. To mark an interface as functional and enforce single abstract method rule

B. To create lambda expressions

C. To implement default methods

D. To make interface abstract

**Answer:** A

**Explanation:** The `@FunctionalInterface` annotation indicates that an interface is intended to be a functional interface (one abstract method). The compiler will generate an error if the interface doesn't meet this requirement.

---

### Q46.

Can we override `equals()` and `hashCode()` methods in Java?

A. No

B. Yes, and they should be overridden together

C. Only equals()

D. Only hashCode()

**Answer:** B

**Explanation:** Yes, we can and should override both `equals()` and `hashCode()` together when defining custom equality for objects. If two objects are equal according to equals(), they must have the same hashCode(). This is crucial for proper functioning in hash-based collections.

---

### Q47.

What is the Object class in Java?

A. A user-defined class

B. The root of the Java class hierarchy - all classes inherit from it

C. An abstract class

D. An interface

**Answer:** B

**Explanation:** The Object class is the root of the Java class hierarchy. Every class in Java directly or indirectly inherits from Object. It provides methods like equals(), hashCode(), toString(), clone(), etc.

---

### Q48.

Can an abstract class implement an interface without implementing all its methods?

A. No

B. Yes

C. Only if the interface has default methods

D. Only if the abstract class is final

**Answer:** B

**Explanation:** Yes, an abstract class can implement an interface without providing implementations for all abstract methods. The concrete subclass that extends the abstract class must then implement the remaining abstract methods.

---

### Q49.

What is the covariant return type in Java?

A. Returning the same type as declared

B. Overriding a method to return a subtype of the return type declared in the parent class

C. Returning null

D. Returning multiple types

**Answer:** B

**Explanation:** Covariant return type (introduced in Java 5) allows an overriding method to return a subtype (more specific type) of the return type declared in the parent class method. For example, if parent returns Animal, child can return Dog.

---

### Q50.

What is early binding and late binding in Java?

A. Early binding is compile-time; Late binding is runtime

B. Early binding is for static methods; Late binding is for instance methods

C. Early binding is method overloading; Late binding is method overriding

D. All of the above

**Answer:** D

**Explanation:** All statements are correct. Early binding (static/compile-time binding) occurs at compile time for static methods, private methods, and final methods. Late binding (dynamic/runtime binding) occurs at runtime for instance methods (polymorphism/method overriding). Method overloading uses early binding; method overriding uses late binding.

---

**End of MCQ Questions**
