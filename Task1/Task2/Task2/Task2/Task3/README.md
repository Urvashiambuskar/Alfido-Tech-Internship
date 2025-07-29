# ✅ Task 3 – OOP with Classes

This Java program demonstrates:
- Classes and Objects
- Inheritance
- Method Overriding


## 🎯 Objective

Create a `Person` class and a `Student` class that inherits from it.  
Use method overriding to display full student info.



## 💻 Java Code

// Parent class
class Person {
    String name;
    int age;

    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method to display info
    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

// Child class
class Student extends Person {
    String college;

    // Constructor
    Student(String name, int age, String college) {
        super(name, age); // call parent constructor
        this.college = college;
    }

    // Method overriding
    @Override
    void displayInfo() {
        super.displayInfo(); // call parent method
        System.out.println("College: " + college);
    }
}

// Main class
public class OOPDemo {
    public static void main(String[] args) {
        // Create a student object
        Student s1 = new Student("Urvashi Ambuskar", 18, "Govt. Women's Polytechnic, Indore");
        
        // Call display method
        s1.displayInfo();
    }
}



## 📤 Output
Name: Urvashi Ambuskar
Age: 18
College: Govt. Women's Polytechnic, Indore

