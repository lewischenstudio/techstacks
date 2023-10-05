# The SOLID Design Principles

#### Table of Contents

- [Introduction](#introduction)
- [Single Responsibility Principle](#single-responsibility-principle)
- [Open-Closed Principle](#open-closed-principle)
- [Liskov Substitution Principle](#liskov-substitution-principle)
- [Interface Segregation Principle](#interface-segregation-principle)
- [Dependency Inversion Principle](#dependency-inversion-principle)
- [Conclusion](#conclusion)

### Introduction

SOLID is a popular set of design principles that are used in object-oriented
software development. SOLID is an acronym that stands for five key design
principles:

- single responsibility principle
- open-closed principle
- Liskov substitution principle
- interface segregation principle, and
- dependency inversion principle.

All five are commonly used by software engineers and provide some important
benefits for developers.

The SOLID principles were developed by Robert C. Martin in a 2000 essay, "Design
Principles and Design Patterns," although the acronym was coined later by
Michael Feathers. In his essay, Martin acknowledged that successful software
will change and develop. As it changes, it becomes increasingly complex. Without
good design principles, Martin warns that software becomes rigid, fragile,
immobile, and viscous. The SOLID principles were developed to combat these
problematic design patterns.

The broad goal of the SOLID principles is to reduce dependencies so that
engineers change one area of software without impacting others. Additionally,
they're intended to make designs easier to understand, maintain, and extend.
Ultimately, using these design principles makes it easier for software engineers
to avoid issues and to build adaptive, effective, and agile software.

While the principles come with many benefits, following the principles generally
leads to writing longer and more complex code. This means that it can extend the
design process and make development a little more difficult. However, this extra
time and effort is well worth it because it makes software so much easier to
maintain, test, and extend.

Following these principles is not a cure-all and won't avoid design issues. That
said, the principles have become popular because when followed correctly, they
lead to better code for readability, maintainability, design patterns, and
testability. In the current environment, all developers should know and utilize
these principles.

### Single Responsibility Principle

Robert Martin summarizes this principle well by mandating that, "a class should
have one, and only one, reason to change." Following this principle means that
each class only does one thing and every class or module only has responsibility
for one part of the software's functionality. More simply, each class should
solve only one problem.

Single responsibility principle (SRP) is a relatively basic principle that most
developers are already utilizing to build code. It can be applied to classes,
software components, and microservices.

Utilizing this principle makes code easier to test and maintain, it makes
software easier to implement, and it helps to avoid unanticipated side-effects
of future changes.

To ensure that you're following this principle in development, consider using an
automated check on build to limit the scope of classes. This check is not a
foolproof way to make sure that you're following single responsibility
principle, but it can be a good way to make sure that classes are not violating
this principle.

The name itself suggest that the "class should be having one and only one
responsibility". What does it mean? Well let's take the class A which does the
following operations.

- Open a database connection
- Fetch data from database
- Write the data in an external file

The issue with this class is that it handles lot of operations. Suppose any of
the following change happens in future.

- New database
- Adopt ORM to manage queries on database
- Change in the output structure

So in all the cases the above class would be changed. Which might affect the
implementation of the other two operations as well. So ideally according to SRP
there should be three classes each having the single responsibility.

### Open-Closed Principle

The idea of open-closed principle is that existing, well-tested classes will
need to be modified when something needs to be added. Yet, changing classes can
lead to problems or bugs. Instead of changing the class, you simply want to
extend it. With that goal in mind, Martin summarizes this principle, "You should
be able to extend a class's behavior without modifying it."

Following this principle is essential for writing code that is easy to maintain
and revise. Your class complies with this principle if it is:

- Open for extension, meaning that the class's behavior can be extended; and
- Closed for modification, meaning that the source code is set and cannot be
  changed.

At first glance, these two criteria seem to be inherently contradictory, but
when you become more comfortable with it, you'll see that it's not as
complicated as it seems. The way to comply with these principles and to make
sure that your class is easily extendable without having to modify the code is
through the use of abstractions. Using inheritance or interfaces that allow
polymorphic substitutions is a common way to comply with this principle.
Regardless of the method used, it's important to follow this principle in order
to write code that is maintainable and revisable.

This principle suggests that "classes should be open for extension but closed
for modification". What is means is that if the class A is written by the
developer AA, and if the developer BB wants some modification on that then
developer BB should be easily do that by extending class A, but not by modifying
class A.

### Liskov Substitution Principle

Of the five SOLID principles, the Liskov Substitution Principle is perhaps the
most difficult one to understand. Broadly, this principle simply requires that
every derived class should be substitutable for its parent class. The principle
is named for Barbara Liskov, who introduced this concept of behavioral subtyping
in 1987. Liskov herself explains the principle by saying:

What is wanted here is something like the following substitution property: if
for each object O1 of type S there is an object O2 of type T such that for all
programs P defined in terms of T, the behavior of P is unchanged when O1 is
substituted for O2 then S is a subtype of T.

While this can be a difficult principle to internalize, in a lot of ways it's
simply an extension of open-closed principle, as it's a way of ensuring that
derived classes extend the base class without changing behavior.

Following this principle helps to avoid unexpected consequences of changes and
avoids having to open a closed class in order to make changes. It leads to easy
extensions of software, and, while it might slow down the development process,
following this principle during development can avoid lots of issues during
updates and extensions.

This principle suggests that "parent classes should be easily substituted with
their child classes without blowing up the application". Let's take following
example to understand this.

Let's consider an Animal parent class.

```java
public class Animal {
  public void makeNoise() {
    System.out.println("I am making noise");
  }
}
```

Now let's consider the Cat and Dog classes which extends Animal.

```java
public class Dog extends Animal {
  @Override
  public void makeNoise() {
    System.out.println("bow wow");
  }
}

public class Cat extends Animal {
  @Override
  public void makeNoise() {
    System.out.println("meow meow");
  }
}
```

Now, wherever in our code we were using Animal class object we must be able to
replace it with the Dog or Cat without exploding our code. What do we mean here
is the child class should not implement code such that if it is replaced by the
parent class then the application will stop running. For ex. if the following
class is replace by Animal then our app will crash.

```java
class DumbDog extends Animal {
  @Override
  public void makeNoise() {
    throw new RuntimeException("I can't make noise");
  }
}
```

### Interface Segregation Principle

The general idea of interface segregation principle is that it's better to have
a lot of smaller interfaces than a few bigger ones. Martin explains this
principle by advising, "Make fine grained interfaces that are client-specific.
Clients should not be forced to implement interfaces they do not use."

For software engineers, this means that you don't want to just start with an
existing interface and add new methods. Instead, start by building a new
interface and then let your class implement multiple interfaces as needed.
Smaller interfaces mean that developers should have a preference for composition
over inheritance and for decoupling over coupling. According to this principle,
engineers should work to have many client-specific interfaces, avoiding the
temptation of having one big, general-purpose interface.

This principle suggests that "many client specific interfaces are better than
one general interface". This is the first principle which is applied on
interface, all the above three principles applies on classes. Let's take
following example to understand this principle.

```java
/**
 * Interface definition for a callback to be invoked when a view is clicked.
 */
public interface OnClickListener {
  /**
   * Called when a view has been clicked.
   *
   * @param v The view that was clicked.
   */
  void onClick(View v);
}
/**
 * Interface definition for a callback to be invoked when a view has been clicked and held.
 */
public interface OnLongClickListener {
  /**
   * Called when a view has been clicked and held.
   *
   * @param v The view that was clicked and held.
   *
   * @return true if the callback consumed the long click, false otherwise.
   */
  boolean onLongClick(View v);
}
```

Why do we need two interfaces just for same action with one single tap and
another with long press. Why can't we have following interface.

```java
public interface MyOnClickListener {
    void onClick(View v);
    boolean onLongClick(View v);
}
```

If we have this interface then it will force clients to implement onLongClick
even if they don't even care about long press. Which will lead to overhead of
unused methods. So having two separate interfaces helps in removing the unused
methods. If any client want both behaviours then they can implement both
interfaces.

### Dependency Inversion Principle

This principle offers a way to decouple software modules. Simply put, dependency
inversion principle means that developers should "depend on abstractions, not on
concretions." Martin further explains this principle by asserting that, "high
level modules should not depend upon low level modules. Both should depend on
abstractions." Further, "abstractions should not depend on details. Details
should depend upon abstractions."

What does it mean that we should be having object of interface which helps us to
communicate with the concrete classes. What do we gain from this is, we hide the
actual implementation of class A from the class B. So if class A changes the
class B doesn't need to care or know about the changes.

One popular way to comply with this principle is through the use of a dependency
inversion pattern, although this method is not the only way to do so. Whatever
method you choose to utilize, finding a way to utilize this principle will make
your code more flexible, agile, and reusable.

### Conclusion

Implementing SOLID design principles during development will lead to systems
that are more maintainable, scalable, testable, and reusable. In the current
environment, these principles are used globally by engineers. As a result, to
create good code and to use design principles that are competitive while meeting
industry standards, it's essential to utilize these principles.

[Content Source](https://www.bmc.com/blogs/solid-design-principles/)
[Content Source](https://medium.com/mindorks/solid-principles-explained-with-examples-79d1ce114ace)
