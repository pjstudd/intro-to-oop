# Chapter 7: Introduction to Object-Oriented Programming (OOP)

## What is OOP?

Object-Oriented Programming (OOP) is a programming approach that
organizes code using classes and objects.\
It allows us to model real-world entities in a structured and reusable
way.

In OOP: - A class is a blueprint. - An object is an instance of a
class. - Classes contain attributes (data) and methods (behavior).

------------------------------------------------------------------------

## Core Principles of OOP

### 1. Encapsulation

Encapsulation means bundling data and methods inside a class and
restricting direct access to some data.

Example:

``` python
class Character:
    def __init__(self, name, health):
        self.name = name
        self.__health = health

    def get_health(self):
        return self.__health

    def take_damage(self, damage):
        self.__health -= damage
```

------------------------------------------------------------------------

### 2. Inheritance

Inheritance allows a class to reuse properties and methods from another
class.

Example:

``` python
class Warrior(Character):
    def attack(self):
        print(self.name, "swings a sword!")

class Mage(Character):
    def attack(self):
        print(self.name, "casts a fireball!")
```

------------------------------------------------------------------------

### 3. Polymorphism

Polymorphism means the same method name can behave differently depending
on the object.

Example:

``` python
characters = [
    Warrior("Thor", 100),
    Mage("Merlin", 80)
]

for character in characters:
    character.attack()
```

------------------------------------------------------------------------

## Why Use OOP?

-   Improves code organization
-   Encourages reusability
-   Protects data
-   Makes programs easier to maintain
-   Models real-world systems effectively

------------------------------------------------------------------------

# Activity: Create Your Own Game Character System

## Objective

Apply encapsulation, inheritance, and polymorphism in a simple game
scenario.

## Instructions

1.  Create a base class called Character.
    -   Attributes: name, health
    -   Make health private.
    -   Add methods: get_health() and take_damage(damage)
2.  Create at least two subclasses that inherit from Character.
    -   Example: Archer, Knight, or Healer
    -   Each subclass must have its own attack() method.
3.  Demonstrate polymorphism.
    -   Create a list of different character objects.
    -   Use a loop to call attack() for each object.
4.  Test your program.
    -   Create at least 3 character objects.
    -   Show them attacking.
    -   Show one character taking damage and display remaining health.

## Guide Tips

-   Use super().\_\_init\_\_(name, health) when calling the parent
    constructor.
-   Use clear and meaningful attack messages.
-   Keep your code properly indented and organized.
-   Test each class separately before combining everything.

------------------------------------------------------------------------

Good luck and enjoy building your object-oriented game system!
