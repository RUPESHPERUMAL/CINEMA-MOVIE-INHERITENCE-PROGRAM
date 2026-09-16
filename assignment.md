# Java Assignment – Cinema Movie Inheritance

## 1. Title

**Cinema Movie Management Using Inheritance and Method Overriding**

## 2. Abstract

This program demonstrates **Inheritance and Method Overriding** in Java using a cinema scenario. The `Movie3D` class inherits properties from the `Movie` class and adds a 3D glasses requirement.

## 3. Objective

* Create a `Movie` class with title and duration.
* Create a `Movie3D` subclass using inheritance.
* Add `glassesRequired` to the 3D movie.
* Override the `display()` method.

## 4. Concepts Used

* Class and Object
* Constructor
* Inheritance
* Method Overriding
* `extends` keyword
* `super()` keyword
* `@Override` annotation

## 5. Algorithm

1. Create the `Movie` class.
2. Declare `title` and `durationMinutes`.
3. Create a constructor to initialize the values.
4. Create the `Movie3D` subclass using `extends`.
5. Add the `glassesRequired` attribute.
6. Use `super()` to initialize parent class values.
7. Override the `display()` method.
8. Create a `Movie3D` object.
9. Display all movie details.

## 6. Program

```java
class Movie {
    String title;
    int durationMinutes;

    Movie(String title, int durationMinutes) {
        this.title = title;
        this.durationMinutes = durationMinutes;
    }

    void display() {
        System.out.println("Title: " + title);
        System.out.println("Duration: " + durationMinutes + " minutes");
    }
}

class Movie3D extends Movie {
    boolean glassesRequired;

    Movie3D(String title, int durationMinutes, boolean glassesRequired) {
        super(title, durationMinutes);
        this.glassesRequired = glassesRequired;
    }

    @Override
    void display() {
        System.out.println("Title: " + title);
        System.out.println("Duration: " + durationMinutes + " minutes");
        System.out.println("3D Glasses Required: " + glassesRequired);
    }
}

public class Main {
    public static void main(String[] args) {
        Movie3D movie = new Movie3D("Avatar 3D", 180, true);
        movie.display();
    }
}
```

## 7. Output

```text
Title: Avatar 3D
Duration: 180 minutes
3D Glasses Required: true
```

## 8. Explanation

* `Movie` is the **parent class**.
* `Movie3D` is the **child class**.
* `extends` is used for inheritance.
* `super()` calls the parent constructor.
* `display()` is overridden in `Movie3D`.
* The object displays all movie details.

## 9. Result

The Java program successfully demonstrates **Inheritance and Method Overriding** using a simple cinema scenario.

## 10. Requirements

* Java JDK 8 or higher
* No external libraries required
