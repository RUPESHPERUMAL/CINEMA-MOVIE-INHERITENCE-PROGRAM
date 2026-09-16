# 🎬 Java Cinema Movie Inheritance

## 📌 Description

This Java program demonstrates **Inheritance and Method Overriding** using a cinema scenario.

* `Movie` is the **parent class**.
* `Movie3D` is the **child class** that extends `Movie`.
* `Movie3D` adds an extra attribute called `glassesRequired`.
* The `display()` method is overridden to display all movie details.

## 🎯 Objective

* To demonstrate **Inheritance** in Java.
* To demonstrate **Method Overriding**.
* To use a **constructor** to initialize movie details.
* To display details of a 3D movie.

## 🧠 Concepts Used

* Classes and Objects
* Constructors
* Inheritance
* Method Overriding
* `extends` keyword
* `super()` keyword
* `@Override` annotation

## 💻 Program

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

## 🖥️ Output

```text
Title: Avatar 3D
Duration: 180 minutes
3D Glasses Required: true
```

## 🔍 How It Works

1. The `Movie` class stores the movie title and duration.
2. The `Movie3D` class inherits the properties of `Movie`.
3. `glassesRequired` is added to represent the need for 3D glasses.
4. `super()` calls the constructor of the parent class.
5. `display()` is overridden in `Movie3D`.
6. The `Movie3D` object displays all the movie details.

## 📂 File Structure

```text
Java-Cinema-Movie/
│
├── Main.java
└── README.md
```

## ✅ Result

The program successfully demonstrates **Inheritance and Method Overriding in Java** using a cinema movie example.
