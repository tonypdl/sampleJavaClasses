# sampleJavaClasses

- [Monster.java Class Example](#monsterjava-class-example)
- [Student.java Class Example](#studentjava-class-example)
- [Animal.java Class Example](#animaljava-class-example)
- [RNG.java Class Example](#RNGjava-class-example)

These Class Examples should provide some possible builds for general classes in Java when first learning how to write classes.

## Monster.java Class Example

This section provides an example of the `Monster.java` class, which includes three instance variables, two constructors (one with no parameters), three set methods, three get methods, and a `toString` method.

Here is sample Monster.java class with three instance variables, two constructors (one with no parameters), three set methods, three get methods, and a toString.
```java
public class Monster {
    private String name;
    private int health;
    private int attackPower;

    // No-parameter constructor
    public Monster() {
        this.name = "Unknown";
        this.health = 100;
        this.attackPower = 10;
    }

    // Parameterized constructor
    public Monster(String name, int health, int attackPower) {
        this.name = name;
        this.health = health;
        this.attackPower = attackPower;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter for health
    public int getHealth() {
        return health;
    }

    // Setter for health
    public void setHealth(int health) {
        this.health = health;
    }

    // Getter for attackPower
    public int getAttackPower() {
        return attackPower;
    }

    // Setter for attackPower
    public void setAttackPower(int attackPower) {
        this.attackPower = attackPower;
    }

    // toString method
    @Override
    public String toString() {
        return "Monster{name='" + name + "', health=" + health + ", attackPower=" + attackPower + "}";
    }
}
```

## Student.java Class Example

This section provides an example of the `Student.java` class, which includes four instance variables, two constructors (one with no parameters), four set methods, four get methods, a method to determine if the student can graduate based on their GPA, and a `toString` method.

Here is a sample `Student.java` class:
```java
public class Student {
    private String name;
    private int age;
    private double gpa;
    private int credits;

    // No-parameter constructor
    public Student() {
        this.name = "Unknown";
        this.age = 18;
        this.gpa = 0.0;
        this.credits = 0;
    }

    // Parameterized constructor
    public Student(String name, int age, double gpa, int credits) {
        this.name = name;
        this.age = age;
        this.gpa = gpa;
        this.credits = credits;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter for age
    public int getAge() {
        return age;
    }

    // Setter for age
    public void setAge(int age) {
        this.age = age;
    }

    // Getter for gpa
    public double getGpa() {
        return gpa;
    }

    // Setter for gpa
    public void setGpa(double gpa) {
        this.gpa = gpa;
    }

    // Getter for credits
    public int getCredits() {
        return credits;
    }

    // Setter for credits
    public void setCredits(int credits) {
        this.credits = credits;
    }

    // Method to determine if the student can graduate
    public boolean canGraduate() {
        return this.gpa >= 2.0 && this.credits >= 120;
    }

    // toString method
    @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + ", gpa=" + gpa + ", credits=" + credits + "}";
    }
}
```

## Animal.java Class Example

This section provides an example of the `Animal.java` class, which includes four instance variables, two constructors (one with no parameters), four set methods, four get methods, a method to calculate the time left until the animal can be sent back to the wild, and a `toString` method.

Here is a sample `Animal.java` class:
```java
public class Animal {
    private String species;
    private String name;
    private int age;
    private int yearsInZoo;

    // No-parameter constructor
    public Animal() {
        this.species = "Unknown";
        this.name = "Unknown";
        this.age = 0;
        this.yearsInZoo = 0;
    }

    // Parameterized constructor
    public Animal(String species, String name, int age, int yearsInZoo) {
        this.species = species;
        this.name = name;
        this.age = age;
        this.yearsInZoo = yearsInZoo;
    }

    // Getter for species
    public String getSpecies() {
        return species;
    }

    // Setter for species
    public void setSpecies(String species) {
        this.species = species;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter for age
    public int getAge() {
        return age;
    }

    // Setter for age
    public void setAge(int age) {
        this.age = age;
    }

    // Getter for yearsInZoo
    public int getYearsInZoo() {
        return yearsInZoo;
    }

    // Setter for yearsInZoo
    public void setYearsInZoo(int yearsInZoo) {
        this.yearsInZoo = yearsInZoo;
    }

    // Method to calculate time left until the animal can be sent back to the wild
    public int timeUntilRelease(int requiredYearsInZoo) {
        return requiredYearsInZoo - this.yearsInZoo;
    }

    // toString method
    @Override
    public String toString() {
        return "Animal{species='" + species + "', name='" + name + "', age=" + age + ", yearsInZoo=" + yearsInZoo + "}";
    }
}
```


