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
        name = "Unknown";
        health = 100;
        attackPower = 10;
    }

    // Parameterized constructor
    public Monster(String n, int h, int ap) {
        name = n;
        health = h;
        attackPower = ap;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String n) {
        name = n;
    }

    // Getter for health
    public int getHealth() {
        return health;
    }

    // Setter for health
    public void setHealth(int h) {
        health = h;
    }

    // Getter for attackPower
    public int getAttackPower() {
        return attackPower;
    }

    // Setter for attackPower
    public void setAttackPower(int ap) {
        attackPower = ap;
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
        name = "Unknown";
        age = 18;
        gpa = 0.0;
        credits = 0;
    }

    // Parameterized constructor
    public Student(String n, int a, double g, int c) {
        name = n;
        age = a;
        gpa = g;
        credits = c;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String n) {
        name = n;
    }

    // Getter for age
    public int getAge() {
        return age;
    }

    // Setter for age
    public void setAge(int a) {
        age = a;
    }

    // Getter for gpa
    public double getGpa() {
        return gpa;
    }

    // Setter for gpa
    public void setGpa(double g) {
        gpa = g;
    }

    // Getter for credits
    public int getCredits() {
        return credits;
    }

    // Setter for credits
    public void setCredits(int c) {
        credits = c;
    }

    // Method to determine if the student can graduate
    public boolean canGraduate() {
        return gpa >= 2.0 && credits >= 120;
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
## RNG.java Class Example

This section provides an example of the `RNG.java` class, which includes three instance variables, two constructors, a method to choose a random value within the specified range, and a method to compare a user's guess with the random value.

Here is a sample `RNG.java` class:
```java
import java.util.Random;

public class RNG {
    private int lowValue;
    private int highValue;
    private int randomValue;

    // Constructor with low and high values
    public RNG(int l, int h) {
        lowValue = l;
        highValue = h;
        randomValue = chooseRandom();
    }

    // Constructor with high value only, low value set to 0
    public RNG(int h) {
        lowValue = 0;
        highValue = h;
        randomValue = chooseRandom();
    }

    // Method to choose a random value within the range
    private int chooseRandom() {
        Random rand = new Random();
        return rand.nextInt((highValue - lowValue) + 1) + lowValue;
    }

    // Method to compare user's guess with the random value
    public void compare(int userGuess) {
        boolean isExact = userGuess == randomValue;
        boolean isHigher = userGuess > randomValue;
        boolean isLower = userGuess < randomValue;

        System.out.println("Guess is exact: " + isExact);
        System.out.println("Guess is higher: " + isHigher);
        System.out.println("Guess is lower: " + isLower);
    }

    // toString method
    @Override
    public String toString() {
        return "RNG{lowValue=" + lowValue + ", highValue=" + highValue + ", randomValue=" + randomValue + "}";
    }
}
```

